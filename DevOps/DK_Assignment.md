## Docker Assignement

## Q
#### Create a container using ubuntu image. Install python in it. Save the container as a image. Delete earlier container. Create a new container and run python in it. 

1. Create a container using the Ubuntu image
```
# Pull the latest Ubuntu image
docker pull ubuntu:latest

# Create and run a new container from the Ubuntu image
docker run -it --name container1 ubuntu:latest

```

2. Install Python in the container
```
# Update package list and install Python
apt update
apt install -y python3
python3 --version
```

3. Save the container as a new image
```
exit

```

4. save the container as a new image
```
# Commit the container as a new image
docker commit container1 container2

```

5. Delete the earlier container
```
# Remove the old container
docker rm container1

```

6. Create a new container and run Python in it
```
# Run a new container from the saved image
docker run -it --name pythoncontainer container2

# Once inside the container, run Python
python3

```

## Q
### Create a container using httpd image. Map outside port 9000. open localhost:9000 on your docker machine. It should display It Works message.

1. Pull the httpd image
```
docker pull httpd:latest

```
2. Run the container and map port 9000
```
docker run -d --name container1 -p 9000:80 httpd:latest

```

3. Access the "It Works" page
```
http://localhost:9000

```
- to stop container on port 
```
docker ps

docker stop container1

```
## Q
### Create a directory on the local file system. Create an index.html file inside this directory. Create a container using httpd image and map this directory to the container. Also map port 8500 to the container. Display the original message accessing the website. 

1. Create a directory on the local filesystem
```
mkdir directory

cd directory

vim index.html

```
2. Create the index.html file:

```
<html>
</head>
<body>
    <h1>It Works!</h1>
    <p>Hello, This is the original message displayed from the web server container.</p>
</body>
</html>

```

3. Run the container and map the directory and port:

```
docker run -d --name container1 -p 8500:80 

```

4. check
```
http://localhost:8500

```

## Q
## Modify the index.html file in the directory. Access the website and display that modified contents are displayed on the website.
## Create 10 containers mapped to the same directory. Assign ports from 8510 to 8520. Display that all websites show the same content.

1. step 1

```
cd directory 

vim index.html

```

```
<html>
<body>
  <h1>Modified Content: All Containers Display the Same Page</h1>
</body>
</html>

```

2. Run 10 Docker containers mapped to the same directory


- do it by the docker compose or add container in loop
```
for i in {8510..8520}; do
  docker run -d \
    -p $i:80 \
    -v /path/to/your/directory:/usr/local/apache2/htdocs/ \
    --name httpd-container-$i \
    httpd
done

```
3. Verify all containers are running
```
docker ps

```

4. stop all container

```
docker stop httpd-container-8510 httpd-container-8511 httpd-container-8512 ...

```


## Q
##Create a python program that takes 2 numbers from the user and displays addition and multiplication result. Now create an image of this program. Run the container from this image and display the results.

1. Python Program (calc.py)
```
# calc.py

def main():
    # Taking two numbers as input from the user
    num1 = float(input("Enter the first number: "))
    num2 = float(input("Enter the second number: "))

    # Perform addition and multiplication
    addition = num1 + num2
    multiplication = num1 * num2

    # Display the results
    print(f"Addition result: {addition}")
    print(f"Multiplication result: {multiplication}")

if __name__ == "__main__":
    main()


```

2. Create a Dockerfile for the Python Program

```
# Use an official Python image as a base
FROM python:3.9-slim

# Copy the Python script into the container
COPY calc.py /calc.py

# Set the default command to run the Python script
CMD ["python", "/calc.py"]

```

3. Build the Docker Image
```
docker build -t python-calc .

```

 4. Run the Docker Container

 ```
 docker run -it python-calc

 ```



## Q
##Cteate a directory. Create an index.html file. Create a image using httpd image. Copy index.html inside the container. Run the container and map port 8200 using your image and display the webpage is displayed.

1. Create a Directory and index.html File
```
mkdir directory
cd directory

```
```
echo "<html><body><h1>Welcome to My Website</h1></body></html>" > index.html

```
2. Create the httpd Container
```
docker run -d \
  -p 8200:80 \
  --name my-httpd-container \
  -v /path/to/your/directory:/usr/local/apache2/htdocs/ \
  httpd

```
##check
http://localhost:8200


## Q
##Create a docker compose file to start 4 containers using httpd image. Map ports 5000, 6000, 7000 and 8000. Port 8000 website should display “Welcome to ACTS”. Port 5000 should display “Welcome to HPCSA”. Port 6000 should display “Welcome to DITISS” and port 7000 should display “Welcome to DAI”. Use docker-compose command.

## structure should

```
my project/
-----------docker_compose.yml
-----------web/
-----------------hpcsa/
------------------------index.html
-----------------dittis/
------------------------index.html
-----------------dai/
------------------------index.html
-----------------acts/
------------------------index.html

```


1. Create docker-compose.yml

```
version: '3.7'

services:
  web5000:
    image: httpd
    container_name: web5000
    ports:
      - "5000:80"
    volumes:
      - ./web5000/index.html:/usr/local/apache2/htdocs/index.html

  web6000:
    image: httpd
    container_name: web6000
    ports:
      - "6000:80"
    volumes:
      - ./web6000/index.html:/usr/local/apache2/htdocs/index.html

  web7000:
    image: httpd
    container_name: web7000
    ports:
      - "7000:80"
    volumes:
      - ./web7000/index.html:/usr/local/apache2/htdocs/index.html

  web8000:
    image: httpd
    container_name: web8000
    ports:
      - "8000:80"
    volumes:
      - ./web8000/index.html:/usr/local/apache2/htdocs/index.html

```

3. Start the Containers Using Docker Compose
```
docker-compose up -d

```

## Q
 cereate a directory create an index.html file the index.html the index.html
 file will display message "this application is running on kubernetes"cretae a image using httpd image copy index.html inside the container runthe container and map port 8200 using your image and display the webpage is displayd

### Step 1: Create Project Directory
```
mkdir project
cd project
```
### Step 2: Create index.html File
```
echo "This application is running on Kubernetes" > index.html
```
### Step 3: Create Dockerfile
### Dockerfile content
```
FROM httpd:latest
COPY index.html /usr/local/apache2/htdocs/
EXPOSE 80
```
### Step 4: Build the Docker Image
```
docker build -t my-httpd-app .
```
### Step 5: Run the Docker Container
```
docker run -d -p 8200:80 my-httpd-app
```
### Step 6: Verify the Webpage
```
curl http://localhost:8200
```


## Q
create a repository on your docker hub account push this image to docker repo


### Step 1: Log in to Docker Hub

### create a repo manually
```
docker login
```
### Step 2: Tag the local image with your Docker Hub username and repository name
```
docker tag <local-image-name> <dockerhub-username>/<repository-name>:<tag>
```
### Example:
```
docker tag my-httpd-app johndoe/my-repo:latest
```
### Step 3: Push the image to Docker Hub
```
docker push <dockerhub-username>/<repository-name>:<tag>
```
### Example:
```
docker push johndoe/my-repo:latest
```


## ------------------------------Advance------------------------------------

## Q
##Create a image of the test.py file. Create a network by name app2. Create a MYSQL container and connect it to this network. Now create a container of test.py application and connect it to the same network and display that the database is created.

1. Python Script (test.py)
```
import mysql.connector
from mysql.connector import errorcode

# Connect to MySQL
try:
    conn = mysql.connector.connect(
        host="dbserver",  # Hostname of MySQL container
        user="root",       # MySQL root user
        password="pass@123"  # MySQL root password
    )
    cursor = conn.cursor()

    # Create 'students' database
    cursor.execute("CREATE DATABASE IF NOT EXISTS students")

    # Switch to the 'students' database
    cursor.execute("USE students")

    # Create a table 'batch24'
    cursor.execute("""
    CREATE TABLE IF NOT EXISTS batch24 (
        id INT AUTO_INCREMENT PRIMARY KEY,
        name VARCHAR(100),
        age INT
    )
    """)

    print("Database 'students' and table 'batch24' created successfully.")

except mysql.connector.Error as err:
    print(f"Error: {err}")
finally:
    cursor.close()
    conn.close()

```
2. Create a Dockerfile for test.py

```
# Use official Python image as base
FROM python:3.9-slim

# Install MySQL connector
RUN pip install mysql-connector-python

# Copy the Python script into the container
COPY test.py /test.py

# Command to run the script
CMD ["python", "/test.py"]

```

 3. Build the Docker Image
 ```
 docker build -t python-mysql-app .

 ```
 4. Create the app2 Network

 ```
 docker network create app2

 ```

 5. Run the MySQL Container and Attach to app2

 ```
 docker run -d \
  --name dbserver \
  --network app2 \
  -e MYSQL_ROOT_PASSWORD=pass@123 \
  mysql:latest

 ```
 6. Run the Python Container and Connect to app2

 ```
 docker run --rm \
  --network app2 \
  python-mysql-app

 ```




## Q
##create a network by name hpcsa. Run a mysql container and attach it to this network. Keep the name of the mysql container as dbserver. The root password should be “pass@123”. Not create a python container and run the test.py script and create a database by name students. And create a table by name batch24. Display the output of the script.

1. Create a custom Docker network
```
docker network create hpcsa

```
2. Run the MySQL container (dbserver)
```
docker run -d \
  --name dbserver \
  --network hpcsa \
  -e MYSQL_ROOT_PASSWORD=pass@123 \
  mysql:latest

```

 3. Create the Python container and script (test.py)

 ```
 import mysql.connector
from mysql.connector import errorcode

# Connect to the MySQL database
try:
    conn = mysql.connector.connect(
        host="dbserver",  # Name of the MySQL container (reachable within the network)
        user="root",       # MySQL user (root)
        password="pass@123"  # Root password
    )
    cursor = conn.cursor()

    # Create database 'students'
    cursor.execute("CREATE DATABASE IF NOT EXISTS students")

    # Use the 'students' database
    cursor.execute("USE students")

    # Create table 'batch24'
    cursor.execute("""
    CREATE TABLE IF NOT EXISTS batch24 (
        id INT AUTO_INCREMENT PRIMARY KEY,
        name VARCHAR(100),
        age INT
    )
    """)

    print("Database 'students' and table 'batch24' created successfully.")

except mysql.connector.Error as err:
    print(f"Error: {err}")
finally:
    cursor.close()
    conn.close()

 ```

 ##  Dockerfile
 ```
 # Use an official Python image as a base
FROM python:3.9-slim

# Install MySQL connector for Python
RUN pip install mysql-connector-python

# Copy the test.py script into the container
COPY test.py /test.py

# Command to run the script
CMD ["python", "/test.py"]

 ```

##  Build the Docker image.
 ```
 docker build -t python-mysql .

 ```

 4. Run the Python container and execute the script
 ```
 docker run --rm \
  --network hpcsa \
  python-mysql

 ```

 5. Verify the output and MySQL changes
 ```
 Database 'students' and table 'batch24' created successfully.

 ```
 - Log into the MySQL container:
 ```
 docker exec -it dbserver mysql -u root -p


 ```
 - Verify the database and table:
 ```
 SHOW DATABASES;
USE students;
SHOW TABLES;

 ```

 ## Recap of the Steps:
 - Created the network hpcsa for the containers to communicate.
- Ran a MySQL container with the name dbserver, connected to the network, and set the root password.
- Created a Python script (test.py) that connects to MySQL, creates a database (students), and creates a table (batch24).
- Built and ran a Python container, which executed the script to create the database and table.
- Verified the output and confirmed the creation of the database and table by accessing the MySQL container.


##  Kubernetes

## Q
 on the Kubernetes cluster create a deployment using httpd image check
 on which node the pod is runing create a service of type nodeport for this
 deployment check the port assigned for this service use url to access
 website on the specified port on the node address

### Step 1: Create a Deployment with the httpd Image
```
kubectl create deployment httpd-deployment --image=httpd
```
### Verify the Deployment

```
kubectl get deployments
kubectl get pods
```
### Step 2: Expose the Deployment as a NodePort Service
```
kubectl expose deployment httpd-deployment --type=NodePort --name=httpd-service --port=80 --target-port=80
```

### Check the assigned NodePort
```
kubectl get svc httpd-service
```
### Step 3: Check on Which Node the Pod is Running
```
kubectl get pod -o wide
```
### Get Node IP
```
kubectl get nodes -o wide
```
### Access the website using http://<node-ip>:<node-port>
```
curl http://<node-ip>:<node-port>
```



 ## Q
 scale the deployment to create 10 pods check on which node the pods are
 running check the ip addresses assigned to the pods try accessing website
 on all node ip and specified port then scale the deployment to 2 replic

 ### Step 4: Scale the Deployment to 10 Pods
```
kubectl scale deployment httpd-deployment --replicas=10
```
### Check the IPs of the pods
```
kubectl get pods -o wide
```
### Access the website again using curl
```
curl http://<node-ip>:<node-port>
```

### Step 5: Scale the Deployment Back to 2 Replicas
```
kubectl scale deployment httpd-deployment --replicas=2
```
### Check the running nodes
```
kubectl get nodes
```
### Check the service and port
```
kubectl get svc httpd-service
```
### Check which pods are running on which node

```
kubectl get pods -o wide
```
### Access the website again using curl
```
curl http://<node-ip>:<node-port>
```