### **Session 6-7 Overview**  

#### **1. Process Automation (DevOps):**  
- DevOps automates software development, deployment, and operations.  
- Focuses on collaboration for faster delivery, better quality, and scalability.  

#### **2. Version Control with Git:**  
- Tracks and manages code changes over time.  
- Enables teamwork on the same project while maintaining history.  

#### **3. Branching, Merging, and Workflows in Git:**  
- **Branching:** Work on separate features/tasks independently.  
- **Merging:** Combine branches back into the main branch.  
- **Workflows:** Strategies like Git Flow and Feature Branch Workflow for collaboration.  

---

### **Assignments**  
1. Install Git, initialize repositories, and connect to remote ones (e.g., GitHub).  
2. Practice branching, merging, resolving conflicts, and managing histories.  
3. Learn stashing, rebasing, reverting, and resetting to handle changes effectively.  

---

### **20 Basic Git Commands**  

#### **General Commands**  
1. `git init`: Start a new repository.  
2. `git clone <URL>`: Copy a remote repo locally.  
3. `git status`: View current repo status.  
4. `git add <file>`: Stage changes.  
5. `git commit -m "message"`: Save changes.  
6. `git log`: View commit history.  
7. `git config --global user.name/email`: Set username/email.  
8. `git diff`: Show changes.  
9. `git remote add origin <URL>`: Link local repo to remote.  
10. `git push origin <branch>`: Upload local changes to remote.  

#### **Branching & Merging**  
11. `git branch`: List or create branches.  
12. `git checkout <branch>`: Switch branches.  
13. `git merge <branch>`: Merge a branch into the current one.  
14. `git pull`: Fetch and merge remote changes.  

#### **Advanced**  
15. `git stash`: Save uncommitted changes.  
16. `git stash pop`: Apply and remove stashed changes.  
17. `git rebase <branch>`: Reapply commits on another branch.  
18. `git revert <commit>`: Undo changes by creating a new commit.  
19. `git reset <commit>`: Move branch pointer to a specific commit.  
20. `git log --oneline`: View compact commit history.  

---

### **Session 8-11 Overview**

#### **1. Docker Basics**  
- **What is Docker?**  
  A platform to package applications and dependencies in portable containers.  
- **Why Docker?**  
  - Simplifies deployment.  
  - Ensures consistency across environments.  
  - Efficient compared to VMs.  

#### **2. Docker Images & Containers**  
- **Image:** Blueprint of an app with all dependencies.  
- **Container:** A running instance of an image, lightweight and isolated.  

#### **3. Dockerfile**  
- A script to build custom images.  
  ```dockerfile
  FROM python:3.9  
  WORKDIR /app  
  COPY . /app  
  RUN pip install -r requirements.txt  
  CMD ["python", "app.py"]  
  ```  

#### **4. Networking**  
- Connects containers to each other or the host. Types:  
  - **Bridge:** Isolated (default).  
  - **Host:** Shares host’s network.  
  - **Overlay:** Connects across multiple hosts.  

#### **5. Volumes**  
- Stores persistent data outside containers.  
  ```bash
  docker run -v my_volume:/data my_image  
  ```  

#### **6. Docker Compose**  
- Manages multi-container apps with YAML:  
  ```yaml
  version: '3'  
  services:  
    web:  
      image: nginx  
      ports:  
        - "80:80"  
    db:  
      image: mysql:5.7  
      environment:  
        MYSQL_ROOT_PASSWORD: password  
  ```  

---

### **20 Key Docker Commands**  

#### **Basic Commands**  
1. `docker --version`: Check Docker version.  
2. `docker images`: List images.  
3. `docker pull <image>`: Download an image.  
4. `docker ps`: Show running containers.  
5. `docker run <image>`: Start a container.  
6. `docker stop <container_id>`: Stop a container.  
7. `docker rm <container_id>`: Remove a container.  
8. `docker rmi <image_id>`: Delete an image.  
9. `docker exec -it <container_id> bash`: Access a container shell.  

#### **Advanced Commands**  
10. `docker build -t <name> .`: Build an image from a Dockerfile.  
11. `docker logs <container_id>`: Show container logs.  
12. `docker network ls`: List networks.  
13. `docker volume ls`: List volumes.  
14. `docker-compose up`: Start services.  
15. `docker-compose down`: Stop services.  
16. `docker inspect <container_id>`: Detailed container info.  
17. `docker stats`: Show real-time container stats.  

### **Session 12-14: Simplified Overview**

#### **1. Container Orchestration**  
- **Definition:** Manages multiple containers for deployment, scaling, and availability.  
- **Why Needed?** Automates large-scale apps, ensures load balancing, and fault tolerance.  
- **Examples:** Kubernetes, Docker Swarm.  

---

#### **2. Kubernetes Basics**  
- **What is Kubernetes?**  
  An open-source platform to manage containerized applications.  
- **Architecture Overview:**  
  - **Master Node:** Handles cluster management (API Server, Scheduler, Controller Manager, etcd).  
  - **Worker Node:** Runs containers (Kubelet, Kube-Proxy, Container Runtime).  

---

#### **3. Kubernetes Objects**  
- **Pod:** Smallest deployable unit, encapsulates containers.  
- **ReplicaSet:** Ensures a specified number of pod replicas.  
- **Deployment:** Manages ReplicaSets and enables rolling updates.  
- **Service:** Exposes pods for communication (e.g., ClusterIP, NodePort).  

---

#### **4. YAML Configuration in Kubernetes**  
- YAML files are used to define objects.  
- **Example Deployment YAML:**  
  ```yaml
  apiVersion: apps/v1
  kind: Deployment
  metadata:
    name: example-deployment
  spec:
    replicas: 3
    selector:
      matchLabels:
        app: my-app
    template:
      metadata:
        labels:
          app: my-app
      spec:
        containers:
        - name: nginx
          image: nginx
  ```  

---

#### **5. 20 Essential `kubectl` Commands**  
1. **`kubectl version`**: Check Kubernetes version.  
2. **`kubectl cluster-info`**: View cluster information.  
3. **`kubectl get nodes`**: List all cluster nodes.  
4. **`kubectl get pods`**: List all pods in the namespace.  
5. **`kubectl describe pod <pod_name>`**: Get detailed pod information.  
6. **`kubectl logs <pod_name>`**: View pod logs.  
7. **`kubectl delete pod <pod_name>`**: Delete a specific pod.  
8. **`kubectl get services`**: List all services.  
9. **`kubectl delete service <service_name>`**: Remove a service.  
10. **`kubectl exec -it <pod_name> -- /bin/bash`**: Access the pod shell.  
11. **`kubectl create -f <file.yaml>`**: Create resources from a YAML file.  
12. **`kubectl apply -f <file.yaml>`**: Apply or update a configuration.  
13. **`kubectl delete -f <file.yaml>`**: Delete resources defined in a YAML file.  
14. **`kubectl scale deployment <name> --replicas=<n>`**: Scale a deployment.  
15. **`kubectl rollout status deployment <name>`**: Check rollout status.  
16. **`kubectl rollout undo deployment <name>`**: Roll back a deployment.  
17. **`kubectl get events`**: List cluster events.  
18. **`kubectl top nodes`**: View resource usage of nodes.  
19. **`kubectl top pods`**: View resource usage of pods.  
20. **`kubectl config view`**: Show Kubernetes configuration.  

---


### **Session 15-18 Overview**

#### **1. Introduction to Jenkins**
- **What is Jenkins?**  
  Jenkins is an open-source automation server for continuous integration and delivery (CI/CD). It automates building, testing, and deploying software.
- **Why use Jenkins?**  
  It speeds up development by integrating code frequently, tracking build failures, and managing pipelines.
- **Key Features:**  
  Extensible via plugins, supports distributed builds, and has a web-based interface.

---

#### **2. Installing Jenkins**
- **Prerequisites:**  
  - Java JDK 8/11.
  - Supported OS: Windows, Linux, macOS.
- **Installation Steps (Linux/Ubuntu):**  
  1. Update system: `sudo apt update && sudo apt upgrade -y`
  2. Install Java: `sudo apt install openjdk-11-jdk -y`
  3. Add Jenkins repository & install:  
     ```bash
     curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
     echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
     sudo apt update && sudo apt install jenkins -y
     ```
  4. Start Jenkins: `sudo systemctl start jenkins`
  5. Access at `http://<your-ip>:8080`.

---

#### **3. Creating Simple Jobs**
- **Steps:**
  1. Go to Jenkins → "New Item" → Choose **Freestyle Project** → Click **OK**.
  2. Configure job (e.g., Git repository URL, build commands).
  3. Save and click **Build Now**.

---

#### **4. Jenkins ‘Hello World’**
- **Pipeline Script Example:**  
  ```groovy
  pipeline {
      agent any
      stages {
          stage('Hello') {
              steps {
                  echo 'Hello World!'
              }
          }
      }
  }
  ```

---

#### **5. GitHub and Jenkins Integration**
- **Steps:**
  1. Install **Git plugin** in Jenkins.
  2. Add GitHub credentials.
  3. Configure job with GitHub repo URL.
  4. Set up GitHub webhook to trigger builds.
  5. Enable build trigger for GitHub changes.

---

#### **6. Docker and Jenkins Integration**
- **Why Docker with Jenkins?**  
  To build and deploy apps in containers, ensuring consistent environments.
- **Steps:**
  1. Install Docker: `sudo apt install docker.io -y`
  2. Add Jenkins user to Docker group: `sudo usermod -aG docker jenkins`
  3. Install Docker Pipeline plugin.
  4. Use Docker in a Jenkins pipeline:
     ```groovy
     pipeline {
         agent any
         stages {
             stage('Run Docker') {
                 steps {
                     script {
                         docker.image('nginx:latest').run()
                     }
                 }
             }
         }
     }
     ```

---

### **20 Jenkins Commands**

#### **CLI Commands**
1. `java -jar jenkins.war` - Starts Jenkins manually.
2. `sudo systemctl start jenkins` - Starts Jenkins as a service.
3. `sudo systemctl stop jenkins` - Stops Jenkins service.
4. `sudo systemctl restart jenkins` - Restarts Jenkins.
5. `sudo cat /var/lib/jenkins/secrets/initialAdminPassword` - Retrieves admin password.

#### **Pipeline Commands**
6. `echo 'Message'` - Prints a message.
7. `sh 'command'` - Runs shell commands.
8. `checkout scm` - Checks out the source code.
9. `build job: 'JobName'` - Triggers another job.
10. `input message: 'Confirm?'` - Pauses the pipeline.

#### **Job Management Commands**
11. `curl -X POST http://<jenkins-url>/job/<job-name>/build` - Triggers job remotely.
12. `curl -X GET http://<jenkins-url>/job/<job-name>/api/json` - Retrieves job details.
13. `curl -X DELETE http://<jenkins-url>/job/<job-name>` - Deletes job.
14. `wget http://<jenkins-url>/jnlpJars/jenkins-cli.jar` - Downloads CLI.
15. `java -jar jenkins-cli.jar -s <jenkins-url> help` - Lists CLI commands.

#### **Docker Integration Commands**
16. `docker ps` - Lists running containers.
17. `docker build -t <image-name> .` - Builds Docker image.
18. `docker run <image-name>` - Runs container.

#### **Advanced Commands**
19. `kubectl run jenkins-agent` - Deploys Jenkins agent in Kubernetes.
20. `pipeline { ... }` - Starts a pipeline script.
