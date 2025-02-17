

---

### 1. **EC2 Instance**  
#### Definition:  
Amazon EC2 (Elastic Compute Cloud) is a scalable compute service that allows users to run virtual machines in the cloud. It provides resizable compute capacity and allows you to run applications and services on-demand.

#### How to Set Up an EC2 Instance:
1. **Sign in** to AWS Management Console.
2. Navigate to **EC2 Dashboard**.
3. Click on **Launch Instance**.
4. Choose an **AMI** (Amazon Machine Image), such as Amazon Linux or Ubuntu.
5. Select the **instance type** (e.g., t2.micro).
6. Configure **instance details** (network, IAM role).
7. Add **storage** (EBS volume).
8. Add **tags** (for identification).
9. Configure **security group** (set inbound/outbound rules).
10. **Review** and click **Launch**.
11. Create or choose an existing **key pair** for SSH access.

---

### EC2 Interview Questions

1. **What is an EC2 instance?**
   - EC2 is a virtual server in the cloud where you can run applications and services.

2. **How does EC2 billing work?**
   - EC2 is billed based on the instance type, hours of usage, and additional services like EBS storage or data transfer.

3. **Explain the different EC2 instance types.**
   - EC2 offers general-purpose, compute-optimized, memory-optimized, storage-optimized, and GPU instances.

4. **What are security groups in EC2?**
   - Security groups act as virtual firewalls for EC2 instances, controlling inbound and outbound traffic.

5. **What is an Elastic IP (EIP)?**
   - An Elastic IP is a static IP address that can be associated with EC2 instances.

6. **What is the difference between EC2 and Lambda?**
   - EC2 is a full virtual server, while Lambda is a serverless compute service.

7. **Can you explain EC2 auto-scaling?**
   - EC2 auto-scaling automatically adjusts the number of EC2 instances to handle traffic changes.

8. **How do you stop and start an EC2 instance?**
   - You can stop and start EC2 instances from the EC2 dashboard in the AWS Management Console.

9. **What is an AMI in EC2?**
   - AMI (Amazon Machine Image) is a template that includes the OS and software required to launch an EC2 instance.

10. **What is the difference between Instance store and EBS?**
   - Instance store is temporary storage tied to the lifecycle of an instance, while EBS is persistent storage.

11. **How can you monitor EC2 instances?**
   - You can use Amazon CloudWatch to monitor EC2 instances, check metrics like CPU utilization, and set alarms.

12. **What are the different types of storage available for EC2?**
   - EC2 supports instance store (ephemeral) and Elastic Block Store (EBS) volumes.

13. **Explain the concept of EC2 placement groups.**
   - Placement groups allow you to control the placement of EC2 instances on the underlying hardware.

14. **How do you manage EC2 instance costs?**
   - Use AWS EC2 pricing options like On-Demand, Reserved, or Spot instances to optimize costs.

15. **What is a key pair in EC2?**
   - Key pairs are used for SSH access to EC2 instances.

16. **Explain the use of AWS Systems Manager with EC2.**
   - AWS Systems Manager allows you to automate EC2 instance management tasks such as patching and configuration.

17. **How do you enable encryption for EC2 instance storage?**
   - You can enable encryption at the time of creating an EBS volume or enable encryption for existing EBS volumes.

18. **What is the difference between stopping and terminating an EC2 instance?**
   - Stopping an instance keeps the data and the EBS volume intact, while terminating deletes the instance and its associated data.

19. **How do you migrate an on-premise server to EC2?**
   - You can use the AWS Server Migration Service (SMS) to migrate on-premise servers to EC2.

20. **Explain the EC2 instance lifecycle.**
   - An EC2 instance goes through several states: Pending, Running, Stopped, Terminated.

---

### 2. **VPC (Virtual Private Cloud)**  
#### Definition:  
A VPC is a virtual network dedicated to your AWS account, allowing you to define your own IP address range, create subnets, and configure routing and security.

#### How to Set Up a VPC:
1. **Sign in** to AWS Console.
2. Navigate to **VPC Dashboard**.
3. Click **Create VPC**.
4. Enter a **CIDR block** (e.g., 10.0.0.0/16).
5. Create **subnets** (private, public).
6. Set up **internet gateway** for public subnet access.
7. Configure **route tables** for traffic routing.
8. Set up **security groups** and **NACLs** for access control.

---

### VPC Interview Questions

1. **What is a VPC in AWS?**
   - A VPC is a virtual network where you can launch AWS resources in a logically isolated section of the AWS cloud.

2. **How does VPC differ from a traditional network?**
   - VPC allows users to define a custom network topology in the cloud, unlike traditional networks.

3. **What are the components of a VPC?**
   - Components include subnets, route tables, security groups, network ACLs, internet gateway, and more.

4. **What is the purpose of an Internet Gateway in a VPC?**
   - It allows communication between instances in a VPC and the internet.

5. **What is a subnet in VPC?**
   - A subnet is a range of IP addresses in your VPC for grouping resources based on security or operational needs.

6. **What is a route table?**
   - A route table controls the routing of traffic between subnets and internet gateways.

7. **What is the difference between a public and private subnet in VPC?**
   - Public subnets are accessible from the internet, while private subnets are not directly accessible.

8. **What is NAT Gateway?**
   - A NAT gateway allows instances in a private subnet to connect to the internet without exposing them directly.

9. **What is the role of Network ACL in VPC?**
   - Network ACLs control traffic flow at the subnet level, providing an additional layer of security.

10. **How can you secure a VPC?**
   - You can use security groups, NACLs, VPN connections, and private subnets to secure VPC resources.

11. **What is VPC Peering?**
   - VPC Peering connects two VPCs in the same region or different regions, allowing them to communicate privately.

12. **What is Direct Connect in VPC?**
   - AWS Direct Connect establishes a dedicated network connection between your premises and AWS.

13. **Explain the concept of VPC Flow Logs.**
   - VPC Flow Logs capture information about IP traffic in your VPC for monitoring and troubleshooting.

14. **What is the difference between a VPN connection and Direct Connect?**
   - A VPN connection is a secure tunnel over the internet, while Direct Connect is a private, dedicated network connection.

15. **How do you use VPC for high availability?**
   - You can deploy resources across multiple availability zones for fault tolerance.

16. **What is a VPC endpoint?**
   - VPC endpoints enable private connections to AWS services without using the public internet.

17. **How do you assign Elastic IPs to instances in a VPC?**
   - You can associate an Elastic IP with an EC2 instance through the EC2 dashboard.

18. **How do you troubleshoot network issues in VPC?**
   - Use VPC flow logs, security group and NACL checks, and traceroute to troubleshoot.

19. **Can you have multiple VPCs in an AWS account?**
   - Yes, you can create multiple VPCs in a single AWS account.

20. **What is Transit Gateway in VPC?**
   - A Transit Gateway is a hub that enables the connection of multiple VPCs and on-premise networks.

---

### 3. **S3 (Simple Storage Service)**  
#### Definition:  
Amazon S3 is an object storage service that provides scalable, durable, and low-latency storage. It's ideal for storing and retrieving any amount of data, such as files, images, backups, and data lakes.

#### How to Set Up S3:
1. **Sign in** to the AWS Management Console.
2. Navigate to the **S3 dashboard**.
3. Click **Create Bucket**.
4. Enter a unique **bucket name** and select a region.
5. Set the **bucket configuration** (e.g., versioning, logging).
6. Configure **permissions** (public or private).
7. Review and **create** the bucket.

---

### S3 Interview Questions

1. **What is Amazon S3?**
   - Amazon S3 is a scalable object storage service that allows users to store and retrieve any amount of data at any time.

2. **What are the storage classes in S3?**
   - S3 offers multiple storage classes such as Standard, Intelligent-Tiering, One Zone-IA, Glacier, and Glacier Deep Archive.

3. **Explain the difference between objects and files in S3.**
   - Objects are the fundamental entities in S3, consisting of data, metadata, and a unique identifier. Files are the data that you store in S3 as objects.

4. **What is S3 Versioning?**
   - S3 Versioning enables you to keep multiple versions of an object in a bucket, helping protect against accidental deletion or overwrites.

5. **What is an S3 Bucket Policy?**
   - A bucket policy is a resource-based policy that allows you to manage access to your S3 bucket and objects.

6. **How do you secure data in S3?**
   - Use bucket policies, IAM policies, encryption (server-side and client-side), and access control lists (ACLs).

7. **What is the difference between S3 and EBS?**
   - S3 is object storage designed for storing large amounts of unstructured data, while EBS is block storage used with EC2 instances.

8. **What is S3 Transfer Acceleration?**
   - S3 Transfer Acceleration enables faster data transfer by routing your traffic through Amazon CloudFront’s globally distributed edge locations.

9. **How do you set up an S3 lifecycle policy?**
   - You can set lifecycle policies to automatically transition objects to different storage classes or delete objects after a certain period.

10. **What is the maximum object size that can be stored in S3?**
    - The maximum size for an individual object in S3 is 5TB.

11. **What are S3 Access Points?**
    - S3 Access Points provide a simple way to manage access to shared datasets for multiple applications or users.

12. **How does S3 ensure durability of data?**
    - S3 provides 99.999999999% durability by replicating data across multiple facilities.

13. **What is S3 Glacier?**
    - S3 Glacier is a low-cost storage service for archival data that provides retrieval times ranging from minutes to hours.

14. **What is the S3 Cross-Region Replication?**
    - Cross-Region Replication automatically replicates objects from one S3 bucket to another in different AWS regions.

15. **How do you manage access to S3 buckets?**
    - Use IAM policies, bucket policies, and ACLs to manage access.

16. **What is S3 Select?**
    - S3 Select allows you to retrieve a subset of data from an object using SQL-like queries.

17. **What is an S3 Object Lock?**
    - S3 Object Lock prevents objects from being deleted or overwritten for a fixed amount of time or indefinitely.

18. **How can you track S3 access?**
    - You can use S3 server access logging and CloudTrail to track access to your S3 bucket.

19. **What is a pre-signed URL in S3?**
    - A pre-signed URL allows temporary access to an object in S3 without requiring AWS credentials.

20. **How do you migrate data to S3?**
    - Use AWS CLI, AWS DataSync, or AWS Snowball to migrate large datasets to S3.

---

### 4. **EBS (Elastic Block Store)**  
#### Definition:  
Amazon EBS provides persistent block-level storage volumes for EC2 instances. These volumes can be used for storing data, operating systems, applications, and databases.

#### How to Set Up EBS:
1. **Sign in** to AWS Management Console.
2. Navigate to the **EC2 Dashboard** and select **Volumes**.
3. Click **Create Volume**.
4. Choose the **volume type** (e.g., SSD or HDD).
5. Select the **size** and **availability zone**.
6. Attach the volume to an EC2 instance.

---

### EBS Interview Questions

1. **What is EBS in AWS?**
   - Amazon EBS is a persistent block-level storage service used for storing data and applications attached to EC2 instances.

2. **What are the types of EBS volumes?**
   - EBS offers different volume types such as General Purpose (SSD), Provisioned IOPS (SSD), and Cold HDD.

3. **What is the difference between EBS and S3?**
   - EBS is block storage for EC2 instances, while S3 is object storage for unstructured data.

4. **How do you attach an EBS volume to an EC2 instance?**
   - You can attach an EBS volume via the EC2 dashboard or using the AWS CLI by specifying the volume ID and instance ID.

5. **What is the maximum size of an EBS volume?**
   - The maximum size of an EBS volume is 16TB.

6. **What is the difference between snapshot and backup in EBS?**
   - Snapshots are point-in-time backups of EBS volumes stored in S3, while backups typically refer to storing EBS data elsewhere.

7. **How do you create a snapshot in EBS?**
   - You can create a snapshot from the EC2 dashboard by selecting the EBS volume and choosing "Create Snapshot".

8. **Can you resize an EBS volume?**
   - Yes, you can resize an EBS volume, and the new size takes effect immediately after modifying the volume.

9. **What is IOPS in EBS?**
   - IOPS (Input/Output Operations Per Second) refers to the number of read and write operations EBS can perform per second.

10. **How do you encrypt EBS volumes?**
    - You can enable encryption when creating an EBS volume or when creating a snapshot.

11. **How do you back up an EBS volume?**
    - Use EBS snapshots to back up the data to S3.

12. **What is an EBS volume's lifecycle?**
    - EBS volumes have states such as creating, available, in-use, and deleting.

13. **What is the difference between an EBS volume and an instance store?**
    - EBS volumes are persistent and data is retained when the instance is stopped, while instance store is temporary storage.

14. **How do you increase the performance of EBS?**
    - You can increase performance by choosing Provisioned IOPS volumes or by using multiple volumes in RAID configurations.

15. **What is Elastic Volumes in EBS?**
    - Elastic Volumes allow you to dynamically adjust the size, IOPS, and type of your EBS volumes without stopping the instance.

16. **What is an EBS snapshot?**
    - An EBS snapshot is a point-in-time backup of an EBS volume that is stored in S3.

17. **How do you monitor EBS performance?**
    - You can monitor EBS performance using Amazon CloudWatch metrics such as read/write operations, latency, and throughput.

18. **How can you automate snapshot creation in EBS?**
    - You can use AWS Lambda or CloudWatch Events to automate snapshot creation.

19. **What is the importance of EBS in high-availability architectures?**
    - EBS provides persistent storage that can be replicated across availability zones for high availability.

20. **What is a multi-attach feature in EBS?**
    - EBS Multi-Attach allows an EBS volume to be attached to multiple EC2 instances within the same availability zone.

---

### 5. **Lambda**  
#### Definition:  
AWS Lambda is a serverless compute service that automatically runs code in response to events, without provisioning or managing servers.

#### How to Set Up Lambda:
1. **Sign in** to the AWS Management Console.
2. Navigate to the **Lambda dashboard**.
3. Click **Create function**.
4. Select **Author from scratch** and configure the runtime (e.g., Node.js, Python).
5. Upload your **function code** or use inline editor.
6. Set permissions by creating an **IAM role**.
7. Define the event source (e.g., S3 trigger).
8. Review and **Create function**.

---

### Lambda Interview Questions

1. **What is AWS Lambda?**
   - AWS Lambda is a serverless compute service that runs code in response to events, without needing to provision or manage servers.

2. **How does AWS Lambda work?**
   - Lambda functions are triggered by events such as changes to data in S3 or DynamoDB, or HTTP requests via API Gateway.

3. **What are the benefits of using AWS Lambda?**
   - Benefits include reduced operational overhead, automatic scaling, and cost savings as you only pay for the execution time.

4. **What is a Lambda trigger?**
   - A trigger is an event that invokes the Lambda function, such as S3 uploads, DynamoDB changes, or API Gateway calls.

5. **How can you secure AWS Lambda functions?**
   - Use IAM roles and policies to control access to AWS services and resources from Lambda functions.

6. **What are the limits of AWS Lambda?**
   - AWS Lambda has a maximum execution timeout of 15 minutes, a memory limit of 3,008 MB, and a maximum payload size of 6 MB for synchronous invocations.

7. **How do you debug AWS Lambda functions?**
   - You can use Amazon CloudWatch logs to debug and monitor Lambda function execution.

8. **What is the difference between Lambda and EC2?**
   - Lambda is serverless and runs code in response to events, while EC2 provides virtual machines where you run applications.

9. **Can AWS Lambda be used for scheduled tasks?**
   - Yes, you can use Amazon CloudWatch Events to schedule Lambda function invocations at regular intervals.

10. **How do you monitor Lambda?**
    - AWS CloudWatch can be used to monitor the execution of Lambda functions with metrics and logs.

11. **What is the execution role in AWS Lambda?**
    - The execution role is an IAM role that grants AWS Lambda permissions to access other AWS services on your behalf.

12. **How do you handle Lambda function errors?**
    - Errors can be handled by using dead-letter queues, retries, or using Amazon CloudWatch to monitor and alert on failures.

13. **What is a Lambda layer?**
    - A Lambda layer is a ZIP archive that contains libraries or other function dependencies that you can reuse across multiple functions.

14. **How do you invoke a Lambda function synchronously?**
    - You can invoke a Lambda function synchronously by using the `Invoke` API or through an AWS service that triggers Lambda synchronously.

15. **What is the Lambda cold start?**
    - Cold start occurs when a Lambda function is invoked after being idle, causing a slight delay as the runtime initializes.

16. **Can Lambda functions be written in multiple programming languages?**
    - Yes, Lambda supports various runtimes such as Node.js, Python, Java, Go, and more.

17. **What is AWS Lambda concurrency?**
    - Concurrency refers to the number of Lambda function executions running simultaneously. You can set a concurrency limit.

18. **How do you scale Lambda functions?**
    - Lambda scales automatically based on incoming events, with no need to manage infrastructure.

19. **How can you handle large payloads in Lambda?**
    - You can store large payloads in S3 and pass a reference (S3 URI) to the Lambda function.

20. **What is Lambda@Edge?**
    - Lambda@Edge allows you to run Lambda functions closer to users by executing them at CloudFront edge locations.

---

Here are the answers to your questions:

### 1. Difference Between S3 and EBS:
- **Amazon S3 (Simple Storage Service)** is an object storage service used for storing and retrieving any amount of data. It is designed for scalability and durability. It is ideal for storing unstructured data like images, videos, backups, and logs.
- **Amazon EBS (Elastic Block Store)** provides persistent block storage volumes for EC2 instances. It is ideal for applications that require a file system and can be mounted to EC2 instances.

### 2. When to Use S3 and EBS:
- **Use S3 when**:  
  - You need scalable, durable, and low-cost storage for data such as backups, media files, or static web content.
  - You require easy data accessibility via the internet.
  - You are storing large amounts of unstructured data.
- **Use EBS when**:
  - You need persistent block-level storage that is tied to an EC2 instance.
  - You are running databases, virtual machines, or applications requiring file systems like ext4, NTFS, etc.
  - You need high-performance storage for I/O-intensive applications.

### 3. Why We Need S3 and EBS When There is Built-in Storage in EC2 Instance:
- **EC2 instance storage** (local storage) is ephemeral and is lost when the instance is stopped or terminated. It is not persistent across reboots or instance failures.
- **S3** provides highly durable, scalable object storage that is not tied to a specific EC2 instance, making it ideal for backups, web content, and large data storage.
- **EBS** provides persistent storage that survives instance reboots, making it suitable for databases and applications that require a file system and data persistence.

### 4. VPC: How to Provide Internet Access to a Private Subnet:
To provide internet access to instances in a private subnet, you can configure a **NAT Gateway** or a **NAT Instance** in a public subnet. Here's how:
- **NAT Gateway/Instance**: Create a NAT Gateway or a NAT Instance in a public subnet with a route to the internet via an Internet Gateway. Private subnets route their outbound traffic to the NAT Gateway for internet access.
- **Route Table**: Update the route table of the private subnet to route traffic to the NAT Gateway.

### 5. Difference Between PEM and PPK Key and When to Generate Each:
- **PEM (Privacy-Enhanced Mail)**: This is the default format for SSH private keys used by AWS EC2 instances. It is used in Linux and macOS for SSH access.
- **PPK (PuTTY Private Key)**: This is the format used by PuTTY, a Windows SSH client. You can convert PEM keys to PPK format using PuTTYgen.
- **When to generate which**:  
  - **PEM**: Use this for connecting to EC2 instances from a Linux or macOS system using SSH.
  - **PPK**: Convert PEM to PPK and use it for connecting to EC2 instances from Windows using PuTTY.

### 6. How to Access Windows and Linux EC2 Locally and Send Files:
- **Linux EC2 Instance**:  
  - Use an SSH client (e.g., `ssh -i key.pem ec2-user@<public-ip>`) to access the EC2 instance.
  - To send files, use `scp` (e.g., `scp -i key.pem file.txt ec2-user@<public-ip>:<destination-path>`).
- **Windows EC2 Instance**:  
  - Use Remote Desktop Protocol (RDP) with the Windows Administrator credentials. Ensure you use the `.pem` key to decrypt the administrator password from the EC2 console.
  - To send files, you can use RDP to copy-paste or set up a shared drive.

### 7. Why EBS is Used in Most HPC Deployment:
- **EBS is used in most HPC deployments** because:
  - It provides **persistent storage** for large datasets and applications, ensuring data is not lost after instance failures or reboots.
  - It supports high-performance block storage with low latency and high throughput, which is crucial for HPC workloads that require fast data access and manipulation.
  - It allows for flexible **scaling** and provides the ability to attach multiple EBS volumes to instances for high I/O performance.
