# DOCKER
- Docker is containerization platform for developing, packaging, shipping, and running application
- it provides the ability to run an appliction in an isolated environment called a container.
- makes deployment and development efficient  

## why we need Docker
- **Consistent Environment**: Ensures apps run the same across all environments.
- **Lightweight**: Uses fewer resources compared to virtual machines.
- **Fast Deployment**: Quick to start and deploy containers.
- **Isolation**: Keeps applications and dependencies separate.
- **Scalability**: Simplifies scaling applications up or down.
- **Portability**: Run containers on any system with Docker installed.
- **Efficient Resource Use**: Shares OS kernel, saving space.

## what is container
- a way to package an application with all the necessary dependencies and configuration.
- it can be easily sheared
- makes deployment and development efficient

## Architecture of docker
![alt text](<Screenshot 2024-11-09 180541-1.png>)
- Running multiple version of same Application in diffrent container

## vm vs Docker


| Virtual Machine (VM)                               | Docker Container                               |
|-----------------------------------------------------|-------------------------------------------------|
| High impact on OS, uses more disk space            | Low impact on OS, very fast, low disk space usage |
| Slower, takes minutes                              | Fast, starts in seconds                         |
| More complex, larger size                          | Easy sharing, rebuilding, and distribution      |
| Encapsulates the entire machine (OS + app)         | Encapsulates only the app and its dependencies  |
| Full isolation with separate OS                    | Shares host OS kernel, lighter isolation        |
| Less portable, dependent on hypervisor             | Highly portable across different environments   |

## Main Components of Docker

- **Dockerfile**: 
  - A text file containing instructions to build a Docker image.
  
- **Docker Image**: 
  - A snapshot of an application and its environment. 
  - Can be run using the Docker engine and shared to another server.

- **Docker Container**: 
  - A running instance of a Docker image that encapsulates the application and its dependencies.

- **Docker Registry**: 
  - A central repository for storing and distributing Docker images.

  
![alt text](<Screenshot 2024-11-09 183002-1.png>)


## Registry vs Repository

- **Registry**: A server that stores and manages Docker images (e.g. Docker Hub).
- **Repository**: A collection of related images (e.g., different versions) within a registry.



## 1 ) make demo project
- PS D:\docker\testapp> npx create-react-app testapp    
- cd testapp
- npm start

## 2 ) make docker File

```
# Use the official Node.js 20 image as the base image for the container

FROM node:20

# Set the working directory inside the container to /myapp

WORKDIR /myapp

# Copy all files from the current directory on the host 
#machine to the working directory inside the container

COPY . .

# Run 'npm install' to install all dependencies listed in package.json

RUN npm install

# Expose port 3000 to allow communication to/from the container 
#on that port (typically used by web servers)

EXPOSE 3000

# Set the default command to run when the container starts 
#- in this case, run 'npm start' to start the application

CMD ["npm", "start"]

```
## 3 ) creating Docker image

- docker build .
  
- PS D:\docker\testapp> docker image ls

```
REPOSITORY   TAG       IMAGE ID       CREATED         SIZE
<none>       <none>    371dd50e01e7   2 minutes ago   2.11GB
```
## 4 ) Run & Manage Docker Container
```

   D:\docker\testapp> docker run 371dd50e01e7

   D:\docker\testapp> docker stop nostalgic_driscoll
```
- **probleam**  our website on port 300 works in container but not outside the container

- so we can port bind it to acsses it outside by command
```

  D:\docker\testapp> docker run -p 3000:3000 bbea29057f25
```


- docker run: Starts a new container.
- -p 3000:3000: Maps port 3000 on your host to port 3000 in the container.
- bbea29057f25: Specifies the image ID to use for the container.
- This runs the container and makes the app accessible at http://localhost:3000


## Running Container Detached mode (Background)

```
D:\docker\testapp> docker run -d  -p 3000:3000 bbea29057f25
```
- -d: Runs the container in detached mode, meaning it runs in the background and doesn’t block your terminal.

## Running multiple containers

- now we have host our web on port 3000
- so for another container we need anotehr port we can't hosgt on the same port
```
D:\docker\testapp> docker run -d  -p 3001:3000 bbea29057f25
```

- now we have two container  by same docker image id

- every container is isolated by each 

- so they run on same outer innner port called 3000/tcp

```
CONTAINER ID   IMAGE          COMMAND              PORTS                            NAMES
e3c352cd173e   bbea29057f25   "httpd-foreground"   80/tcp, 0.0.0.0:3001->3000/tcp   interesting_sinoussi
9feed702602e   bbea29057f25   "httpd-foreground"   80/tcp, 0.0.0.0:3000->3000/tcp   tender_tesla
```


## usefull info to manage container


```
docker ps
```
- show only running processes

```
docker ps -a
```
- show all container

```
docker rm  
```
- delete container

```
D:\docker\testapp> docker run -d --rm  -p 3001:3000 bbea29057f25
```
- -- rm will remove the container automaticly when you stop it 


```
D:\docker\testapp> docker run -d --rm --name "ashutoshapp"  -p 3001:3000 bbea29057f25
```

- --name " " will ad name to container
```
docker stop ashutoshapp
```  

## managing docker images 

- cheak docker images
```
docker image ls
```
- until now we are using image id
- but we can give it name (tag)
```
docker build -t ashutoshapp:01 .
```
- -t tag 
- ashutoshapp:01 name and : version 

- . means Docker will use the current directory as the source for the build context

  
  
  ````
  PS D:\docker\testapp> docker image ls
```
REPOSITORY    TAG       IMAGE ID       CREATED        SIZE
ashutoshapp   01        075d6eb7cb0f   4 hours ago    2.11GB
<none>        <none>    371dd50e01e7   4 hours ago    2.11GB
httpd         latest    bbea29057f25   3 months ago   221MB
```

- delete image
```
docker rmi asutoshapp
```
## what if we update project

- make another version
```
docker build -t ashutoshapp:02 .
```

## pre define docker images
ngnix web server
- wait for incoming request from browser
- by default listen port 80

```
docker pull ngnix
```
```
docker run -p 8080:80 ngnix
```
- if you dont define version by default it is latest


## docker container with interactive mode

```
docker run -it ashutoshapp
```
- -it interactive terminal

## sharing images DockerHUB

```
docker login

docker push ASHUTOS-SG/app: tagname

## make sure you have image app in current directory

```
- now the image is on docker hi=ub
- anyone can downlooad it 

```
docker pull ASHUTOSH-SG/app
```

rename image
```
docker tag ashutoshapp:01 ASHUTOS-SG/app:tagname

```

## using our image remotely PULL images

 - in vm linux
```
 docker pull ASHUTOSH-SG/app:02
 ```
 - run by port binding

 ```
 docker run -p 3000:3000 ASHUTOSH-SG/app:02
 ```

## Docker Volumes

- now you have app storing information permenently

- so we have py programe to store name continuesly
```
docker run -it --rm --name pyapp c1232m3242
```
**probleam**
- now it will show enter your name 
- we will type
-  it will show
- then affter complete program automatically get stop

- due to --rm it delete container and our files also get delete

**solution** = **volume**

```
docker run -it --rm -v myvolume:/myapp/ c13123243b34
```
- -volume name of volume: working directory as mention in docker file

- je directory aapn dhili ahe ti container chya baher ahe ani aapn
- container delete kel tari directory diste

- chek your volume
```
docker volume ls
```
- cheak the details of volume
```
docker volume inspect myvolume
```
## what are bind mounts


```
try:
    with open('venv/servers.txt', 'r') as file:
        content = file.readlines()
except Exception as e:
    print(e, type(e))
else:
    for line in content:
        print(f'{line.rstrip()}')

```

- this programe read from external files
- name of the servers
save to file in container
  
- so how to update this file outside of container

```
docker run w123123
```

```
docker run --rm 09cb32923
```

- mount a perticular file or directory

```
docker run -v [absoulute path of file]:/myapp/servers.txt --rm 0ad92344345
```
- ith aap local file server.txt
- je locally ahe machine madhi
- ti /myapp/server.txt shi bind kartoy

- _[absoulute path of file]:/myapp/servers.txt

## docker ignore

- make a new file .dockerignore

- add file name 
Dockerfile
.git

## communication from/to containers

## working with api

- so our container interacting with the outer world internet api

- whatever you importing in py file
- add it in your cmd section of docker file

```
docker run a3344745
```

## commmunication container & local DB

```
import pymysql


# Function to create a connection to the MySQL database
def create_connection():
    return pymysql.connect(
        host="mysqldb",  # Your MySQL server host
        user="root",       # Your MySQL username
        password="root",  # Your MySQL password
        database="userinfo"    # Your MySQL database name
    )


# Function to create a table to store usernames if it doesn't exist
def create_table(connection):
    cursor = connection.cursor()
    cursor.execute("""
        CREATE TABLE IF NOT EXISTS usernames (
            id INT AUTO_INCREMENT PRIMARY KEY,
            name VARCHAR(255)
        )
    """)
    connection.commit()
    cursor.close()


# Function to insert a name into the database
def insert_name(connection, name):
    cursor = connection.cursor()
    cursor.execute("INSERT INTO usernames (name) VALUES (%s)", (name,))
    connection.commit()
    cursor.close()
    #Insert name into files also
    with open("servers.txt", "a") as file:
        file.write(name+"\n")


# Function to fetch all usernames from the database
def fetch_all_usernames(connection):
    cursor = connection.cursor()
    cursor.execute("SELECT name FROM usernames")
    usernames = [row[0] for row in cursor.fetchall()]
    cursor.close()
    return usernames

# Main function
def main():
    connection = create_connection()
    create_table(connection)

    while True:
        print("1. Add a name")
        print("2. Show all usernames")
        print("3. Quit")
        choice = input("Enter your choice: ")

        if choice == "1":
            name = input("Enter a name: ")
            insert_name(connection, name)
            print(f"Name '{name}' added to the database.")
        elif choice == "2":
            usernames = fetch_all_usernames(connection)
            if usernames:
                print("usernames in the database:")
                for name in usernames:
                    print(name)
            else:
                print("No usernames found in the database.")
        elif choice == "3":
            print("Goodbye!")
            break
        else:
            print("Invalid choice. Please try again.")

    connection.close()

if __name__ == "__main__":
    main()
```
for explanation of this doker file 
watch video from 2:06 

```
docker run -it --rm a64644682
```
i will occure communication error

- it will not able to comnnect with our local host


## DOKER Network

- **probleams**
we use ip to connect in this 
we have to run on ip and communicate by sub nework ip

- docker network can run 2 container in same network to communicate

```
docker network create my-net
```
- created container 

- now we assign our build container to this network
```
docker run -d --env MYSQL_PASSWORD="root" --env MYSQL_DATABASE="userinfo" --name mysqldb --network my-net mysql

```
- --network my-net 

- add another container 

```
docker run -it --rm --network my-net b3827647
```


## docker compose
- it is just configuration file to manage multiple container running on the same machine

**probleam**
- we need to add many things like root password in creating of image

### 1. **What is Docker Compose (02:30:04)**
   - **Docker Compose** is a tool that allows you to define and run multi-container Docker applications. It uses a YAML file (`docker-compose.yml`) to define services, networks, and volumes for your application.
   - You can easily manage multiple containers with a single command, making it perfect for applications that require several services (e.g., a web server, a database, etc.).

### 2. **Docker Compose for Multiple Containers (02:38:12)**
   - With Docker Compose, you can define multiple containers (services) that work together in a single `docker-compose.yml` file.
   - Each service is defined in the YAML file with its own configuration (e.g., image, environment variables, volumes, etc.).
   - Example:
     ```yaml
     version: '3'
     services:
       web:
         image: nginx
       app:
         image: myapp
     ```
   - Running `docker-compose up` will start both containers (`web` and `app`) at once.

### 3. **Docker Compose with Network (02:52:44)**
   - Docker Compose automatically creates a default network for all the services to communicate with each other. But you can also define custom networks.
   - Custom networks allow you to isolate containers from each other and give you more control over their communication.
   - Example:
     ```yaml
     version: '3'
     services:
       web:
         image: nginx
         networks:
           - frontend
       app:
         image: myapp
         networks:
           - backend

     networks:
       frontend:
       backend:
     ```
   - Here, the `web` service is connected to the `frontend` network, and the `app` service is connected to the `backend` network.

### 4. **Docker Compose with Volume (02:59:17)**
   - Volumes in Docker Compose are used to persist data across container restarts.
   - You can define volumes for services, such as a database, to store data.
   - Example:
     ```yaml
     version: '3'
     services:
       db:
         image: postgres
         volumes:
           - db-data:/var/lib/postgresql/data

     volumes:
       db-data:
     ```
   - This configuration creates a persistent volume (`db-data`) for the `db` service to store PostgreSQL data.

### 5. **Docker Compose with Port Binding (03:03:45)**
   - Docker Compose allows you to bind container ports to host machine ports, enabling access to services running inside containers.
   - Example:
     ```yaml
     version: '3'
     services:
       web:
         image: nginx
         ports:
           - "8080:80"
     ```
   - This binds port `80` inside the `web` container to port `8080` on the host machine. Now, you can access the web service by navigating to `http://localhost:8080`.

### Summary of Docker Compose Features:

- **Multiple containers**: Easily define and manage several services (containers) in one file.
- **Networking**: Services can communicate using default or custom networks.
- **Volumes**: Persist data for services (e.g., databases) using Docker volumes.
- **Port binding**: Map ports from containers to the host to access services.

With Docker Compose, you can define complex multi-container applications in a simple and repeatable manner.





## advance topic


## communication of multiple contINER


```
docker run -d --env MYSQL_PASSWORD="root" --env MYSQL_DATABASE="userinfo" --name mysqldb mysql
```
now my sql container is running

- now check network of your container

cheack ip

```
docker inspect mysqldb 
```
add ip in python file hosts =


-- we need authentication
in python file

with
- RUN pip install pymysql

add
- RUN pip install cryptography

```
docker build .
```

```
docker run -it --rm aaf8465584651
```