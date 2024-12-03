# 📝Cloud Computing

- [How Clod Computing Works?](#how-clod-computing-works)
- [Problems solved by the Cloud](#problems-solved-by-the-cloud)
- [The Five Characteristics of Cloud Computing](#the-five-characteristics-of-cloud-computing)
- [Types of Cloud Computing](#types-of-cloud-computing)
- [Types of Services on Cloud Computing](#types-of-services-on-cloud-computing)
- [Six Advantages of Cloud Computing](#six-advantages-of-cloud-computing)
- [Benefits of Cloud Computing](#benefits-of-cloud-computing)

### How Clod Computing Works?

- It works On Demand, the user/company pays only for what is using.
- Instant services and provisioning
- Scalability

## Problems solved by the Cloud

- Flexibility
- Cost-Effectiveness
- Scalability
- Elasticity
- High-availability and fault-tolerance
- Agility

## The Five Characteristics of Cloud Computing

- **On-demand self service**: Users can provision resources and use them without human interaction from the service providers. Everything is provisioned automatically.

- **Broad Network Access**: The resources are available over the network and can be accessible by others platforms inside the cloud or between customer services.

- **Multi-tenancy and Resource Pooling**: Multiple customers can share the same physical infrastructure or application with security and data privacy. In cloud commonly the same hardware is used to Multiple customers, and the data keeps totally safe and private.

- **Rapid elasticity and Scalability**: Automatically and quickly acquire and dispose resources when needed. Quickly and easily scale based on demand.

- **Measured Services**: Usage is measured, users pay correctly for what they have used (seconds, hours, days, etc.)

## Types of Cloud Computing

**Private**

- Closed/Not open for the public
- To provide services/infra to a specific organization
- Known Provider: Rackspace

**Public**

- Deliver stored apps on the internet for open access
- Provides all the services to deploys apps
- Known Provider: AWS, Azure, GCP

**Hybrid**

- Keep some servers on premises and extend some capabilities to the Cloud
- Can keep sensitive data on the On Premise server (locally) and the others services on cloud.

## Types of Services on Cloud Computing

**Infrastructure as a Service (IaaS)**

- Provide building tools for cloud IT accessible from network
- Provides network, computers, data storage and processing quickly
- Flexibility
- Can easily be parallelized with on-premises

**Platform as a Service (PaaS)**

- Environment to develop and deploy apps
- Focus on Deployment and App management
- Remove the needs of infra management
- The platform provides the infra and manages it to run the application

**Software as a Service (SaaS)**

- Completed product that is run and managed by the service provider
- Made to final users such as office 365

## Six Advantages of Cloud Computing

- Trade capital expense (CAPEX) for operational expense (OPEX) (or variable expenses)
- Benefit from massive economies of scale
- Stop guessing capacity
- Increase speed and agility
- Stop spending money running and maintaining data centers
- Go global in minutes

## Benefits of Cloud Computing

Cloud computing is the on-demand delivery of IT resources over the Internet with pay-as-you-go pricing. Instead of buying, owning, and maintaining physical data centers and servers, you can access technology services, such as computing power, storage, and databases, on an as-needed basis from a cloud provider like Amazon Web Services (AWS).

**Agility** - Agility refers to the ability of the cloud to give you easy access to a broad range of technologies so that you can innovate faster and build nearly anything that you can imagine. You can quickly spin up resources as you need them – from infrastructure services, such as compute, storage, and databases, to Internet of Things, machine learning, data lakes and analytics, and much more.

**Elasticity** - With cloud computing elasticity, you don’t have to over-provision resources upfront to handle peak levels of business activity in the future. Instead, you provision the number of resources that you actually need. You can scale these resources up or down instantly to grow and shrink capacity as your business needs change.

**Cost savings**- The cloud allows you to trade capital expenses (such as data centers and physical servers) for variable expenses, and only pay for IT as you consume it. Plus, the variable expenses are much lower than what you would pay to do it yourself because of the economies of scale.

**Ability to deploy globally in minutes** - With the cloud, you can expand to new geographic regions and deploy globally in minutes. For example, AWS has infrastructure all over the world, so you can deploy your application in multiple physical locations with just a few clicks. Putting applications in closer proximity to end users reduces latency and improves their experience.

[References](https://aws.amazon.com/what-is-cloud-computing/)


# 📝How AWS Works

AWS is a cloud computing provider. It has services to multiple demands of any size.

### AWS Global Infrastructure

AWS has a global infra that can attend customers in multiple locations. The infra is composed by:

##### AWS Regions

- A regions is a cluster of data centers.
- They are all around the world and have names (us-east-1, sa-east-1)

##### AWS Availability Zones (AZ's)

- Availability Zones (AZ) give customers the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center.
- Each region has many AZ. Usually 3, min 2 max 6
- Each availability zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity
- They’re separate from each other, so that they’re isolated from disasters
- They’re connected with high bandwidth, ultra-low latency networking
- All AZs together will form a **region**
- All traffic between AZs is encrypted
  > Each AWS Region consists of multiple, isolated and physically separated availability zones within a geographical area.

##### AWS Points of Presence/Edge Locations

- Deliver customer’s content through a worldwide network of Points of Presence (PoP) locations, which consists of Edge Locations and Regional Edge Cache servers.
- AWS has 216 Points of Presence (205 Edge Locations & 11 Regional Caches) in 84 cities across 42 countries
- Content is delivered to end users with lower latency

##### AWS Data Centers

- Amazon Data Centers where they have the physical computers

##### AWS Local Zones

- AWS Local Zones are a new type of AWS infrastructure deployment that places AWS compute, storage, database, and other select services closer to large population, industry, and IT centers.

### AWS Use Cases

- Enterprise IT, Backup & Storage, Big Data analytics
- Website hosting, Mobile & Social Apps
- Gaming

### AWS Services

AWS Has a large services portfolio. Some of them are available Globally other are scoped by a Region.

![AWS Global vs Regional vs AZ](https://jayendrapatil.com/wp-content/uploads/2016/03/AWS-Global-vs-Regional-vs-AZs.png)

##### Global

- IAM (Access Management)
- Route 53 (DNS Service)
- CloudFront (CDN)
- SES (Simple Email Service)
- WAF (Web Application Firewall)

##### Region Scoped

- Amazon EC2 (Infrastructure as a Service - IaaS)
- AMI (Amazon Machine Image)
- Elastic Beanstalk (Platform as a Service - PaaS)
- Lambdas (Function as a Service - FaaS)
- Rekognition (Software as a Service - SaaS)
- S3 (has a global console, but this is a Regional Service)
- VPC (Virtual Private Cloud)
- DynamoDB
- Storage Gateway


# 📝IAM - Identity Access Management

- [IAM Permissions](#iam-permissions)
- [IAM Account Security](#iam-account-security)
- [How a user can access AWS](#how-a-user-can-access-aws)
- [IAM Security Tools](#iam-security-tools)
- [IAM Best Practices](#iam-best-practices)
- [IAM Shared Responsibility Model](#iam-shared-responsibility-model)

Identity Access Management is a Global Service.

- First we have our Root Account. This account should not be shared or even used. We must use only to Create another users, called IAM Users.
- Users are people in our organization and they can be grouped.
- The Groups only contain users. (Not allowed Group Chain).
- Groups and Users are needed, because AWS Services needs Permissions, and we create these permissions for each group or user.

### IAM Permissions

**Policies**

- Users and Groups can be assigned to JSON Documents that contains the permissions (allowing or denying).
- Policies define the permissions to users/groups.
- Apply the "Least Privilege Principle". Only give the needed permissions.

Policy content:

```
A JSON policy document includes these elements:

Optional policy-wide information at the top of the document
One or more individual statements
Each statement includes information about a single permission. The information in a statement is contained within a series of elements.

Version – Specify the version of the policy language that you want to use. As a best practice, use the latest 2012-10-17 version.

Statement – Use this main policy element as a container for the following elements. You can include more than one statement in a policy.

Sid (Optional) – Include an optional statement ID to differentiate between your statements.

Effect – Use Allow or Deny to indicate whether the policy allows or denies access.

Principal (Required in only some circumstances) – If you create a resource-based policy, you must indicate the account, user, role, or federated user to which you would like to allow or deny access. If you are creating an IAM permissions policy to attach to a user or role, you cannot include this element. The principal is implied as that user or role.

Action – Include a list of actions that the policy allows or denies.

Resource (Required in only some circumstances) – If you create an IAM permissions policy, you must specify a list of resources to which the actions apply. If you create a resource-based policy, this element is optional. If you do not include this element, then the resource to which the action applies is the resource to which the policy is attached.

Condition (Optional) – Specify the circumstances under which the policy grants permission.
```

[AWS Docs Reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies.html#access_policies-json)

**Roles**

- Are created for another Services, so they can access or execute a process inside another service.
- Some AWS service will need to perform actions on your behalf. To do so, we will assign permissions to AWS services with IAM Roles.
- We need to create or attach policies to this Role to grant the permissions.
- Then we attach the role to the service, and the service will be able to perform actions in out behalf.
- CamelCaseNamed
- The most common roles: [EC2 Instance Roles, Lambda Function Roles, Roles for CloudFormation]

<p align="center" width="100%"><img src="assets/roles.jpg" alt="roles" width="300"/></p>

### IAM Account Security

AWS Provides more security allowing us to add protection mechanisms to our account.

**MFA (Multi Factor Authentication)**

- Password that you know + security device you own.
- Main benefit of MFA: if a password is stolen or hacked, the account is not compromised.
- MFA Devices: Virtual Devices (Authy, Google Authenticator), Universal 2nd Factor (U2F) Security Key, Hardware Key Fob MFA Device, Hardware Key Fob MFA Device for AWS GovCloud (US)

**Password Policy**

- Set a minimum password length.
- Require specific characters in the password: Upper/Lower, numbers, non-alphanumeric.
- Allow IAM users to change their passwords.
- Require password change each X days.
- Prevent password reuse.

### How a user can access AWS?

A user can access AWS by:

**AWS Management Console**

- Root or IAM user + password (+ MFA optional)

**AWS CLI**

- Command Line Interface, protected by Access Key and Secrets. If wants to use the CLI in the own computer, so the user needs to install the AWS CLI.

**AWS CloudShell (CLI)**

- is a CLI inside the AWS Console, the user don't need to install this one.

**AWS SDK**

- Software Development Kit, for coding, also protected by Access Key and Secrets.

The access keys and secrets are generated through the AWS Console and must be kept in secret. The users manages their own keys.
Access Keys is similar to the username.
Secret Keys is similar to the password.

### IAM Security Tools

**IAM Credentials Report** [root-account level]

- The Credentials Report lists all your account's users and the status of their credentials.

**IAM Access Advisor** [iam-user level]

- The access advisor shows the services permissions granted to a user and when those services were last accessed.

### IAM Best Practices

- Don’t use the root account except for AWS account setup
- One physical user = One AWS user
- Assign users to groups and assign permissions to groups
- Create a strong password policy
- Use and enforce the use of Multi Factor Authentication (MFA)
- Create and use Roles for giving permissions to AWS services
- Use Access Keys for Programmatic Access (CLI / SDK)
- Audit permissions of your account with the IAM Credentials Report
- Never share IAM users & Access Keys

### IAM Shared Responsibility Model

AWS Is response for the infrastructure and the user is responsible for how he use this infrastructure.

**AWS Responsibility**

- Infrastructure (global network security)
- Configuration and vulnerability analysis
- Compliance validation

**User Responsibility**

- Users, Groups, Roles, Policies management and monitoring
- Enable MFA on all accounts
- Rotate all your keys often
- Use IAM tools to apply appropriate permissions
- Analyze access patterns & review permissions


# 📝EC2 - Elastic Cloud Compute

- [How to Create a Basic EC2 Instance](#How-to-Create-a-Basic-EC2-Instance)
- [Amazon Machine Image](#Amazon-Machine-Image)
- [EC2 Instance Types](#ec2-Instance-Types)
- [EC2 Security Groups](#EC2-Security-Groups)
- [EC2 SSH and Instance Connect](#EC2-SSH-and-Instance-Connect)
- [EC2 Instance Roles](#EC2-Instance-Roles)
- [EC2 Instances Purchasing Options](#EC2-Instances-Purchasing-Options)
- [EC2 Shared Responsibility Model](#EC2-Shared-Responsibility-Model)
- [EC2 Instance Storage](#EC2-Instance-Storage)
- [EC2 Elastic Load Balancing and Auto Scaling Groups](#EC2-Elastic-Load-Balancing-and-Auto-Scaling-Groups)

AWS EC2 is one of the most popular of AWS services. EC2 stands to Elastic Compute Cloud and is a service where you can rent virtual servers from AWS. This Cloud Computing is from Infrastructure as a Service (IaaS) type. EC2 is also a Region Scoped Service.

### How to Create a Basic EC2 Instance

To create an EC2 Instance we need to follow the bellow steps on EC2 Console:

- Select an AMI (Amazon Machine Image). It is the operating system. (most common is Amazon Linux 2 and it is free tier)
- Select the Instance Type. It is the server hardware configurations (t2-micro is free tier)
- Configure Instance Details if you want to change anything. In this case, we can create the `user data` to instance, that is the code start to it. Bellow a script to print hello world on our instance.

```bash
#!/bin/bash
# Use this for your user data (script from top to bottom)
# install httpd (Linux 2 version)
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
echo "<h1>Hello World from $(hostname -f)</h1>" > /var/www/html/index.html
```

- Create the storage: It is data disk available in our instance and it is customizable. By default Whenever you launch an EC2 instance, the instance store volume type is ephemeral (Amazon EC2 instance store)

- Create a Security Group (SG) and add a rule to HTTP allows access from anywhere, `Port 80 and Source 0.0.0.0/0, ::/0`

- Finally Review and Launch. (Save the Key/Par Generated). A few seconds later the instance will be available and accessible.

- When finish it, just stop/terminate the instance.

---

### Amazon Machine Image

**AMIs** stands to Amazon Machine Image and are a customization of an EC2 Instance:

- You must use an AMI from the same region as that of the EC2 instance. (The region of the AMI has no bearing on the performance of the EC2 instance)
- We can add our own software configurations, operating systems, monitoring and others configurations.
- This will leverage to a faster boot, because the software is pre-packed.
- AMIs are built for a specific region (can be copied across them)
- We can launch AMIs: 1) provided by AWS, 2) our own AMI or 3) AMIs from AWS Marketplace.
- We can create an AMI starting from an instance. It will create the AMI and a snapshot of the storage.

**EC2 Image Builder**:

- Used to automate the creation of Virtual Machine or Container Images.
- Automatically: Create, maintain, validate and test AMIs
- The builder can run scheduled (when a pack is updated, weekly, etc...)
- It is a free service (pay for the resources)

In order to create it by Image Builder we need to create an `Image Pipeline`, `Recipe`, `Define infrastructure` and `Define Distribution`:

- This pipeline will have a name/description and a schedule (By time, by Cron or Manual)
- After that we must choose or create a `Recipe`: In this Recipe we choose if it is a AMI or a Docker image, Select the OS, the components to be installed with the image (such as Java, AWS Cli), and the tests that we can do to check if the image has the correct components.
- After, we must select `Define infrastructure`: To do it we need to create a Role for the Image Builder execute actions in our behalf, it is an EC2 Role. Then we select the instance Type (e.g. t2.micro) and other basic configurations.
- Finally, we `Define Distribution`, by choosing the Region(s) to be available and ready to use.

Since this pipeline is ready we can execute anytime to build our AMI. This pipeline will create an EC2 instance (where the AMI will be created based on) and terminate it. As well an instance will be created to test and after testing phase, it will be terminated. Finally it will create the distribution and the AMI will be available to use.

<p align="center" width="100%"><img src="assets/image-builder.jpg" alt="image-builder" width="500"/></p>

---

### EC2 Instance Types

**AWS has the following naming convention:**
m5.2xlarge

- m: instance class
- 5: generation of the instance (AWS improve them over time)
- 2xlarge: the size of the instance. (Memory, CPU, etc... )

There are a few [instance types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html):

**General Purpose**:

- Great for a diversity of workloads such as web services and code repositories.
- Use cases: Small and midsize databases, Data processing tasks that require additional memory, Caching fleets.
- This one have a good balance between the compute, memory and networking.
- t2.micro is an example

**Compute Optimized**:

- Great for compute-intensive workloads that require high performance processors.
- Services such as Batch processing, media transcode, High performance web servers, High performance compute (HPC), Scientific modeling and Machine Learning or Dedicated Gaming Servers.
- For now, all the Compute Optimized Instance have naming starting with _C_, like c5.large.

**Memory Optimized**:

- These types have fast performance for workloads that require in-memory processing.
- Use cases: High-performance, relational (MySQL) and NoSQL (MongoDB, Cassandra) databases. Distributed web scale cache stores that provide in-memory caching of key-value type data (Memcached and Redis). In-memory databases using optimized data storage formats and analytics for business intelligence (for example, SAP HANA). Applications performing real-time processing of big unstructured data (financial services, Hadoop/Spark clusters). High-performance computing (HPC) and Electronic Design Automation (EDA) applications.

- Most of the instances of this type starts with _R_ (that remembers RAM). We also have instances starting with _X_.

**Storage Optimized**

- Made for storage-intense tasks that require high, sequential Read and Write access to large data sets on local storage
- Use cases: High Frequency Online Transaction Processing (OLTP) systems, Relational and NoSQL databases, Cache for in-memory database (like Redis), Data warehousing, Distributed file systems.

**Accelerated Computing**:

- Simmilar to Memory optimized, but this one use hardware accelerators, or co-processors, to perform functions such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs.

---

### EC2 Security Groups

- They are fundamental of network security in AWS. They control how traffic is allowed into our EC2 instances. It is the Firewall of the instance.
- They contain only **Allow** rules
- Reference by IP or by other Security Group
- Regulate the Access to the Ports, Authorized IP ranges (IPV4 and 6)
- Control of inbound network (from outside to inside the instance)
- Control of outbound network (from instance to outside) - by default, all traffic outbound (from our instance to the rest of the world) is allowed.
- Common Ports that we need to know

<p align="center" width="100%"><img src="assets/security-group.jpg" alt="security-group" width="400"/></p>

```
22 - SSH (Secure Shell) - log into EC2 Linux instance
22 - SFTP - (Secure File Transport Protocol) - upload file using SSH
21 - FTP (File Transfer Protocol) - upload files into a file share
80 - HTTP - access unsecured websites
443 - HTTPS - access secured websites
3389 - RDP (Remote Desktop Protocol) - Log into a windows instance
```

---

### EC2 SSH and Instance Connect

- SSH is one of the most important function. It allows you to control a remote machine, uptade, and lots of configurations, all using the command line.
- Mac, Linux and Win 10+ = SSH and Windows <10 = Putty

```bash
# check permissions on .pem file (must be chmod 0400)
# and then log using ssh:

ssh -i permissionsFile.pem ec2-user@ec2-public-ip
```

- **EC2 Instance Connect** is an Second Option to run SSH directly from Console. It runs a browser based SSH instance connection/terminal. In this case a temporary Key is uploaded to EC2 instance by AWS. Works only out-of-the-box with Amazon Linux 2.

- Remember to Allow port 22 in Security Group.

---

### EC2 Instance Roles

In order to run or access aws services, usually in our terminal we would use `aws configure`and pass our credentials. But in EC2 instance it is not a good practice, since it is a server and can be managed by more than one person. So if you want to EC2 to perform an action in other services in our behalf, we need to create a role to this EC2.

- For example: if we want to execute the command `aws iam list-users` we need to create a role to that contains the IAM Policy, in this case, the read user permission. To do it we need to create the policy and the role in our IAM Console and after that, in EC2 console, attach the role to the EC2 instance. Now our instance can perform this list-users action without require your secret keys directly inside the server.

---

### EC2 Instances Purchasing Options

EC2 Instances in the cloud, the default type of EC2 is on-demand instances.

**On-demand instances**

- No commitment to user to specific time.
- Full control over the life-cycle of instance: when start, stop, etc.
- Pay only for the seconds that the instance is on state Running.
- Recommend to short workloads and irregular runnings that cannot be stopped until finish.

**Reserved Instances**:

- Minimum commitment of one year, maximum of three years.
- Up to 75% discount compared to On-Demand.
- Purchasing options: no upfront | partial upfront | all upfront (upfront = pay all now and get more discount).
- Can buy a instance that runs in one specific Region [Regional] or Specific Zone [Zonal] - it affects the price.
- There are three kinds of reserved instances:

1. **Reserved Instances**: for long workloads and always use the selected type of instance during the commitment time. (use case: host a database)
2. **Convertible Reserved Instances**: long workloads with flexible instances (can change the type of the instance over time)
3. **Scheduled Reserved Instances**: When you need to use the instance only in scheduled time. For example: when you need to use the instance every monday from 6am to 11am for one year.

About the prices: A Standard Reserved Instance provides a more significant discount than a Convertible Reserved Instance.

| Action                                       | Standard Reserved Instance | Convertible Reserved Instance                                                                  |
| -------------------------------------------- | -------------------------- | ---------------------------------------------------------------------------------------------- |
| Modify Instance                              | Modify Attributes          | Modify Attributes                                                                              |
| Exchanging Reserved Instances                | Can't be exchanged.        | Can be exchanged during the term for another Convertible Reserved Instance with new attributes |
| Selling in the Reserved Instance Marketplace | Can be sold.               | Can't be sold.                                                                                 |
| Buying in the Reserved Instance Marketplace  | Can be bought.             | Can't be bought.                                                                               |

**Spot Instances**: Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud. Spot Instances are available at up to a 90% discount compared to On-Demand prices.

- You can "lose" at any time, because spot price changes.
- Can be combined with On-demand Instances
- Up to 90% of discount compared to On-Demand
- Has access to multiple AWS services.
- You can use Spot Instances for various stateless, fault-tolerant, or flexible applications such as big data, containerized workloads, CI/CD, web servers, high-performance computing (HPC), and test & development workloads.

**Dedicated Hosts**: Book an entire physical server.

- An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your use.
- This type address compliance requirements, reduce cost by allowing you to use your own licenses
- Three year reservation period
- More expensive
- Useful to compliance needs/regulatory issues, use software that require licenses.

**EC2 Dedicated Instances**: Hardware dedicated to the customer.

- Can share the hardware if instances within the same account.
- It is a soft version of dedicated hosts.

Difference between Dedicated Hosts and EC2 Dedicated Instances

- Both allow you to use dedicated server, but in the EC2 Dedicated Hosts you pay for each Host and can have more access to the hardware it is much more flexible and is recommended when you have server bound licenses, while in EC2 Dedicated Instances you pay for each instance and cannot have access to hardware.

---

### EC2 Shared Responsibility Model

**AWS Responsibility**

- Infrastructure (global network security)
- Isolation of physical hosts
- Replace Faulty Hardware
- Compliance validation

**User Responsibility**

- Security Groups rules
- Operating System patches and updates
- Software installed inside the instance
- IAM Roles to/on EC2 and users access
- Data security on your instance

**Shared Responsibility**:

> Security and Compliance is a shared responsibility between AWS and the customer. This shared model can help relieve the customer’s operational burden as AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates.


# 💾 EC2 Instance Storage

- [EBS Elastic Block Store - Volumes](#ebs-elastic-block-store---volumes)
- [EBS Snapshots](#EBS-Snapshots)
- [EC2 Instance Store](#EC2-Instance-Store)
- [EFS Elastic File System](#EFS---Elastic-File-System)
- [EBS vs. EFS](#EBS-vs-EFS)
- [Amazon FSx](#amazon-fsx)
- [EC2 Storage Shared Responsibility Model](#EC2-Storage-Shared-Responsibility-Model)
- [Summary](#Summary)

## EBS Elastic Block Store - Volumes

**Main Information about Elastic Block Store**:

- An EBS Volume is a **network drive** that you can attach to your instance while they run. It uses the network to communicate with the instance, so it might have a little bit of latency.
- It can be detached from an instance and attached to other quickly (benefit of network driver)
- It Can persist data even if the instance is terminated.
- Can be mounted to one instance at a time (On CCP level exam). One instance can have more than one EBS at a time.
- They are bound to a specific availability zone, this means if your instance is in us-east1-a and your EBS is in us-east1-b, they cannot be bound to each other. To do it across AZs, we need **Snapshots** or create an EBS Volume to the same AZ.
- It have a provisioned capacity in GBs or IOPs (inputs and outputs per second). The billing is based on this capacity, and this capacity can be increased/decreased over time.

**Good to know about EBS**:

- Free tier: 30 GB of EBS on General Purpose (SSD) or Magnetic per Month.
- Analogy to a "network USB stick" that you can plug in other computers.
- We can have existing EBS volumes that keeps unattached.
- EBS Volumes are network drives with good but 'limited' performance: EC2 Instance Store have the best performance, because they are the hard disk, physical, on the data-center attached on the machine that runs the server.

> Amazon Elastic Block Store (EBS) is an easy to use, high-performance block storage service designed for use with Amazon Elastic Compute Cloud (EC2) for both throughput and transaction-intensive workloads at any scale. A broad range of workloads, such as relational and non-relational databases, enterprise applications, containerized applications, big data analytics engines, file systems, and media workflows are widely deployed on Amazon EBS.

<p align="center" width="100%"><img src="assets/ebs.jpg" alt="ebs" width="400"/></p>

## EBS Snapshots

Snapshot is a backup of our EBS Volumes at a point in time. It keeps available in one Region. But to use it in a volume, we need to create the volume inside an AZ.

- To Create this snapshot you don't have to detach the volume from an instance (besides it is recommended)
- With the Snapshot we can Copy to other regions or AZ's or Create a brand new EBS Volume.
- This snapshot will be a "start" to the new EBS Volume. So the new volume will start with the data starting from the snapshot. The new volume will be a Restore from a snapshot.
- Amazon EBS Snapshots are stored incrementally, which means you are billed only for the changed blocks stored

<p align="center" width="100%"><img src="assets/ebs-snapshots.jpg" alt="ebs-snapshots" width="400"/></p>

## EC2 Instance Store

This is the **physical HARD DRIVE** attached to the server. Limited space, but higher performance. It is called by **ephemeral**

- Better I/O performance. It is good to buffer/cache/scratch data/temp files. Always with short workloads.
- EC2 Instance Store lose their storage and data if they are stopped.
- Risk of losing data (because it is a physical hardware)
- Backups and Replications are our responsibility.
- It is Block Level storage.

> An instance store provides temporary block-level storage for your EC2 instance. This storage is located on disks that are physically attached to the host computer. Instance store is ideal for the temporary storage of information that changes frequently, such as buffers, caches, scratch data, and other temporary content, or for data that is replicated across a fleet of instances, such as a load-balanced pool of web servers. Instance storage is temporary, data is lost if instance experiences failure or is terminated. EC2 instance store cannot be used for file sharing between instances.

## EFS - Elastic File System

EFS stands to Elastic File System and it is a Network File System (NFS). This NFS can be attached to hundreds of EC2 instances at a time.

- Amazon EFS is a regional service storing data within and across multiple Availability Zones (AZs) for high availability and durability.
- It is a shared NFS.
- Works in Linux EC2 Instances and works across multiple AZs. It makes EFS High Available and Scalable. But, this also makes the EFS more expensive (3x gp2) and you pay what you use not capacity. If you use only 20gb, that's your usage and you'll pay for this.
- High Available By Default
- Data access: EC2 instances can access files on an EFS file system across many Availability Zones, Regions and VPCs
  - Amazon EC2 instances can access your file system across AZs, regions, and VPCs
  - On-premises servers can access using AWS Direct Connect or AWS VPN.

> Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed, elastic NFS file system. It is built to scale on-demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, eliminating the need to provision and manage capacity to accommodate growth. Amazon EFS is designed to provide massively parallel shared access to thousands of Amazon EC2 instances, enabling your applications to achieve high levels of aggregate throughput and IOPS with consistent low latencies.

<p align="center" width="100%"><img src="assets/efs.jpg" alt="efs" width="300"/></p>

**EFS Storage Options**

- Amazon EFS Standard Storage Class
  - The EFS Standard storage class is designed for active file system workloads, and you pay only for the amount of file system storage you use per month. Data is stored regionally within and across multiple Availability Zones (AZs).
- Amazon EFS Standard-Infrequent Access Storage Class:
  - The EFS Standard-Infrequent Access storage class (EFS Standard-IA) is cost-optimized for files accessed less frequently. Data stored on the EFS Standard-IA storage class costs less than EFS Standard storage class, and you will pay a fee each time you read from or write to a file. Data is stored regionally within and across multiple Availability Zones (AZs).
- Amazon EFS One Zone Storage Class:
  - The EFS One Zone storage class is designed for active file system workloads, and you pay only for the amount of file system storage you use per month. Data is stored within a single Availability Zone. Standard data transfer fees apply for inter-AZ or inter-region access to file systems.
- Amazon EFS One Zone-Infrequent Access Storage Class:
  - The EFS One Zone-Infrequent Access storage class (EFS One Zone-IA) is cost-optimized for files accessed less frequently. Data stored on the EFS One Zone-IA storage class costs less than the One Zone storage class, and you will pay a fee each time you read from or write to a file. Data is stored within a single Availability Zone. Standard data transfer fees apply for inter-AZ or inter-region access to file systems.
- Amazon EFS Bursting Throughput (Default):
  - In the default Bursting Throughput mode, there are no charges for bandwidth or requests, and you get a baseline rate of 50 KB/s per GB of throughput included with the price of EFS Standard storage class. Read operations are metered at a 1:3 ratio toward this rate, so you can drive up to 150 KB/s per GB of read throughput or 50 KB/s per GB of write throughput with this baseline rate.
- Amazon EFS Provisioned Throughput:
  - You can optionally select the Provisioned Throughput mode and provision the throughput of your file system independent of the amount of data stored and pay separately for storage and throughput. Read operations are metered at a 1:3 ratio toward this rate, so you can drive up to 3 MB/s of read throughput or 1 MB/s of write throughput for every 1 MB/s of throughput provisioned. Like the default Bursting Throughput mode, the Provisioned Throughput mode also includes 50 KB/s per GB (or 1 MB/s per 20 GB) of throughput in the price of EFS Standard and EFS One Zone storage classes. You are billed only for the throughput provisioned above what you are provided based on data you have stored.

### EBS vs EFS

- EBS are bound to one AZ and can be attached to one instance at a time. To move across regions we can use the snapshots (it is just a copy).
- EFS works across multiple regions and can be attached to multiple instances. The same data is available to all instances. It makes the EFS a shared file system.

## Amazon FSx

We have two types of FSx in AWS:

**Amazon FSx for Windows File Server**:

- Fully managed, highly reliable and scalable windows native shared file systems.
- Built on windows file server and supports SMB Protocol (Server Message Block) and Windows NTFS (New Technology File System - windows file system)
- Integrated with Microsoft Active Directory
- Can be accessed from AWS or On-premise

<p align="center" width="100%"><img src="assets/fsx.jpg" alt="fsx" width="300"/></p>

**Amazon FSx for Lustre**:

- A fully managed, high-performance, scalable file storage for High Performance Computing (HPC)
- Works for Linux and Clusters (Lusters)
- Machine Learning, Analytics, Video Processing, Financial Modeling
- Scales up to 100s GB/s, millions of IOPS, sub-ms latencies

<p align="center" width="100%"><img src="assets/fsx-hpc.jpg" alt="fsx" width="400"/></p>

### EC2 Storage Shared Responsibility Model

**AWS Responsibility**

- Infrastructure
- Replication for Data through the Drivers and Volumes (ensure disasters recover or in case a Hardware stop working)
- Replace Faulty Hardwares
- Ensure that their employees cannot access our data.

**User Responsibility**

- Setup backup and snapshots procedures
- Data encryption
- Responsibility about the data content on drivers
- Understand the risk of using [EC2 Instance Store](#EC2-Instance-Store)

## Summary

- EBS volumes:
  - Network drives attached to one EC2 instance at a time
  - Mapped to an Availability Zones
  - Can use EBS Snapshots for backups / transferring EBS volumes across AZ
- AMI: create ready-to-use EC2 instances with our customizations
  - EC2 Image Builder: automatically build, test and distribute AMIs
- EC2 Instance Store:
  - High performance hardware disk attached to our EC2 instance
  - Lost if our instance is stopped / terminated
- EFS: network file system, can be attached to 100s of instances in a region
- EFS-IA: cost-optimized storage class for infrequent accessed files
- FSx for Windows: Network File System for Windows servers
- FSx for Lustre: High Performance Computing (HPC) Linux file system

# 💻 Elastic Load Balancing and Auto Scaling Groups

This is where we can see the power of cloud computing, because of the automatically scaling and distribution of loads with low configurations.

- [Scalability & High Availability](#scalability--high-availability)
- [Scalability vs Elasticity (vs Agility)](#scalability-vs-elasticity-vs-agility)
- [Elastic Load Balancer (ELB)](#elastic-load-balancer-elb)
- [Auto Scaling Groups (ASG)](#auto-scaling-groups-asg)
- [Scaling Strategies](#scaling-strategies)
- [Summary](#summary)

## Scalability & High Availability

**Scalability**: Scalability is linked but is different from High Availability, Scalability means that the application or system can handle different amounts of load by adapting. There are two different kinds of scalability:

- **Vertical Scalability**: Means increasing the size of the instance:

  - Add more resources (like CPU power, RAM, Storage, etc...).
  - It is limited due the hardware limitations.
  - It is recommended to non-distributed systems as Databases.
  - Scale Up (increasing) or Scale Down (decreasing)
  - A few analogies:
    1. Instead of using a t2.micro, use a t2.large (increasing)
    2. Instead of have a Junior employee, we hire a Senior employee because him can handle more workloads and solve it faster.

- **Horizontal Scalability (elasticity)**: Means increasing the number of instances or systems to our application.
  - Have no limitations, we can always add more instances
  - Implies to distributed systems and web apps/modern apps
  - In AWS **Scale Out** means increasing the number of instances and **Scale In** means decreasing the number of instances.
  - On AWS is easy to scale because of the [**Auto Scaling Groups**](#auto-scaling-groups-asg) and [**Load Balancer**](#elastic-load-balancer-elb)
  - A few analogies:
    1. Add more instances to our application run (Scale out)
    2. Hire multiple temporary employees to handle with workload. As soon the load is lower you can dismiss them and keep your default number of employees.

**High Availability**: Means that your application is available in multiple locations, in this case that our service running in multi availability zones.

- High Availability means to run our app/system in at least two different AZs
  - This means more Security, Disaster Recover, Keep the work running.
- A few analogies:
  1. To do it in AWS we have ASG and ELB that are multi-az.
  2. This company has employees in three different cities in the country. So if anything stops one branch, the other two still are working and can handle the workload.

## Scalability vs Elasticity (vs Agility)

- **Scalability**: is the ability for a system to accommodate a larger load by making the hardware stronger (vertical scale, scale-up) or by add nodes (horizontal scale, scale-out).

- **Elasticity**: Once the system is scalable, elasticity means that there will be some "auto-scaling" so that system can scale based on the load. This is "cloud-friendly": pay-per-use, match demand, optimize costs.

- **Agility**: (not related to scale - distractor), new IT resources available very quickly. (one click away, what used to happen in weeks)

## Elastic Load Balancer (ELB)

Elastic Load Balancer are managed by AWS and they are servers that forward the internet traffic to multiple servers (EC2 Instances). `They are the backend of EC2 Instances`. The ELB is what will be exposed to the users and when receive the connection/access it will redirect traffic to instances.

**Why use a Load Balancer?**

- Spread the load across multiple downstream instances.
- Expose a single point of access (DNS) to our application.
- Handle with failures of instances (Regular health checks to the instances), don't redirect to unhealthy instances.
- Provide SSL termination (HTTPS) for our websites
- High Availability across zones

**Why use an Elastic Load Balancer?**

- AWS maintains and guarantees that it will be working
  - AWS takes care of upgrades, maintenance, high availability
  - AWS provides only a few configuration knobs
  - We only have to configure some behaviors of our ELB

**Four Types of ELB**

- Application Load Balancer: (HTTP/HTTPS only) - Layer 7
- Network Load Balancer: (Ultra-high performance, allows TCP) - Layer 4 (handle with millions of request per second, like gaming situation).
- Gateway Load Balancer: New AWS ELB used when you need to deploy and manage a fleet of third-party virtual appliances that support GENEVE
- Classic Load Balancer: (slowly retiring) - Layer 4 and 7

When configuring the ELB we need to create a `Target Group`, this target group contains the instances that are going to handle the multiple access.

<p align="center" width="100%"><img src="assets/elb.jpg" alt="elb" width="400"/></p>

## Auto Scaling Groups (ASG)

The loads and access of websites can change overtime, so we need to add or remove resources. We can do it automatically by using the Auto Scaling Groups. To do so, we need to have an Elastic Load Balancer configured, which means that our application can manage the loads.

- The main goal of ASG:
  - Scale Out (add EC2 instances) to match an increased load.
  - Scale In (remove EC2 instances) to match a decreased load.
  - Ensure that we have a minimum, desired and maximum number of machines running.
  - Automatically register new instances to our Load Balancer.
  - Replace unhealthy instances (If a instance fails, it register a new one automatically)
- The Auto Scaling Groups leaverage to **costs savings**, since we can adjust the capacity automatically and scale in the right moments (imagine a peak of access in our website, we are going to have machines available to deal with the load and after that we don't need them anymore. In this case we pay more, but just on the peak and after that we dont have to pay the any additional machines).

## Scaling Strategies

**Manual Scaling**: We change manually in the console/cli the desired capacity of our ASG.

**Dynamic Scaling**: Respond to changing demand. We have four types of dynamic scaling strategies.

- Simple/Step Scaling:
  - When a CloudWatch alarm is triggered (example CPU over 70%), then add 2 Instances
  - When a CloudWatch alarm is triggered (example CPU less then 30%), then remove 1 Instance
- Target Tracking:
  - Based on metrics of the target. (no cloudwatch, just tracking the resource), example: I want the average ASG CPU to be around 40% of capacity. So it will add or remove instances to reach this goal.
- Scheduled Scaling: Anticipating known events to handle better with the loads.
  - Example: On lunch time (starting 11am) i want my min capacity to be 15 instances. After 14h i want 7 instances.
- Predictive Scaling: Uses machine learning to predict future traffic and scale based on past identified patterns.
  - This is useful when our load has predictable time-based patterns.

### Tips, to Create an ASG:

- When creating an ASG Group, we need to create a template, so the new instances will be inherited from it. Whenever we need to register a new instance, ASG will get this template and launch it for us.
- We can also attach our Load Balancer to our ASG and select our `target group`, so the new instances will be created and attached to the target group.
- Create Health Checks to Replace unhealthy instances
- Create the group size: Minimum of Instances, Desired Number of Instances and the Maximum Number of Instances.
- When create this groups sizes, we can create the Scaling policies to Target tracking scaling policy, this means that we can scale based on CPU usage, network in or out, count of requests per target, etc.

<p align="center" width="100%"><img src="assets/asg.jpg" alt="asg" width="400"/></p>

Summary to Create an Auto Scaling Group with Load Balancing:

- Create the Load Balancing (Application Load Balancer) give it a name, select the AZs to be available and the Security Groups.
- Create the Target Groups (attach instances if needed)
- Create the ASG Group configurations (select subnets, template instance, select the target groups, select health checks, select the group sizes [min, desired, max] + scaling polices).
- Finally, the server i'll be ready to scale and is totally elastic. 👌✔

<p align="center" width="100%"><img src="assets/elb-asg.jpg" alt="elb-asg" width="400"/></p>

## Summary

- High Availability (application available in multi-az) vs Scalability (vertical means add size/cpu to instance and horizontal means add more instances) vs Elasticity (capacity of scale up and down when needed) vs Agility (work faster) in the cloud.
- Elastic Load Balancer:
  - Distribute traffic across backend EC2 instances, can be Multi-A
  - Supports health check
  - 3 types: Application LB (HTTP – L7), Network LB (TCP – L4), Classic LB (old)
- Auto Scaling Groups (ASG):
  - Implement Elasticity for your application, across multiple AZ
  - Scale EC2 instances based on the demand on your system, replace unhealthy
  - Integrated with the ELB
- Scaling Strategies:
  - Manual
  - Dynamic: Simple/Step (cloudwatch alarms), Target Tracking, Scheduled Scaling and Predictive Scaling.


# ECS, Fargate and ECR

In AWS we have services to run and manage our applications into containers. In order to understand how these services works, we must first understand what is Docker.

## Docker

Docker is a software development platform to deploy apps. With docker we pack our app into a container and can be run in any OS.

Another definition of Docker would be `Docker is a software development platform that allows you to run applications the same way, regardless of where they are run. It can scale containers up and down within seconds.`

Docker can run in any machine, and it brings some benefits:

- Any Machine and OS
- No compatibilities issues
- Predictable behaviors
- Less work
- Easy to maintain and deploy
- Easy to scale up and down

Inside an EC2 instance we can have multiple docker containers running: An image with node, another with java, another with mysql, etc. When our application is packed into a container it is easy to run inside the EC2.

Docker images can be stored privately or publicly: **Private** are stored into ECR (Elastic Container Registry from Amazon) and the **Public** ones are stored into Docker Hub

## Elastic Container Service

Elastic Container Service (ECS) is a service to Launch docker containers on AWS.

- When we are talking about ECS we must understand that we need to provision and maintain the infrastructure (EC2 Instances).
- AWS takes care of starting and stopping the containers and choose the most available container to place the container.
- It has full integration with the Application Load Balancer

<p align="center" width="100%"><img src="assets/ecs.jpg" alt="ecs" width="300"/></p>

## Fargate

Fargate is also used to launch docker containers on AWS, but Fargate does not require us to provision the infrastructure.

- So more simple service and is serverless, since we don't need to to manage any server or EC2 instances.
- AWS just run the container based on the CPU/RAM our container needs.

<p align="center" width="100%"><img src="assets/fargate.jpg" alt="fargate" width="300"/></p>

## Elastic Container Register

Elastic Container Register (ECR) is the AWS service to store the containers.

- It is a private docker registry.
- This is where the containers are stored, so they can be run by ECS or Fargate.

<p align="center" width="100%"><img src="assets/ecr.jpg" alt="ecr" width="300"/></p>

---

On (CCP) practitioner level is required to understand what is the main differences between ECS Fargate and ECR.
ECS: Run containers with need of provisioning the infrastructure.
Fargate: Run containers without provisioning the infrastructure.
ECR: Where the Containers are stored.

## Summary

- Docker: container technology to run applications
- ECS: run Docker containers on EC2 instances
- Fargate: Run Docker containers without provisioning the infrastructure it is a Serverless offering (no EC2 instances)
- ECR: Private Docker Images Repository


# 📝S3 - Simple Storage Service

S3 stands to Simple Storage Service and it is one of the main services of AWS. This service is basically "Infinity Scaling" storage.
Amazon S3 Console is a global console, that means that we can see all buckets in all regions, but the buckets itself, needs to be bound to a region. S3 is a key value based object storage service. S3 stores data in a flat non-hierarchical structure.

- [S3 Use cases](#s3-use-cases)
- [S3 Buckets](#s3-buckets)
- [S3 Objects](#s3-objects)
- [S3 Create a Bucket and Add Objects](#s3-create-a-bucket-and-add-objects)
- [S3 Security](#s3-security)
  - [S3 Bucket Policy](#s3-bucket-policy)
- [S3 Static Website](#s3-static-website)
- [S3 Versioning](#s3-versioning)
- [S3 Server Access Logging](#s3-server-access-logging)
- [S3 Replication](#s3-replication)
- [S3 Storage Classes](#s3-storage-classes)
- [S3 Glacier Vault Lock and Object Lock](#s3-glacier-vault-lock-and-object-lock)
- [S3 Snow Family](#s3-snow-family)
- [S3 Storage Gateway](#s3-storage-gateway)
- [S3 Shared Responsibility Model](#s3-shared-responsibility-model)
- [Summary](#summary)

## S3 Use cases

- Backup and Storage
- Disaster Recovery (copying data in multiple regions)
- Archive data
- Application Hosting / Web site hosting (static websites uses Amazon S3 as backbone)
- Media Hosting
- Data Lakes & Big Data Analytics
- Software delivery
- Many AWS services uses Amazon S3 as integration/storage as well, such as [EBS Snapshots](../ec2-instance-storage/README.md/#EBS-Snapshots).

## S3 Buckets

Amazon S3 allows people to store `objects` (think as files) in `buckets` (think as directories).

- Buckets must have a unique name (across all regions and accounts)
- Buckets must be created inside a specific Region.
- Naming Convention: To give a name to the bucket must follow this naming convention
  - No uppercase, No underscore, 3-63 characters long, Not an IP, Must start with lowercase letter or number"

## S3 Objects

The `objects` are the files to be stored in S3 Bucket.

- Objects (files) must have a Key, the key is the full path to the object:
  - The key is composed of prefix + object name
    - s3://my-bucket/**my_file.txt**
    - s3://my-bucket/**my_folder1/another_folder/my_file.txt**
  - In this first example the file has only the name, so it has not prefix. It is just 'my_file.txt'
  - In this second example, the prefix is 'my_folder1/another_folder/' and the object name is 'my_file.txt'
- There is no concept of "directories” within buckets. Just keys that contains slashes ('/').
- The objects values are the content of the body.
- Max Object size is 5TB (but can be spitted "multi-part upload" and have multiple files of 5 TB)
- The object contains Metadata: list of key/value pairs, Track data, Security and lifecycle goals
- The Object contains Tags to identify better
- Version ID (S3 Allows Versioning)

## S3 Create a Bucket and Add Objects

- Creating the bucket
  - In AWS Console we can create the bucket, and choose the name (Globally unique name) and the Region. We can also copy the settings from an existing bucket.
  - Choose if we are blocking Global Access (on the internet)
  - Enable versioning
  - Add Tags and Encryption
  - Click in create
- Adding Objects
  - Inside the bucket, just click in Upload (or drag and drop) and select the file.
  - We can also create folder and objects to it.

## S3 Security

**User Based:**

- IAM Policies - attach IAM policies to users or groups and them you be allowed to access the bucket from console/cli/sdk

**Resource Based:**

- [Bucket Policies](#s3-bucket-policy): Rules attached directly to S3 Buckets where we can allow or deny access/actions in our bucket.
- Object Access Control List (ACL) - Object level. Grant or Deny access, but this rule is attached directly to the object. More common ACL.
- Bucket Access Control List (ACL) - Bucket level. Less common, normally use Bucket Policies.

**Encryption:** We can encrypt objects in S3 using encryption keys.

An IAM Principal can access S3 objects if:

- The IAM Permissions allows it **OR** if the Resource Policy allows. (an user that does not contain the IAM Policy to access the bucket, can access a bucket where the Resource Policy allows IAM Users)
- There is not Deny

A few examples of usage of S3 Security:

- Your site exposed to web, by default nobody can access it, to allow it we need to create to attach the **S3 Bucket Policy** to allow the public access.
<p align="center" width="100%"><img src="assets/security-public.jpg" alt="security-public" width="400"/></p>

- An IAM User that already has a policy attached to the account allowing S3 access. In this case there is no need to create the S3 Bucket Policy.
<p align="center" width="100%"><img src="assets/security-iam.jpg" alt="security-iam" width="400"/></p>

- An EC2 instance wants to access our S3, so we need to create a Role to EC2 and attach the permissions (policies) to it and attach the role in our EC2. Now the instance will be able to access the bucket.
<p align="center" width="100%"><img src="assets/security-role.jpg" alt="security-role" width="400"/></p>

- Cross-Account-Access: For this case we may use the S3 Bucket Policy, which will allow the cross-account access.
<p align="center" width="100%"><img src="assets/security-cross-account.jpg" alt="security-cross-account" width="400"/></p>

### S3 Bucket Policy

Bucket policies are JSON based policies, looks like the IAM Policy; In this document we need to define:

- Resources: The AWS S3 Resource. We can use, for example, the ARN like `arn:aws:s3:::jlimadev-demo-april-2021/*` to allow everything inside the resources. In this case read all objects from my bucket. (Example policy bellow)
- Action: Set of API to allow or deny (e.g. S3:GetObject)
- Effect: Allow or Deny
- Principal: Who can access?

Usually we use S3 Bucket to:

1. Grant Public Access to the bucket; (for this we must remove the public access settings on the bucket on `Block all public access` settings on bucket permissions tab)
2. To force objects to be encrypted at the upload
3. Grant access to another account (cross-account)

Public access policy example, generated by AWS Policy Generator:

```json
{
  "Id": "Policy1617654569293",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1617654567141",
      "Action": ["s3:GetObject"],
      "Effect": "Allow",
      "Resource": "arn:aws:s3:::jlimadev-demo-april-2021/*",
      "Principal": "*"
    }
  ]
}
```

## S3 Static Website

S3 Can host static websites and have them accessible on the www.
S3 website has an URL an this URL can be public or not.

- URL structure:
  - `bucket-name`.s3-website-`AWS-region`.amazonaws.com (inside the region)
  - `bucket-name`.s3-website.`AWS-region`.amazonaws.com (outside the region)

To create an Static Web site we can upload a `index.html` in our bucket and, in Bucket Properties, activate the `static websites hosting` option.

- We cannot forget to allow all the public access to our website and create the Bucket Policy to allow internet access.
- If try to access a not public S3 Bucket, a 403 error will show up.

## S3 Versioning

Keep versions of the objects in S3 Bucket. Anytime we update a file, it will get a new version. Versioning is activated in bucket level. To enable it in AWS Console, we need to go in our Bucket and enable `Bucket Versioning`.

Advantages by activating the versioning feature:

- Protection to file deletion (intended or unintended).
- Restore versions of the file.
- Easy rollback to previous versions.

The file when is versioned, it keeps the same key, but Increment the key by 1.

Important to understand about versioning:

- By default, versioning is not enabled, but we can enable whenever we want.
- File only start to get versions when we enable this feature to the bucket.
- Files prior the versioning will get the first version as null.
- Suspending versioning will not suspend versioned files.

About deleting versioned objects:

- To delete permanently an object, we need to select the specific version to delete.
- When we delete without choosing the version, it will add a `Delete Mark` to the object. To delete permanently we need to do it in each version.
- If we want to restore an object with delete mark, we need to perform the delete action again, but in this case, it will delete the delete mark, making the the object be available.

## S3 Server Access Logging

It is for audit purposes, enables log access to S3Bucket. Any access (allowed, denied) will be logged into another S3 bucket.

- The logs are written in a specific bucket for logs.
- This data can be analyzed: Get errors, issues, audit, suspicious patterns.

We can enable it in our bucket properties and change the `Server access logging` and select the target bucket. So, we cannot forget to create the target bucket, where the logs will be stored.

<p align="center" width="100%"><img src="assets/s3-logs.jpg" alt="s3-logs" width="100" height="200"/></p>

## S3 Replication

We have two types of data replication: `Cross-Region-Replication (CRR)` and `Same-Region-Replication (SRR)`.

- Replicate all the content continuously to another bucket, it happens asynchronously.
- For this we must enable versioning in **Source** and **Destination** Bucket.
- The buckets can be in different accounts. (Need the proper IAM permissions)
- The replication rule needs a IAM Role to perform the replication. It creates one automatically or we can create our own role.

Cross-Region-Replication (CRR) use cases: Compliance, lower latency access, replication cross-account.

Same-Region-Replication (SRR) use cases: log aggregation, live replication between test and prod environments.

- It does not replicate files before the replication setting be set, only new files. To replicate existing files we must re-upload or use s3 sync tool.
- If we need to deletions we also need to set this option.

<p align="center" width="100%"><img src="assets/s3-replication.jpg" alt="s3-replication" width="300"/></p>

## S3 Storage Classes

Amazon S3 has multiple classes of storage, and the type of storage can save some costs. A single bucket can have objects in different classes. They are defined in Object Level, we can set it when we are uploading the file.

To understand better the classes we need to understand the concepts of Durability and Availability.

**Durability**: Means how long your file will keep stored or How often you will lose your file. AWS by default have the High Durability (99,99 | 11 9's) of objects across multiple AZ in all storage classes.

**Availability**:
How readily available a service is. S3 standard has 99.99% availability. S3 may not be available per 53 minutes in a year.

**Pricing**:

- S3 Standard does not charge any data retrieval fee.
- S3 Intelligent-Tiering does not charge any data retrieval fee.
- All other storage classes have a retrieval fee.

The S3 storage classes are:

**Amazon S3 Standard - General Purpose:**

- This is the most common. Used for frequently accessed data
- 99,99% of Availability
- Low latency and high throughput
- Sustain 2 concurrent facility failures
- Use cases: Big Data analytics, mobile & gaming applications, content distribution

**Amazon S3 Standard - Infrequent Access (IA):**

- When you don't access the file often, but requires rapid access when needed.
- 99,99% of Availability
- Lower cost compared to Amazon S3 Standard, but retrieval fee
- Sustain 2 concurrent facility failures
- Use Cases: As a data store for disaster recovery, backups…

**Amazon S3 One Zone - Infrequent Access:**

- It is very similar to S3 Standard IA, but his one only saves the file in one AZ.
- 99.5% Availability
- Lower cost compared to S3-IA (by 20%)
- Use cases: Store secondary backups copies of non-premise data, or store data you can easily recreate or to save replicas from another regions in S3.

**Amazon S3 Intelligent Tiering**

- Auto select the type (Frequent or Infrequent)
- 99,99% of Availability
- Same Low latency and high throughput of S3 Standard
- _Cost optimization_ by auto move the objects between tiers based on the use patterns of the object (If used often goes to S3 Standard, otherwise it goes to S3 IA).
- It is also very resilient with events that impact an entire AZ.
- Use cases: when you don't know exactly the tiering or want optimize costs.

**Amazon Glacier**

- Low cost object storage (in GB/month) meant for archiving/backup
- Data is retained for the longer term (years)
- Retrieval options (each one has the fees for retrieval):
  - Expedited (1 to 5 minutes)
  - Standard (3 to 5 hours)
  - Bulk (5 to 12 hours)
- Use cases for: for Backups and Archiving

> Amazon S3 Glacier (S3 Glacier), is a storage service optimized for infrequently used data, or "cold data. Data at rest stored in S3 Glacier is automatically server-side encrypted using 256-bit Advanced Encryption Standard (AES-256) with keys maintained by AWS.

**Amazon Glacier Deep Archive**

- Store data for years in AWS.
- Cheapest option for Backup and Archive
- All the data is replicated in at minimum of 3 AZs
- Retrieval options (each one has the fees for retrieval):
  - Standard (12 hours)
  - Bulk (48 hours)
- For backups and archiving that will take a long time to be retrieved, store regulatory data that demands history, like medical data, financial data, etc. Not very often requested, but if need this data we can have it in up to 12 hours.

**Amazon S3 Reduced Redundancy Storage**: (deprecated - omitted)

In AWS we can create the lifecycle rules, and can se the transition Rules: The transition rules are used to move the objects between the classes by the following rules:

<p align="center" width="100%"><img src="assets/transition-rules.jpg" alt="transition-rules" width="400"/></p>

## S3 Glacier Vault Lock and Object Lock

Lock objects to specified amount of time.

**S3 Object lock**:

- This one adopts the WORM (Write Once, Read Many) class.
- It blocks an object version from being deleted during a specified amount of time.
- You can use S3 Object Lock to meet regulatory requirements that require WORM storage, or add an extra layer of protection against object changes and deletion.
- Users with special permissions can make changes to the Lock policy and delete the data.

**Glacier Vault Lock**:

- This one adopts the WORM (Write Once, Read Many) class.
- We create a Lock Policy to the files, and the files will be locked to modifications.
- Once the policy is set, **no one** can delete or modify the policy (even admins).
- Really good to use when we have compliance data retention rules and policies.

  > S3 Glacier Vault Lock allows you to easily deploy and enforce compliance controls for individual S3 Glacier vaults with a vault lock policy. You can specify controls such as “write once read many” (WORM) in a vault lock policy and lock the policy from future edits. Once locked, the policy can no longer be changed.

  <p align="center" width="100%"><img src="assets/vault-lock.jpg" alt="vault-lock" width="300"/></p>

## S3 Snow Family

Highly-secure, portable devices and offline devices, to collect and process data at the edge, and migrate data into and out of AWS.

The Snow Family: Offline devices to perform data migrations. If takes more than a week to transfer all the data, use the snowball devices.

 <p align="center" width="100%"><img src="assets/snow-family.jpg" alt="snow-family" width="500"/></p>

### Data Migration

- Snow devices types: Snowcone, Snowball Edge and Snowmobile
- Use to migrate data through devices instead of using network. Network is so much more limited to data transfer, so the migration can be much more faster when using this kind f device.
- Reasons why network transfer is limited: Limited connectivity, Limited bandwidth, High network costs, Shared bandwidth, Connection stability.
- Example of usage with S3 use case
  - Normal method: direct upload files to S3 using network.
  - With snow family: AWS send the device and you transfer the data to the device and send it back to AWS. Internally they will upload the data to S3 very fast.

**AWS Snowball Edge**:

- Physical data transport solution to move TBs or PBs of data in or out of AWS.
- Alternative to move data over the network
- Pay per data transfer job
- Provide block storage and Amazon S3 Object storage
- Use case: large data cloud migration, DC decommission, disaster recovery

We have a few types of snowball edge:

- **Snowball Edge Storage Optimized**:
- 80 TB of HDD Capacity for block volume and S3 Compatible Storage
- **Snowball Edge Compute Optimized**:
- 42 TB of HDD Capacity for block volume and S3 Compatible Storage

**AWS Snowcone**:

Small and portable computing device, rugged and secure that resist a multiple natural environments.

- Device used for edge computing, storage, and data transfer.
- 8TBs of usable storage
- Used where snowball does not fit: Drone, Space environments, deserts, missions where does not have connectivity.
- We must provide our own cables and batteries.
- Can be sent back to AWS offline, or connect it to internet and use AWS DataSync to send the data.

**AWS Snowmobile**:
It is a truck to get all the data.

- Each snowmobile has 100 PB of capacity (we can use multiple in parallel)
- Transfer exabytes of data (1EB = 1000PBs = 1000000 TBs)
- To transfer 1EB we need 10 snowmobiles.
- High security: temperature controlled, GPS 24/7 and video surveillance.
- Better use snowball if transfer more than 10PB

**Snowball Process**

1. Request snowball devices from the AWS console for delivery
2. Install the snowball client on your servers
3. Connect the snowball to your servers and copy files using the client
4. Ship back the device when you’re done (goes to the right AWS facility)
5. Data will be loaded into an S3 bucket
6. Snowball is completely wiped

 <p align="center" width="100%"><img src="assets/snow-family-flow.jpg" alt="snow-family-flow" width="500"/></p>

### Edge Computing

- Process data while it is being created on an Edge Location (Anything that does not have internet or cannot access the cloud. For example: A truck on a road, a ship on sea, underground)
- Usually to locations with limited/no internet access and limited/no easy access to computing power.
- we setup a Snowcone or Snowball Edge to Edge computing
  - Preprocess data
  - Machine learning at the edge
  - Transcoding media streams
- We can usually ship it back over time to upload the data.
- All the devices can run EC2 Instances and AWS Lambda Functions (using AWS IoT Greengrass)
- Long-term deployment options: 1 and 3 years of discounted pricing
  **AWS Snowcone (smaller)**:

**AWS Snowball Edge (Compute optimized)**:

- 52 vCPUs, 208 GiB of RAM
- Optional GPU (useful for video processing or machine learning)
- 42 TB usable storage

**AWS Snowball Edge (Storage optimized)**:

- Up to 40 vCPUs, 80 GiB of RAM
- Object storage clustering available

### AWS OpsHub

Historically, to use Snow Family devices, you needed a CLI (Command Line Interface tool). Today, you can use AWS OpsHub (a software you install on your computer / laptop) to
manage your Snow Family Device.

- It is a desktop application to manage Snow Family devices
- Unlocking and configuring single or clustered devices
- Transferring files
- Launching and managing instances running on Snow
  Family Devices
- Monitor device metrics (storage capacity, active
  instances on your device)
- Launch compatible AWS services on your devices
  (ex: Amazon EC2 instances, AWS DataSync, Network File System (NFS))

## S3 Storage Gateway

AWS Storage Gateway is a hybrid solution to extend on-premises storage to S3.

It is a hybrid cloud cloud storage service that gives you on-premises access to virtually unlimited cloud storage. It Allows us to bridge all that happens into on-premisses server directly to the cloud.

- Part of your infrastructure is on-premises
- Part of your infrastructure is on the cloud

Use cases of Hybrid Cloud for Storage:

- Long cloud migrations
- Security requirements
- Compliance requirements
- IT strategy

S3 is a proprietary storage technology (unlike EFS / NFS), so how do you expose the S3 data on-premise? AWS Storage Gateway!

AWS Storage Cloud Native Options:

- Block Storage: Elastic Block Store (EBS) and EC2 Instance Store
- File Storage: Elastic File System (EFS)
- Object Storage: S3 and Glacier

The Storage Gateway is bridge between on-premise data and cloud data in S3.

The gateways will be using one of theses behind the scenes: Amazon EBS, S3 or Glacier.

- So the Hybrid storage service is used to allow on-premises to seamlessly use the AWS Cloud.
- Use cases: disaster recovery, backup & restore, tiered storage

Types of Storage Gateway:

- File Gateway
- Volume Gateway
- Tape Gateway

> All data transferred between the gateway and AWS storage is encrypted using SSL (for all three types of gateways - File, Volume and Tape Gateways).

 <p align="center" width="100%"><img src="assets/storage-gateway.jpg" alt="storage-gateway" width="300"/></p>

## S3 Shared Responsibility Model

**AWS**:

- Infrastructure (global security, durability, availability, sustain concurrent loss of data in two facilities)
- Configuration and Vulnerability analysis
- Compliance Validation

**Customer**:

- S3 Versioning, Bucket Policies, Replication Setup, Logging and Monitoring
- S3 Storage Classes
- Data encryption

## Summary

- Buckets vs Objects: global unique name, tied to a region
- S3 security: IAM policy, S3 Bucket Policy (public access), S3 Encryption
- S3 Websites: host a static website on Amazon S3
- S3 Versioning: multiple versions for files, prevent accidental deletes
- S3 Access Logs: log requests made within your S3 bucket
- S3 Replication: same-region or cross-region, must enable versioning
- S3 Storage Classes: Standard, IA, 1Z-IA, Intelligent, Glacier, Glacier Deep Archive
- S3 Lifecycle Rules: transition objects between classes
- S3 Glacier Vault Lock / S3 Object Lock: WORM (Write Once Read Many)
- Snow Family: import data onto S3 through a physical device, edge computing
- OpsHub: desktop application to manage Snow Family devices
- Storage Gateway: hybrid solution to extend on-premises storage to S3


# 🎲 Database and Analytics

Storing data on disk (EFS, EBS, S3, EC2 Instance Store) can have limits, so if we need to store data with some structure or definition, we may want to use database.
What is a database:

- Can structure the data
- Can build indexes to perform queries/search through the data
- Can define relationship between datasets.

Databases are optimized for a purpose and come with different features, shapes and constraints, thats why exists multiple types of databases:

- [Relational Databases](#relational-databases)
  - [Relational Database Service - RDS](#rds---relational-database-service)
  - [Amazon Aurora](#amazon-aurora)
- [NoSQL Databases](#noSql-databases)
  - [Amazon Elasticache](#amazon-elasticache)
  - [Amazon DynamoDB](#amazon-dynamodb)
  - [Amazon DynamoDB Accelerator - DAX](#amazon-dynamodb-accelerator---dax)
  - [Amazon DocumentDB](#amazon-documentDb)
- [Databases and Shared Responsibility on AWS](#Databases-and-Shared-Responsibility-on-AWS)
- [Amazon Redshift](#Amazon-Redshift)
- [Amazon Elastic MapReduce - EMR](#amazon-elastic-mapReduce---emr)
- [Amazon Athena](#amazon-athena)
- [Amazon Quicksight](#amazon-quicksight)
- [Amazon Neptune](#amazon-neptune)
- [Amazon QLDB](#amazon-qldb)
- [Amazon Managed Blockchain](#amazon-managed-blockchain)
- [Summary](#summary)

## Relational Databases

- Use table to each Entity, the tables have attributes
- We can create a relationship between the tables by using keys (Primary Key/Foreign Key/Indexes)
- Looks like an excel spreadsheet, with link (relationship) between them.
- We can use the SQL (Structured Query Language) to perform queries

Basically we have two ways to create Relational Databases in AWS: RDS and Aurora. They are both managed by AWS, but Aurora is a cloud native and more cloud friendly while RDS will be running known technologies directly in a managed service.

## NoSQL Databases

- NoSQL means non relational databases. They are built for a specific purpose and specific data models. They have flexible schemas for building modern applications.
- Types: Key-Value, Document, Graph, in-memory, search databases
- We can have the data in JSON (Javascript Object Notation) format (we can add new fields, nest data, support arrays, etc.)
- Benefits:
  - Flexibility: easy to evolve data model
  - Scalability: designed to scale-out by using distributed clusters
  - High-performance: optimized for a specific data model
  - Highly functional: types optimized for the data model

Example of JSON data

```json
{
  "name": "John",
  "age": 30,
  "cars": ["Ford", "BMW", "Fiat"],
  "address": {
    "type": "house",
    "number": 23,
    "street": "Dream Road"
  }
}
```

Amazon provides multiple services of NoSQL databases: Elasticache, DynamoDB, DynamoDB Accelerator

## Databases and Shared Responsibility on AWS

AWS Manages the databases, it has multiple benefits:

- Quick Provisioning, High Availability, Vertical and Horizontal Scaling
- Automated Backup & Restore, Operations, Upgrades
- Operating System Patching is handled by AWS
- Monitoring, alerting

We can have our own database (and others technologies) in EC2 Instances, but we must handle and manage it (the resiliency, backup, patching, high availability, fault
tolerance, scaling)

## RDS - Relational Database Service

RDS Stands to Relational Database Service and it is a managed DB by AWS for databases that uses SQL as query language. RDS databases are used for OLTP (Online Transaction Processing).

The performance of AWS managed RDS instance is better than a customer-managed database instance

We can create multiple relational databases types in the cloud, fully managed by AWS:

- Postgres
- MySQL
- MariaDB
- Oracle
- Microsoft SQL Server
- Aurora (AWS Proprietary database)

Advantages of using RDS instead of using a EC2 deployed database:

RDS is a managed service:

- Automated provisioning, OS Patching
- Continuos backup options and restore to specific timestamp (Point in time to restore)
- Monitoring dashboards
- We can create scale to read data from replicas for improved read performance
- Setup Multi AZ setup (Disaster Recovery and Highly Available)
- Setup Maintenance windows for upgrades
- Scaling capability (vertical and horizontal)
- Storage in a EBS (Elastic Block Store GP2 or io1) inside an EC2 instance

**Important**: We cannot use SSH into our database instances.

 <p align="center" width="100%"><img src="assets/rds.jpg" alt="rds" width="500"/></p>

- The ELB will receive the web requests
- The EC2 instances doing/hosting the application logic
- RDS doing Reads and Writes

**RDS Deployment Options:**

- **RDS Read Replicas**: Here we can scale the workload of our DB, we can create up to 15 replicas. The data is written only to main DB and we can read the data from the replicas. **Read Replica improves database scalability and are used for improved read performance**.
  > Read Replicas allow you to create read-only copies that are synchronized with your master database. Read Replicas are used for improved read performance. You can also place your read replica in a different AWS Region closer to your users for better performance. Read Replicas are an example of horizontal scaling of resources.

<p align="center" width="100%"><img src="assets/rds-read-replicas.jpg" alt="rds" width="300"/></p>

- **RDS Multi-AZ**: Failover in case of AZ outage (high availability), data is read/written to main database. Can have only one other AZ as failover (the data will be replicated to failover db, that will be used only if the main db has any kind of issue).
  **The main purpose of RDS Multi-AZ is High Availability**.
  > Amazon RDS Multi-AZ deployments provide enhanced availability and durability for RDS database (DB) instances, making them a natural fit for production database workloads. When you provision a Multi-AZ DB Instance, Amazon RDS automatically creates a primary DB Instance and synchronously replicates the data to a standby instance in a different Availability Zone (AZ).

<p align="center" width="100%"><img src="assets/rds-multi-az.jpg" alt="rds" width="300"/></p>

- **RDS Multi-Region** (read replicas): Disaster recovery strategy in case of Region issue, local performance for global reads (Example: so if we have the main db in us-east-1 and replica in sa-east-1, we can read locally from region sa-east-1 with less latency, but if we need to write, it goes to main db, in us-east-1) replications costs.
  **The main purpose of RDS Multi-Region is Disaster Recovery**

<p align="center" width="100%"><img src="assets/rds-multi-region.jpg" alt="rds" width="400"/></p>

## Amazon Aurora

It is an AWS proprietary technology (not open-source) of a Relational database. Aurora is Cloud Optimized, so it have much more performance compared Relational Database Service (RDS).

- Amazon Aurora supports Postgres and MySQL
  - Compared to RDS running a MySQL database, Aurora MySQL has 5x more performance
  - Compared to RDS running a Postgres database, Aurora Postgres has 3x more performance
- Aurora storage automatically grows in increments of 10GB, up to 64 TB.
- Aurora costs more than RDS (20% more) – but is more efficient
- Not included into Free Tier

Aurora databases are used for OLTP (Online Transaction Processing)

<p align="center" width="100%"><img src="assets/aurora.jpg" alt="aurora" width="400"/></p>

## Amazon Elasticache

Is used to get a Redis or Memcached managed database.

- Caches are in-memory databases with high performance, low latency
- Cache databases Helps reduce load off databases for read intensive workloads, instead of use the repetitive query hitting the database, we can get common responses from our cache.
- Very readily available, easy accessible and they can relieve the pressure on main database by returning common results.
- AWS takes care of OS maintenance / patching, optimizations, setup, configuration, monitoring, failure recovery and backups.
- Keywords: In-memory database
- Architecture example:

<p align="center" width="100%"><img src="assets/aurora.jpg" alt="aurora" width="400"/></p>

## Amazon DynamoDB

DynamoDB is a fully managed and High Available NoSQL Key/Value Database with replications across 3 AZs.

> Amazon DynamoDB is a key-value and document database that delivers single-digit millisecond performance at any scale. It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications. DynamoDB offers flexible schema and can easily handle unstructured data.

- Scales to massive workloads, distributed “serverless” database (We don't need to manage any server related to this database)
- Millions of requests per seconds, trillions of row, 100s of TB of storage
- Fast and consistent in performance
- Single-digit millisecond latency – low latency retrieval
- Integrated with IAM for security, authorization and administration
- Low cost and auto scaling capabilities
- Keywords: Serverless, low-latency and single digit millisecond.
- High Available by default (EFS is high available as well)

<p align="center" width="100%"><img src="assets/dynamodb.jpg" alt="dynamodb" width="300"/></p>

### Amazon DynamoDB Accelerator - DAX

Amazon DynamoDB Accelerator is a in-memory cache for DynamoDB and it is fully managed by AWS.
It has 10x performance improvement

- single digit millisecond latency to `microseconds` latency when accessing tables.
- Secure, highly available and high scalable

Main difference between DAX and Elasticache: DAX is used only with DynamoDB while Elasticache is used with another databases.

- Architecture example:

```
Application <-R/W-> DynamoDB Accelerator (DAX) <-R/W-> DynamoDB
```

## Amazon Redshift

Based on Postgres database, but this one is not used to `OLTP - Online Transaction Processing`, this one is used to `OLAP - Online Analytical Processing`, this type of database is for analytics and data warehousing.

Usually the exam ask what kind of database is used for analytics and data warehousing, so Amazon Redshift is the answer.

- Load data once every hour, not every second.
- 10x performance compared to others data warehouses, scale to PBs of data.
- The data is stored in Columns (columnar storage of data)
- Massive Parallel Query Execution (MPP)
- High Availability
- Pay as you go, based on the launched instances
- Has SQL interface to perform queries.
- Integrated with BI tools such as Amazon Quicksight and Tableau.
- Redshift does not support storing unstructured data.

## Amazon Elastic MapReduce - EMR

EMR stands to Elastic MapReduce and it is a tool to perform big data processing and analysis by provisioning Hadoop Clusters.

- EMR helps us to create Hadoop Clusters (it can be hundreds of EC2 instances) to do big data processing and analysis
- Supports Apache Spark, HBase, Presto, Flink and others.
- EMR takes care of provisioning EC2 Instances and the configurations
- Autoscaling Groups integration
- Spot instances integration

Use Cases: data processing, big data, machine learning, web indexing...

## Amazon Athena

Amazon Athena is a serverless database to perform SQL queries on S3.

- It does not need a server to run, and for this, we don't need manage any infrastructure, so we pay only per executed query.
- Pay per query, not for database
- Used to query data in S3
- Outputs are stored in S3
- Secured by IAM

Use cases: One-time SQL queries, serverless queries on S3, log analytics.

## Amazon Quicksight

It is a serverless learning-powered Business Intelligence (B.I) service to create interactive dashboards.

Fast, auto scalable, embeddable, with per-session pricing;

Use cases: Business Analytics, Building Visualizations, Perform ad-hoc analysis, get insights using data

Fully integrated with AWS DBs: RDS, Aurora, Athena, S3, DynamoDB, Redshift

## Amazon DocumentDB

Amazon DocumentDB is the AWS implementation of MongoDB. It is a NoSQL database and optimized to run in cloud.

- It is used to store, query and index JSON data.
- Fully managed database, highly available with replication across 3 AZs.
- Storage grows automatically from 10gb to 64TB.
- Automatically scales to workloads with millions of requests per second.

## Amazon Neptune

Amazon Neptune is a fully managed Graph Database.

- Neptune is highly available with replication across 3 AZs and it can have upp to 15 read replicas.
- Build and run applications working with highly connected
  datasets
- Optimized to run complex and hard queries
- Can store up to billions of relationships and query graphs with milliseconds of latency

Use cases for Amazon Neptune:

- Social network (users interactions and connections)
- Knowledge Database (such as wikipedia)
- Fraud detection
- Recommendations Engines (users who bought product X also bought this other Y product)

## Amazon QLDB

QLDB stands to Quantum Ledger Database, so Amazon QLDB is a database service for Ledger and Store securely financial data and transactions.

- It is completely immutable system, so no entry can be removed or modified, it is all encrypted and all entries have logs and data to audit.
- Provides a centrally verifiable history of all changes made to data residing in it
- Used to review history of all the changes made to your application data over time.
- QLDB is a fully managed database and is highly available with replication across 3 AZs.
- 2-3x better performance than common ledger blockchain frameworks.
- In QLDB there is no concept of decentralization. So QLDB has a central and unique point of control while `Amazon Managed Blockchain` use this kind of concept.

Ledgers are typically used to record a history of economic and financial activity in an organization. Many organizations build applications with ledger-like functionality because they want to maintain an accurate history of their applications' data, for example, tracking the history of credits and debits in banking transactions, verifying the data lineage of an insurance claim, or tracing the movement of an item in a supply chain network. Ledger applications are often implemented using custom audit tables or audit trails created in relational databases.

## Amazon Managed Blockchain

Blockchain makes it possible to execute financial transactions between multiple parties, without the need of a central authority. With Amazon Managed Blockchain is possible to join public blockchain networks or create your own private network.

> Amazon Managed Blockchain is a fully managed service that allows you to join public networks or set up and manage scalable private networks using popular open-source frameworks. Amazon Managed Blockchain eliminates the overhead required to create the network or join a public network and automatically scales to meet the demands of thousands of applications running millions of transactions.

- It is compatible with Ethereum and HyperLedger Fabric.
- While QLDB is a ledger database purpose-built for customers who need to maintain a complete and verifiable history of data changes in an application that they own and manage in a centralized way, QLDB is not a blockchain technology. Instead, blockchain technologies focus on enabling multiple parties to transact and share data securely in a decentralized way; without a trusted, central authority. Every member in a network has an independently verifiable copy of an immutable ledger, and members can create and endorse transactions in the network.

## Amazon DMS

Amazon Data Migration Service is a service to migrate data from one database to another. As we could see, exists multiple types of databases, so if we need to migrate data from other types we use DMS.

- DMS Runs into an EC2 instance, and this kind of resource only runs while the migration is running.
- With DMS we can quickly and securely migrate databases to AWS

it supports Homogeneous Migrations and Heterogeneous Migrations.

- The homogeneous migrations are to same type of database: Ex. Oracle to Oracle.
- The heterogenous migrations are to different types of database: SQL Server to Oracle
- We can also migrate to Kinesis Stream Data.

<p align="center" width="100%"><img src="assets/dms.jpg" alt="dms" width="200"/></p>

## Amazon Glue

Amazon Glue is a serverless and fully managed service to perform ETL (Extract Transform and Load). With ETL we can connect to multiple databases to extract data, transform according our needs and load into another database to add the analysis part.

- Example of usage

<p align="center" width="100%"><img src="assets/glue.jpg" alt="glue" width="500"/></p>

Glue also has a another service called `Glue Data Catalog`. This service catalogs all the datasets in AWS Infrastructure and it keeps available with all the information about the dataset, such as table names, columns names, types, etc.

## Summary

- Relational Databases - OLTP: RDS & Aurora (SQL)
- Differences between Multi-AZ, Read Replicas, Multi-Region
- In-memory Database: ElastiCache
- Key/Value Database: DynamoDB (serverless) & DAX (cache for DynamoDB)
- Warehouse - OLAP: Redshift (SQL)
- Hadoop Cluster: EMR
- Athena: query data on Amazon S3 (serverless & SQL)
- QuickSight: dashboards on your data (serverless)
- DocumentDB: “Aurora for MongoDB” (JSON – NoSQL database)
- Amazon QLDB: Financial Transactions Ledger (immutable journal, cryptographically verifiable)
- Amazon Managed Blockchain: managed HyperLedger Fabric & Ethereum blockchain
- Glue: Managed ETL (Extract Transform Load) and Data Catalog service
- Database Migration: DMS
- Neptune: graph database


# Serverless

Serverless is a new paradigm in which the developers don’t have to manage servers anymore, it is just deploy and not need to worry about where it is.

Initially, serverless was pioneered by AWS with AWS Lambda, but now Serverless is the concept of fully managed services.

**Important**: Serverless does not mean that there are no servers! They exists but you don't have to worry about anything about them (no manage, provision or even see where are they)

## AWS Serverless Services

AWS have multiple serverless services such as:

- S3
- DynamoDB
- Amazon Aurora
- Amazon Athena
- Fargate
- AWS Lambdas

Read more [here](https://medium.com/awesome-cloud/aws-serverless-services-and-serverless-computing-in-aws-a1298ace0e3c)

## AWS Lambdas

AWS Lambdas are serverless functions executions.
Comparing to an EC2 instances: In EC2 instance we have virtual serves in the cloud, they are limited by RAM and CPU and they keep running continuously. When Scaling it means to add more compute power or more servers.

When we are talking about AWS Lambdas we don't have servers to manage, we just have functions!

- Functions executions
- Limited by time (made to short executions, max 15 minutes)
- Run on demand
- Scaling automatically

AWS Lambdas has multiples benefits:

- Integrated with the AWS Services
- Event driven: Functions are invoked when an specific event happens. They are reactive.
  - Lambda can be configured to execute code in response to events, such as changes to Amazon S3 buckets, updates to an Amazon DynamoDB table, or custom events generated by your applications or devices.
- Preprocessing: Lambda can be used to run preprocessing scripts to filter, sort or transform data before sending it to downstream applications/services.
- Integrated with many programming languages (JS/NodeJS, Java, Python, Ruby, etc.)
- Integrated with cloud watch to monitoring
- Easy to get more resources per functions
- Increase RAM also increase CPU and network.

Lambdas can also run containers with **Lambda Container Image**, but they need to be created with the exactly specifications AWS Lambdas needs (must implement the Lambda Runtime API). It is not very common the use, the best case for using container are with ECS or Fargate.

Lambdas use cases:

- Thumbnails: Receive an image into S3 (this will trigger a lambda) and the lambda will create a small version of the image to store again into S3 and will store the metadata of the image into dynamoDB.
<p align="center" width="100%"><img src="assets/lambda.jpg" alt="lambda" width="500"/></p>

- CRON Jobs: Schedule to run a script (with Cloud Watch Event Bridge). This will trigger the lambda every one hour to perform a task.
<p align="center" width="100%"><img src="assets/cron.jpg" alt="cron" width="300"/></p>

**Pricing**:

- Invocations
  - Free tier first 1.000.000 of lambdas invocations
  - $ 0.20 per 1 million of requests (after free tier)
- Compute Time/Duration
  - 400.000 GB/Seconds of compute time per month
    - if the function consume 1GB of RAM, you can use it for 400.000 seconds
    - if the function consume 128MB of RAM, you can use it for 3.200.000 seconds
  - After that you pay $1.00 for 600.000 GB/Seconds
- More pricing [examples](https://aws.amazon.com/pt/lambda/pricing/)

## Amazon API Gateway

Amazon API Gateway is serverless HTTP API, a fully managed service for developers to easily create, publish, maintain, monitor and secure APIs.

With API gateway we can allow external request on services that are not exposed directly. API Gateway will proxy a request into a service with all the needed security and scale.

- Fully Scalable and Serverless
- Supports REST APIs and Websocket APIs
- Supports security, authentication, API Keys, monitoring
- Can be configured to send data directly to Amazon Kinesis Data Stream
- Can call AWS Lambda functions to create a front-door for a serverless app.

API gateway example:
A client create a item in your website, your website saves it on dynamo with this structure:

<p align="center" width="100%"><img src="assets/api-gateway.jpg" alt="api-gateway" width="500"/></p>

Your site calls api gateways through your Rest API, then api gateway will proxy the request to the Lambda function and this lambda will insert the register into dynamoDB.

## AWS Batch

This [AWS Batch](../other-services/README.md) is serverless if is running with Fargate

## Summary

- Lambda is Serverless, Function as a Service, seamless scaling, reactive and can runs functions up to 15 minutes
- In lambda we are billed by Invocations and by Time running x RAM
- API Gateway: expose Lambda functions and other AWS services as HTTP API
- AWS Batch: Is serverless when running with Fargate


# Other Compute Services

## AWS Batch

AWS Batch is fully managed service to batch processing at any scale. With this service we can run 100.000s of batch jobs on AWS.

- Batch Jobs are jobs with an start and a end pre-determined, it is the opposite of streaming jobs that has no end. (e.g. from 13pm to 15pm)
- Batch Jobs are defined as Docker Images and Run on ECS
- AWS Batch will dynamically launch EC2 Instances or Spot Instances to accommodate the batch jobs.
- AWS Provision the right amount of memory and compute processing to each job.
- Cost optimization and no worry about create the infra.

<p align="center" width="100%"><img src="assets/batch.jpg" alt="drawing" width="700"/></p>

## AWS Batch vs Lambda

**Lambda:**

- Lambda is limited by time
- Has limited runtime (programming languages)
- Limited disk space
- Serverless

**AWS Batch**:

- No time limit
- Any runtime as long it is packed as a docker image (any container with any programming language)
- Storage of the Instance (EC2 EBS Volume or Instance Store)
- Is a managed service (not serverless because it need EC2 instances)

## Amazon Lightsail

Amazon Lightsail is a standalone service for Virtual servers, storage, databases, and networking for users that are not used to cloud services/no cloud experience.

- Low and predictable prices
- Simple alternative to EC2, RDS, ELB, EBS, Route 53.
- Great for beginners with cloud
- Setup monitoring and notifications
- Use cases:

  - Simple web apps (has templates for nodejs, LAMP, nginx, MEAN)
  - Websites (Wordpress, Magento, Plesk)
  - Dev and Test environment

- Has high availability but not have any auto-scaling
- It has limited integrations with AWS Services

---

• Batch: run batch jobs on AWS across managed EC2 instances or it can be Serverless if running with Fargate
• Lightsail: predictable & low pricing for simple application & DB stacks


# Deploy and Managing Infrastructure at Scale

In this section we are going to understand how to deploy our workload into AWS

- [Cloud Formation](#cloud-formation)
- [Elastic Beanstalk](#elastic-beanstalk)
- [AWS Cloud Development Kit](#aws-cloud-development-kit)
- [AWS CodeDeploy](#aws-codedeploy)
- [AWS CodeCommit](#aws-codecommit)
- [AWS CodeBuild](#aws-codecommit)
- [AWS CodePipeline](#aws-CodePipeline)
- [AWS CodeArtifact](#aws-CodeArtifact)
- [AWS CodeStar](#aws-CodeStar)
- [AWS Cloud9](#aws-Cloud9)
- [AWS Systems Manager](#aws-systems-manager)
- [AWS OpsWorks](#aws-opsWorks)

## Cloud Formation

Cloud Formation is a Declarative way to deploy our resources into AWS. It is used when you need to create and repeat an architecture in different environments, regions or AWS accounts

With cloud formation you can "say": I want a S3 Bucket, I want an EC2 instance, i want a EBS as storage to that instance and so on. Cloud formation creates everything in the right order and with the exact configuration;

Infrastructure as a Service (IaaS):

- Nothing is created by the console, it is code
- Changes can be reviewed as code review and storage in repositories

Costs:

- Each deploy resource is tagged (easy to identify and understand costs)
- You can estimate costs of resources by using a template
- Savings strategies: example: In DEVL environment destroy everything at midnight and build it up again at 7am

Productivity:

- Ability to destroy and re-create an infrastructure on the cloud on the fly
- Automated generation of Diagram for your templates!
- Declarative programming (no need to figure out ordering and orchestration)
- Leverage existing templates on the web!
- Leverage the documentation
- Supports (almost) all AWS resources

We can also use the CloudFormation Stack Designer: here we can see all the resources as a Diagram and we can see the relations between the components.

## Elastic Beanstalk

Elastic Beanstalk (EB) is a developer centric view of deploying an application on AWS. It is a Platform as a Service (PaaS). There is no additional charge for Elastic Beanstalk. You pay only for the underlying AWS resources that your application consumes and you can quickly deploy and manage applications in the AWS Cloud without having to learn about the infrastructure that runs those applications.

> AWS Elastic Beanstalk is an easy-to-use service for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS. Simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring. At the same time, you retain full control over the AWS resources powering your application and can access the underlying resources at any time. There is no additional charge for Elastic Beanstalk - you pay only for the AWS resources needed to store and run your applications.

Usually developers face a few problems dealing with AWS, but they just want to deploy the code

- Managing Infrastructure
- Configuration of databases, load balancers
- Scaling concerns

Most of the web apps have a similar architecture (ELB + ASG). With Beanstalk we can deploy using all these features but in one view, with full control of the application. You worry about the code, only.

It is a Managed Service

- Instances Configuration are made by beanstalk
- Deployment strategies are configured and made into beanstalk (Internally Beanstalk create a deployment into CloudFormation)
- Capacity Provisioning
- Load Balancing and Auto Scaling
- Application Monitoring and health monitoring (Health agent pushes metrics to cloudwatch, check the app health and publishes health events)

It Support many languages and platforms: Java, Go, NodeJS, Docker or your own platform.

Three Architecture Models:

- Single Instance deployment (good for devl environment)
- LB + ASG: Great for production and pre-production web applications
- ASG only: Great for non-web apps in production (workers)

Difference between CloudFormation and Beanstalk

- CloudFormation is IaaC and you can deploy any AWS Services and integrations
- Beanstalk is PaaS and it uses CloudFormation to deploy the Web Applications and you just need to worry about your code.

## AWS Cloud Development Kit

Define our infrastructure by using a preferred programming language. The code is compiled into a CloudFormation template (JSON/YAML).

- You can therefore deploy infrastructure and application runtime code together
  - Great for Lambdas, Docker containers (ECS/EKS)

<p align="center" width="100%"><img src="assets/cdk.jpg" alt="cdk" width="600"/></p>

In this example we build our CDK Application using our language defining resources, and the CDK CLI will transform to a CloudFormation template to be deployed by cloudformation.

## AWS CodeDeploy

AWS Code Deploy is a tool to deploy code automatically.

- AWS CodeDeploy is a Hybrid service and can be used in Amazon EC2, AWS Fargate, AWS Lambda, and your on-premises servers.
- It does not use Beanstalk or CloudFormation behind the scenes. It is a different service.
- You must first create the servers/instances (configured) to CodeDeploy run
- By deploy code we can understand upgrade versions of our software automatically.

## AWS CodeCommit

Is a way to store the code into a Git AWS Repository. It is a competitor to GitHub.
With AWS CodeCommit we can create multiple repositories, we can easily share code into our organization and keep the versions.

- The code is automatically versioned
- It is fully managed
- Scalable & Highly Available
- Private, Secured, Integrated with AWS

## AWS CodeBuild

You can build you code into AWS. It means it can compiles the source code, run tests, and produce the final package.

- The package that is produced can be deployed (for CodeDeploy for example)
- Fully Managed and Serverless
- Scalable and Highly Available
- You pay only for the time the package is being built

<p align="center" width="100%"><img src="assets/code-build.jpg" alt="code-build" width="500"/></p>

## AWS CodePipeline

With AWS Code Pipeline we can orchestrate our deployment steps
Usually in our pipelines we Get our code, test, build, provisioning servers and deploy. With CodePipeline we can do it. It is a CI/CD tool.

- It is fully managed
- Compatible with CodeCommit, CodeBuild, CodeDeploy, Elastic Beanstalk, Cloud Formation, GitHub and others providers + have custom plugins.
- CodePipeline uses Amazon CloudWatch Events to detect changes in CodeCommit repositories used as a source for a pipeline.

Example of usage

<p align="center" width="100%"><img src="assets/code-pipeline.jpg" alt="code-pipeline" width="500"/></p>

## AWS CodeArtifact

AWS CodeArtifact is a Artifact Management service to store, publish and share software packages used in development processes.

- secure, scalable and fully managed
- It is a place to store the code dependencies
- Integrated with multiple Artifacts (Maven, Gradle, npm, yarn, twine, pip, and NuGet)
- Developers and CodeBuild can then retrieve dependencies straight from CodeArtifact

## AWS CodeStar

It is a unified UI to manage software development activities in one place. It is a central service to development that allows a quick start using AWS Tools.
It gives you a dashboards with integration with CodeCommit, CodeBuild, CodePipeline, CodeBuild, etc.

- Each CodeStar project includes development tools, including AWS CodePipeline, AWS CodeCommit, AWS CodeBuild, and AWS CodeDeploy, that can be used on their own and with existing AWS applications
- You can use AWS CodeStar and AWS Cloud9 to develop, build, and deploy a serverless web application

# AWS Cloud9

It is a Cloud IDE into AWS, it is a code editor running directly in the browser.

- Classic IDEs (such as IntelliJ, VSCode) you need to install in your computer
- With Cloud IDE you don't need to install, just need internet connection and access the IDE
- Cloud9 allows work collaboration (pair programming) in real-time

## AWS Systems Manager

AWS System Manager (SSM) is a Hybrid service to manage EC2 Instances and On-Premise systems at scale. Works with Linux and Windows. With Systems Manager we can get operational insights of its resources to quickly identify any issues that might impact applications using those resources

> AWS Systems Manager allows you to centralize operational data from multiple AWS services and automate tasks across your AWS resources. You can create logical groups of resources such as applications, different layers of an application stack, or production versus development environments.
> With Systems Manager, you can select a resource group and view its recent API activity, resource configuration changes, related notifications, operational alerts, software inventory, and patch compliance status. You can also take action on each resource group depending on your operational needs. Systems Manager provides a central place to view and manage your AWS resources, so you can have complete visibility and control over your operations.

AWS SSM is basically a service to patch our fleet of instances/servers or even run commands in all of them.

- We can understand the status get insights of our infrastructure
- has multiple products inside this service
- Most popular features:
  - Patching automation for enhanced compliance
  - Run commands across an entire fleet of servers
  - Store parameter configuration with the SSM Parameter Store

How SSM Works:

- We need to install the SSM agent onto the systems we control (Each EC2 Instance or On-Prem Servers)
  - Installed by default on Amazon Linux AMI & some Ubuntu AMI
  - SSM Agent installed report to SSM Service
- If an instance can’t be controlled with SSM, it’s probably an issue with the SSM agent!
- Thanks to the SSM agent, we can run commands, patch & configure our servers

## AWS OpsWorks

It is another Hybrid Service to manage repetitive actions in our servers. it is a managed Chef & Puppet of AWS.

To understand it, we need to understand two tolls before: `Chef & Puppet`: Chef & Puppet help you perform server configuration automatically by code, or repetitive actions related to your servers.

- AWS OpsWorks is an alternative to AWS SSM, but this one, you only provision standard AWS Resources (EC2, Databases, ELB)
- How it works: Based on a `cookbook` it will provision an architecture to your service, by provisioning ELB, ASG, EC2, Databases and your Application

<p align="center" width="100%"><img src="assets/opsworks.jpg" alt="opsworks" width="500"/></p>

## Summary

- CloudFormation: (AWS only)
  - Infrastructure as Code, works with almost all of AWS resources
  - Repeat across Regions & Accounts
- Beanstalk: (AWS only)
  - Platform as a Service (PaaS), limited to certain programming languages or Docker
  - Deploy code consistently with a known architecture: ex, ALB + EC2 + RDS
- Cloud Development Kit (CDK): Define your cloud infrastructure using a programming language
- CodeDeploy (hybrid): deploy & upgrade any application onto servers
- Systems Manager (hybrid): patch, configure and run commands at scale
- OpsWorks (hybrid): managed Chef and Puppet in AWS
- CodeCommit: Store code in private git repository (version controlled)
- CodeBuild: Build & test code in AWS
- CodeDeploy: Deploy code onto servers
- CodePipeline: Orchestration of pipeline (from code to build to deploy)
- CodeArtifact: Store software packages / dependencies on AWS
- CodeStar: Unified view for allowing developers to do CI/CD and code
- Cloud9: Cloud IDE (Integrated Development Environment) with collab


# 🌎 AWS Global Infrastructure

When we are talking about Global Infrastructure we can understand multiple geographic locations. On AWS This could be Regions and/or Edge Locations.

Benefits of Multiple Geographic Locations:

- Decreasing Latency: less latency between communications and packages transfers. (eg. From Brazil to Japan, it surely will have latency), deploy applications closer to the users (Edge Locations)
- Disaster Recovery (DR): Infrastructure is resilient to disasters, fail-over strategies (move to another region)
- Attack Protection: It is harder to attack a distributed infrastructure

AWS Infrastructure consists in:

- Regions: For deploying applications and infrastructure
- Availability Zones: Made of multiple data centers
- Edge Locations (Points of Presence): for content delivery as close as possible to users

Global Services to Decrease Latency and Improve Availability

- [Route53](#route53)
- [CloudFront](#cloudFront)
- [S3 Transfer Accelerator](#s3-transfer-accelerator)
- [AWS Global Accelerator](#aws-global-accelerator)
- [AWS Outposts](#aws-outposts)
- [AWS Wavelength](#aws-wavelength)
- [Summary](#summary)

## Route53

It is a Managed DNS (Domain Name System) of AWS.
Route 53 features are (non exhaustive list): Domain Registration, DNS, Health Checks, Routing Policy

DNS is a collection of rules and records which helps clients understand how to reach servers through URLs. DNS records examples:

```
• www.google.com => 12.34.56.78 == A record (IPv4)
• www.google.com => 2001:0db8:85a3:0000:0000:8a2e:0370:7334 == AAAA IPv6
• search.google.com => www.google.com == CNAME: hostname to hostname
• example.com => AWS resource == Alias (ex: ELB, CloudFront, S3, RDS, etc…)
```

<p align="center" width="100%"><img src="assets/route53.jpg" alt="route53" width="400"/></p>

### Route 53 Routing Policies

Multiples strategies of Routing, expect by the simple route policy, all have health checks and each one different goals:

- **Simple Routing Policy**: A client (web browser) request through an URL and Route 53 resolves and responds an IP. This one does not have health checks.

> With simple routing, you typically route traffic to a single resource, for example, to a web server for your website.

    <p align="center" width="100%"><img src="assets/route53-simple-routing-policy.jpg" alt="route53-simple-routing-policy" width="300"/></p>

- **Weighted Routing Policy**: It is to distribute the traffic across multiple instances: So, a client (web browser) request through an URL and Route 53 resolves and multiples IPs with a weight to each one. And since we have multiple instances, Route 53 perform health checks.

  - Example: 20% of the users will get response from server 1, 30% of the users will get response from server 2, 50% of the users will get response from server 3. It is like a Load Balancing
  <p align="center" width="100%"><img src="assets/route53-weighted-routing-policy.jpg" alt="route53-weighted-routing-policy" width="300"/></p>

- **Latency Routing Policy**: This Latency Routing Policy is made to reduce latency by understanding WHERE is the request coming from, and it will make sure to send a response from the closest server to provide lower possible latency. This one also have health checks.

> This routing policy is used when you have resources in multiple AWS Regions and you want to route traffic to the region that provides the best latency.

- Example: We have an application global application published in South America (Brazil) and Europe (France). Our users are around the globe, so if we receive an request from Argentina it will get the response from the server in South America, the closest one.
<p align="center" width="100%"><img src="assets/route53-latency-routing-policy.jpg" alt="route53-latency-routing-policy" width="300"/></p>

- **Failover Routing Policy**: We have two instances, main instance and failover instance, if the main one fails it will redirect automatically to the failover instance. It performs health checks on the main instance.
<p align="center" width="100%"><img src="assets/route53-failover-routing-policy.jpg" alt="route53-failover-routing-policy" width="300"/></p>

This failover routing policy can be:

**Active-Active failover**

> Use this failover configuration when you want all of your resources to be available the majority of the time. When a resource becomes unavailable, Route 53 can detect that it's unhealthy and stop including it when responding to queries.

**Active-Passive failover**

> Use an active-passive failover configuration when you want a primary resource or group of resources to be available the majority of the time and you want a secondary resource or group of resources to be on standby in case all the primary resources become unavailable. When responding to queries, Route 53 includes only the healthy primary resources. If all the primary resources are unhealthy, Route 53 begins to include only the healthy secondary resources in response to DNS queries.

[AWS Failover types](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-types.html)

## CloudFront

CloudFront is a Content Delivery Network (CDN). It improves the read performance and cache the content into Amazon Edge Locations all around the world. It improves the user experience (less latency).

- Amazon contains 216+ Points of Presence (Edge Locations).
- CloudFront has DDoS protection, Shield and AWS Web Application Firewalls. (You can use AWS WAF web access control lists (web ACLs) to help minimize the effects of a distributed denial of service (DDoS) attack. For additional protection against DDoS attacks, AWS also provides AWS Shield Standard and AWS Shield Advanced.)
- The first call always goes to the Original Location, but after that, the content will cached in the edge location and next requests will be faster for all users.
  - A Static S3 Web Site deployed in Brazil (sa-east-1). A user from china tries to access. The first access on china will be slower because the response comes from the origin, but it will be cached into Edge Location, so next users will get faster responses.

<p align="center" width="100%"><img src="assets/cloudfront.jpg" alt="cloudfront" width="400"/></p>

CloudFront can cache from:

**S3 Bucket**:

- For distributing files and caching them at the edge
- Enhanced security with CloudFront Origin Access Identity (OAI)
- CloudFront can be used as an ingress (to upload files to S3)

<p align="center" width="100%"><img src="assets/cloudfront-s3.jpg" alt="cloudfront-s3" width="400"/></p>

**Custom Origin (HTTP)**

- Any kind of website
- Load Balancer, EC2, S3 Website (Bucket must be enabled as website)
- Any HTTP backend (even on premise)

<p align="center" width="100%"><img src="assets/cloudfront-http.jpg" alt="cloudfront-http" width="400"/></p>

### CloudFront vs S3 Bucket Replication

- In CloudFront we work with all the Edge Locations around the world. The files are cached, but they have a Time To Live (TTL) and they are great for static content that must be available everywhere.

- In S3 Bucket Replication we need to choose a region to replicate the data, and files are updated in near real time. The files are Read Only as well and it is great for Dynamic content (but in a few regions, not all)

## S3 Transfer Accelerator

As we know an S3 Bucket is linked to one region and sometimes we need to transfer files all around the world into a specific Bucket.

With S3 Transfer Accelerator we can speed up the transfer of the file by transferring the file to an AWS Edge Location. This Edge Location will forward the file to the target bucket. This is only used when you need to download or upload files in buckets that are far away of the user.

Amazon S3 Transfer Acceleration enables fast, easy, and secure transfers of files over long distances between your client and an S3 bucket. Transfer Acceleration takes advantage of Amazon CloudFront’s globally distributed edge locations. As the data arrives at an edge location, data is routed to Amazon S3 over an optimized network path.

- Example: We have a bucket in Australia and our user will upload a file in USA. So it will upload into the Edge Location and internally the file will to your bucket using AWS internal network (faster and private)

<p align="center" width="100%"><img src="assets/s3-transfer-accelerator.jpg" alt="s3-transfer-accelerator" width="400"/></p>

## AWS Global Accelerator

Improves global applications availability and performance by using AWS Global Network. Through the Edge Locations it uses the internal network of AWS and it is very faster.

- Leverage the AWS internal network to optimize the route to your application (60% improvement)
- 2 Anycast IP are created for your application and traffic is sent through Edge Locations
- The Edge locations send the traffic to your application

<p align="center" width="100%"><img src="assets/s3-global-accelerator.jpg" alt="s3-transfer-accelerator" width="300"/></p>

### AWS Global Accelerator vs CloudFront

They both use the AWS global network and its edge locations around the world and Both services integrate with AWS Shield for DDoS protection.

**CloudFront** is a Content Delivery Network and it improves the performance of cacheable content (such as images, videos, static files) and the content is served at the edge.

- CloudFront uses Edge Locations to cache content
- CloudFront is designed to handle HTTP protocol
- CloudFront uses multiple sets of dynamically changing IP addresses to route traffic to your origin.
- CloudFront pricing is mainly based on data transfer out and HTTP requests

**AWS Global Accelerator** has no caching, it proxies the packets by using the edge location and the internal network to have more speed. Improves performance for a wide range of applications over TCP or UDP.

- Global Accelerator uses Edge Locations to find an optimal pathway to the nearest regional endpoint.
- Global Accelerator will provide you a set of static IP addresses as a fixed entry point to your applications.
- Global Accelerator Pricing: it charges a fixed hourly fee and an incremental charge over your standard Data Transfer rates, also called a Data Transfer-Premium fee (DT-Premium).
- Global Accelerator is best used for both HTTP and non-HTTP protocols such as TCP and UDP.
- Good for HTTP use cases that require static IP addresses and Good for HTTP use cases that required deterministic, fast regional failover.

## AWS Outposts

With Hybrid Cloud: businesses can keep an server on premises infrastructure alongside a cloud infrastructure, Therefore, in hybrid you usually have to deal two infra by managing them (Cloud and On-Premise). So you have different commands, different instances, etc.

Thinking about it, AWS has release AWS Outposts, which is a physical "Server Rack" that offers the same AWS Infrastructure, APIs and tools to build the applications on Premise the same way wou would do in the cloud.

- AWS will setup and manage “Outposts Racks” within your on-premises infrastructure and you can start leveraging AWS services on-premises
- You are responsible for the Outposts Rack physical security after the installation.

Benefits:

- Low-latency access to on-premises systems
- Local data processing
- Data residency
- Easier migration from on-premises to the cloud
- Fully managed service
- Some services that work on Outposts: EC2, S3, EBS, EKS, ECS, RDS, EMR

<p align="center" width="100%"><img src="assets/aws-outposts.jpg" alt="aws-outposts" width="400"/></p>

## AWS Wavelength

- Wavelength Zones are infrastructure deployments, embedded within the telecommunications providers data centers at the edge of the 5G Networks.

This brings AWS services to the edge of the 5G Networks, allowing services such as EC2, EBS, VPC...

- Ultra-low latency applications through 5G networks
- Traffic doesn’t leave the Communication Service Provider’s (CSP) network
- High-bandwidth and secure connection to the parent AWS Region
- No additional charges or service agreements
- Use cases: Smart Cities, ML-assisted diagnostics, Connected Vehicles, Interactive Live Video Streams, AR/VR, Real-time Gaming, …

<p align="center" width="100%"><img src="assets/aws-wavelength.jpg" alt="aws-wavelength" width="300"/></p>

## Summary

- Route 53: Great to route users to the closest deployment with least latency and good for disaster recovery strategies.
- CloudFront: Replicate part of your application to AWS Edge Locations and cache common requests (less latency)
- S3 Transfer Acceleration: Accelerate S3 Downloads and Uploads
- AWS Global Accelerator: Improve Global Availability and Performance of your apps by using internal AWS networking.
- AWS Outposts: Deploy Outposts Racks in your own Data Centers to extend AWS services
- AWS Wavelength: Ultra-low latency connection to the applications through 5g network. It brings AWS services to the edge by using the 5G.


# 🚦 Cloud Integration

When we start deploying multiple applications, they will inevitably need to communicate with one another. There are two patterns of application communication:
**Synchronous Communications**: An application communicating directly to another application. (Synchronous between applications can be problematic if there are sudden spikes of traffic)

**Asynchronous Communications** It is event driven and an application puts events or notifications in queues/streams and the other systems communicates with the queues if there is anything in there. The applications keeps decoupled from each other. In AWS we use the following services to Cloud Integrations with Asynchronous Communications:

- [Simple Queue Service (SQS)](#simple-queue-service)
- [Simple Notification Service (SNS)](#simple-notification-service)
- [AWS Kinesis](#aws-kinesis)
- [Amazon MQ](#amazon-mq)
- [Summary](#summary)

## Simple Queue Service

First we need to understand how does a queue work: We have producers that generates message and stores it in a queue. Once this message is stored in a queue it can be read by consumers, who will be polling the message and process it, and after finish the processing it will delete the message from the queue.

Simple Queue Service (SQS) is one of the most old AWS Services and it is used to decouple between application tiers.

- Fully Managed and Serverless services + Auto scalable
- By default it keeps the message from 4 to 14 days and there is no limit of messages into the queue.
- Messages are delete after read by consumers
- A System must pool the message
- Messages in a Queue are typically processed by a single consumer
- Consumers share the work to to read messages & scale horizontally.
- The consumer has to poll and pull messages from SQS

In AWS we have two types of Queues:

- Standard: At-least one delivery, no ordering
- FIFO: First In First Out delivery and Exactly-Once processing
  Keywords: Producer and Consumer

  <p align="center" width="100%"><img src="assets/sqs.jpg" alt="drawing" width="500"/></p>

## Simple Notification Service

For this service need to understand PUB/SUB: It has a topic and this topic notify multiple consumers at once (fan out) of different types (such as Lambda, SQS, Email).

In Simple Notification Service (SNS) the publisher only need to send one notification to a Topic and the consumers are subscribed to this topic, you can have as many as you want.

- The “event publishers” only sends message to one SNS topic
- As many “event subscribers” as we want to listen to the SNS topic notifications
- Each subscriber to the topic will get all the messages
- Keywords: Publisher and Subscriber

 <p align="center" width="100%"><img src="assets/sns.jpg" alt="drawing" width="400"/></p>

Difference between SNS and SQS:

**SQS**:

- SQS is distributed queuing service.
- With SQS all the consumers share the messages
- Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. Messages can’t be received by multiple receivers at the same time. Any one receiver can receive a message, process and delete it. Other receivers do not receive the same message later.
- Consumers poll and pull messages from SQS
- Do your system care about an event?

**SNS**:

- SNS is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.
- With SNS each subscriber get ALL the messages
- Processing the same message in multiple ways.
- Do multiple services care about the same event?

## AWS Kinesis

Amazon Kinesis it is Real Time big data streaming.

- It is a Managed service to collect, process and analyze real-time streaming data at any scale.

Kinesis has some known features:

- Kinesis Data Streams: low latency streaming to ingest data at scale from multiple sources at the same time.
- Kinesis Data Firehose: loads streams into another AWS services (such as S3, Elasticache, redshift, etc.)
- Kinesis Data Analytics: perform real-time data analytics using SQL
- Kinesis Video Streams: monitor real-time video streams for analytics or Machine Learning

## Amazon MQ

It is a managed Apache ActiveMQ and RabbitMQ which are services to work with Queue and Notification Topics. The use case is when you are migrating to the cloud, instead of re-engineering the application to use SQS and SNS, we can use Amazon MQ.

- SQS, SNS are “cloud-native” services, and they’re using proprietary protocols from AWS.
- Traditional applications running from on-premise may use open protocols such as: MQTT, AMQP, STOMP, OpenWire, WSS
- Amazon MQ doesn’t “scale” as much as SQS / SNS
- Amazon MQ runs on a dedicated machine (not serverless)
- Amazon MQ has both queue feature (SQS - Queue) and topic features (SNS - Topic)

## Summary

- SQS:
  - Queue service in AWS
  - Multiple Producers, messages are kept up to 14 days
  - Multiple Consumers share the read and delete messages when done
  - Used to decouple applications in AWS
- SNS:
  - Notification service in AWS (Pub/Sub)
  - Subscribers: Email, Lambda, SQS, HTTP, Mobile…
  - Multiple Subscribers, send all messages to all of them
  - No message retention
- Kinesis: real-time data streaming, persistence and analysis
- Amazon MQ: managed Apache MQ in the cloud (MQTT, AMQP.. protocols)

All these services can scale independently from our application!


# 🕐 Cloud Monitoring

- [CloudWatch Metrics](#cloudwatch-metrics)
- [CloudWatch Alarms](#cloudwatch-alarms)
- [CloudWatch Logs](#cloudwatch-logs)
- [CloudWatch Events - EventBridge](#cloudwatch-events---eventbridge)
- [CloudTrail](#cloudtrail)
- [Amazon X-Ray](#amazon-x-ray)
- [Amazon CodeGuru](#amazon-CodeGuru)
- [Service Health Dashboard](#service-health-dashboard)
- [Personal Health Dashboard](#personal-health-dashboard)
- [Cloudwatch vs. CloudTrail vs. Config](#cloudwatch-vs-cloudtrail-vs-config)
- [Summary](#summary)

## CloudWatch Metrics

CloudWatch provides metrics for every services in AWS. A Metric is a variable to monitor (CPU Utilization, NetworkIn…)

- Metrics have timestamps
- Can create CloudWatch dashboards of metrics
- Important Metrics:
  - EC2 instances: CPU Utilization (understanding the need of scale), Status Checks, Network (not RAM)
  - Default metrics every 5 minutes
  - Option for Detailed Monitoring ($$$): metrics every 1 minute
  - EBS volumes: Disk Read/Writes
  - S3 buckets: BucketSizeBytes, NumberOfObjects, AllRequests
  - Billing:Total Estimated Charge (only in us-east-1)
  - Service Limits: how much you’ve been using a service API
  - Custom metrics: we can create our own metrics

## CloudWatch Alarms

Alarms are use to trigger notifications for any metric. The alarms are customizable and we have multiple options (min, max, average, etc.). Alarms have three states: `OK` (green), `INSUFFICIENT_DATA` (yellow), `ALARM` (red).

With CloudWatch Alarms we can:

- Auto Scaling: Scale In/Up or Scale Out/Down EC2 instances to a desired count
- EC2 Actions: stop, terminate, reboot or recover an EC2 instance
- SNS Notifications: send notifications into SNS topics
- Billing Alarms
- Choose a schedule to check metrics and evaluate alarms.

## CloudWatch Logs

With CloudWatch Logs (customizable data of running applications). We can also enables real-time monitoring of logs and adjustable CloudWatch Logs retention (keep the logs for a week, a month, a year)

So, We can collect logs from applications within:

- Elastic Beanstalk: collection of logs from application
- ECS: collection from containers
- AWS Lambda: collection from function logs
- CloudTrail based on filter
- CloudWatch log agents: on EC2 machines or on-premises servers
- Route53: Log DNS queries

By default CloudWatch Logs does not work with EC2 instances, to do so, we need to

- Install CloudWatch Agent into EC2 Instance.
- Create the correct IAM Permissions.
- The agent also works with on-premise (Hybrid agent) so we can collect logs from it as well.
- The cloudwatch agent will communicate and send the logs to our CloudWatch Logs.

## CloudWatch Events - EventBridge

Is a service to do a serverless cron job and work with events within AWS Services.

- **Schedule**: we can create a scheduled script to run every X define period.
- **Event Pattern**: Event rules to react to a service doing an specific action such as:
  - Trigger Lambdas
  - Register notifications into SNS topics

### Amazon EventBridge

Amazon EventBridge is the next evolution of CloudWatch events. Received this new name and replaces CloudWatch Events name. (In the exam it is called EventBridge)

- Has a default event bus, which are Events generated by AWS Services
- Partner Event Bus: Can receive events from SaaS services or applications (Zendesk, DataDog, Segment, Auth0)
- Custom Event Bus:Can create custom event buses
- Schema Models: it a model event schema

> The main difference between CloudWatch Events and EventBus is that EventBus has new features and it a evolutions, so we have the default event bus (aws service) + partner and custom events and schema models.

## CloudTrail

CloudTrail Provides governance, compliance and audit for your AWS Account by storing every single event that happens in AWS Account. CloudTrail is enabled by default!

- Get an history of events / API calls made within your AWS Account by:
  - Console
  - SDK
  - CLI
  - AWS Services
- We Can put logs from CloudTrail into CloudWatch Logs or S3 to preserve logs to more time.
- A trail can be applied to All Regions (default) or a single Region.

If we need to check any action performed into our account, the best place to check first/investigate is CloudTrail.

In CloudTrail we have three types of events:

- **Management Events**: Operations performed on Resources in our AWS Account. By default, trails are configured to log management events and they can be split into two categories (Read Events, don't modify resources and Write Events, may modify resources). Examples:
  - Configuring security (IAM AttachRolePolicy) - Write Event
  - Configuring rules for routing data (Amazon EC2 CreateSubnet) - Write Event
  - Setting up logging (AWS CloudTrail CreateTrail) - Write Event
  - Delete DynamoDB Table (Write Event)
  - Check Policies (IAM Read) - Read Event
- **Data Events**: By default this type of event is not logged because of the high volume, since it works on object level/data level. Examples:
  - Amazon S3 object-level activities (GetObject, DeleteObject) [Read and Write Events]
  - AWS Lambda Function executions (Invoke API) [Read Event]
- **Insight Events**: This type of event is to detect unusual activities in our AWS Account. It works by analyzing the normal management events and creates a base line of what is normal into our account, so it keeps analyzing the WRITE events to detect unusual patterns such as:
  - inaccurate resource provisioning
  - hitting service limits
  - Bursts of AWS IAM actions
  - Gaps in periodic maintenance activity

With Insight Events we can check the anomalies in CloudTrail Console, Store events into S3 and Integrate with EventBridge to perform actions.

<p align="center" width="100%"><img src="assets/cloudtrail.jpg" alt="drawing" width="700"/></p>

**CloudTrail Retention**: By default the events are store for 90 days. To keep the events for longer times, we can log them to S3 Bucket and use Amazon Athena to Query the events. (we can store all events types: Management Events, Data Events and Insights Events)

## Amazon X-Ray

Usually it is more easy to debug monolith applications, because it is almost everything connected and into the same application. When we have distributed systems, microservices, etc, it is more difficult to debug and trace events as a big picture. For this, we have Amazon X-Ray.

With Amazon X-Ray we can have a big picture and a visual analysis of our apps. The advantages of X-Ray are:

- Troubleshooting Performance (bottlenecks)
- Understand Dependencies in microservices architectures
- Pinpoint services issues and review requests behaviors
- Find errors, exceptions and understand throttles
- Measure SLA

## Amazon CodeGuru

A Machine Learning service to Automated Code Reviews and for Application Performance Recommendations.

**CodeGuru Reviewer**: Automated Code Reviews for static code analysis. (development).

- It analysis the code in our repository (code commit, or github).
- Identity critical issues, security vulnerabilities, and hard-to-find bugs.
- Enforce code practices, common coding best practices, resource leaks, security detection, input validation
- Uses machine learning and automated reasoning
- Hard-learned lessons across multiple AWS open-sources repositories
- Supports Java and Python (more incoming)
- Integration with GitHub, CodeCommit and BitBucket

**CodeGuru Profiler**: Visibility/recommendations of application performance during runtime (production).

- It detects the expensive lines of code in pre-prod and once it is deployed it starts measuring and analyzing performance.
- Helps to understand the runtime behavior of application
- Identify and remove code inefficiencies
- Improve application performance (e.g., reduce CPU utilization)
- Decrease compute costs
- Provides heap summary (identify which objects using up memory)
- Anomaly Detection
- Support applications running on AWS or on- premise
- Minimal overhead on application

<p align="center" width="100%"><img src="assets/codeguru.jpg" alt="codeguru" width="700"/></p>

## Service Health Dashboard

It an AWS Website to show the status of all services in all regions of AWS.
https://status.aws.amazon.com/

- Shows all regions, all services health.
- Shows historical information for each day
- Subscribable RSS feed

## Personal Health Dashboard

Amazon PHD (Personal Health Dashboard) is service that provides alerts and remediation guidances to you when AWS has impacting events to a service or part of infrastructure that may impact our resources.

While the Service Health Dashboard displays the general status of AWS services, **Personal Health Dashboard gives you a personalized view into the performance and availability of the AWS services underlying your AWS resources**. It provides proactive notification to help you plan for scheduled activities.

- Keywords: Alert, remediation, proactive, scheduled activities
- https://phd.aws.amazon.com/

## Cloudwatch vs. CloudTrail vs. Config

- Cloudwatch: Think resource **performance** monitoring, events, and alerts.
- CloudTrail: Think **account-specific activity** and audit.
- Config: Think **resource-specific** change history, audit, and compliance.
- Trusted Advisor: real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits and performance improvement.

## Summary

- CloudWatch: Cloudwatch has multiple features for monitoring our apps
  - Metrics: Are the performance indicators of AWS services and billing metrics
  - Alarms: We can create notifications and actions based on metrics
  - Logs: collect log files from services and store/analyse it
  - Events (EventBridge): create schedule jobs and react to events into our account
- CloudTrail: Governance, Compliance and Audit tools with every events that happens into our account
- CloudTrail Insights: Automated analysis of CloudTrail Events
- X-Ray: trace requests and get a big picture/debugging of distributed systems/microservices.
- CodeGuru: automated code reviews and application performance recommendations
- Service Health Dashboard: Dashboard with all AWS services status across all regions.
- Personal Health Dashboard: Status of AWS Services that impact OUR infrastructure and we can create a plan to deal with it.

[UP](#🕐-Cloud-Monitoring)



# 🔐 Virtual Private Cloud - VPC

We need to understand the main concepts of the resources of VPC

- [VPC](#vpc)
- [Subnets](#subnets)
- [Internet Gateway](#internet-gateway)
- [NAT Gateway](#nat-gateway)
- [Network ACL (NACL)](#network-acl)
- [Security Groups](#security-groups)
- [VPC Flow Logs](#vpc-flow-logs)
- [VPC Peering](#vpc-peering)
- [VPC Endpoints](#vpc-endpoints)
- [Site to Site VPN](#site-to-site-vpn) (vpn and goes to public internet)
- [Direct Connect](#direct-connect) (vpn and goes to private internet)
- [Transit Gateway](#transit-gateway)
- [Summary](#summary)

## VPC

VPC stands to Virtual Private Cloud and it is a private network to deploy your resources (regional resource). A VPC is linked to specific region, so we can have multiple VPC.

> Amazon Virtual Private Cloud (Amazon VPC) is a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including the selection of your IP address range, creation of subnets, and configuration of route tables and network gateways. A VPC spans all of the Availability Zones in the Region whereas A subnet spans only one Availability Zone in the Region.

Inside of VPC we have Subnets and CIDR Ranges (allowed IPs)

Sample VPC example:

- We have the AWS Cloud, and AWS Has regions, inside that region we create a VPC. Inside the VPC we create the CIDR ranges to define the allowed IPs and the subnets.
- Our VPC can reach one or more AZs, so we have the subnets, each subnet inside an AZ. Inside Each Subnet, we have Public and Private subnets.
<p align="center" width="100%"><img src="assets/vpc-sample.jpg" alt="drawing" width="500"/></p>

## Subnets

Subnets are partition of our network and is associated to an Availability Zone

- **Public Subnet**: Is a subnet accessible for the internet (we can put, for example, an EC2 Instance). It requires an internet gateway.
- **Private Subnet**: Is a subnet not accessible for the internet (we can put, for example, a database). Our private subnet can have access to the internet by using the NAT Gateway.

To define access to the internet and communication between subnets, we use route tables.

## Internet Gateway

Inside each subnet we can have EC2 instances, For this instances be accessible to the internet, we need to use the Internet Gateway. The internet gateway create a way to our Subnet connect to the internet.

The public subnet will have a route to the internet gateway that is communicating with the internet. As soon we have the internet gateway and a route to it, that makes the subnet a **public subnet**. It is defined at VPC Level.

## NAT Gateway

Works with the **Private Subnet**. By default private subnet does not have access to the internet and cannot be accessed through the internet as well. But if we need to access the internet (for updates to softwares, or something similar) we can use the NAT Gateway.

NAT Gateway is a AWS-Managed service to allow private subnet access the internet while remaining private.

The NAT Gateway need to be created inside the Public Subnet and we create a Route from our Private Subnet to this NAT Gateway and it will be able to get internet connectivity.

### Using Internet and NAT Gateways

Following the same example of sample VPC:

- Inside each subnet we can have EC2 instances, and to allow the public subnet we create the Internet Gateway and create the route to it, and it goes to the internet.
- Inside the private subnet, by default we do not have access to the internet, so to get the access (to update a software into EC2), we need to create a NAT Gateway inside the Public Subnet and create a Route to this NAT Gateway. The NAT Gateway will communicate with Internet Gateway and the internet gateway will perform the access.
<p align="center" width="100%"><img src="assets/gateways.jpg" alt="drawing" width="300"/></p>

## Network ACL

When we are inside the Subnet we have a protection called Network ACL (NACL or Network Access Level).

- NACL is a firewall (Subnet Level) which controls traffic from and to subnet.
- NACL can have ALLOW and DENY rules
- NACL is stateless, this means, the return traffic must be explicitly allowed by rules.
- A NACL contains a numbered list of rules and evaluates these rules in the increasing order while deciding whether to allow the traffic.
- Automatically applies to all instances in the subnets that it's associated with
- The rules include only IP Addresses

## Security Groups

Security Groups are Firewall specific firewall that controls traffic to and from an ENI (Elastic Network Interface) and/or EC2 Instances.

- Can have only ALLOW rules
- Operates at the instance level
- Rules include IP Addresses and other security groups
- Security Groups are Stateful, this means the Return traffic is automatically allowed, regardless of any rules.
- Security Groups evaluate all rules before deciding whether to allow traffic.
- Control of inbound network (from outside to inside the instance)
- Control of outbound network (from instance to outside) - by default, all traffic outbound (from our instance to the rest of the world) is allowed.

## NACL vs Security Groups

In the next image we can see NACL as the first protection layer, at the subnet level, checking every entry on the subnet and if allowed proxies to the next level.

In the next image we can see Security Groups as the second layer of protection, checking if the authorized ip can access the instance, because, we can have cases when an IP is allowed into the subnet, but not into the instance.

<p align="center" width="100%"><img src="assets/nacl-sg.jpg" alt="drawing" width="300"/></p>

The main differences are

Security Group: Operates at instance level, support only allow rules, is stateful (return traffic is automatically allowed, regardless any rules)

NACL: Operates at the subnet level, allow and deny rules, is stateless (return traffic must be explicitly allowed by the rules)

for more details [visit amazon page](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Security.html)

## VPC Flow Logs

VPC Flow logs captures all logs from all network interfaces, so we have:

- VPC Flow logs
- Subnet Flow logs
- Elastic Network Interface Flow logs
- It also captures network information from AWS managed interfaces into the services: Load Balancers, ElastiCache, RDS, Aurora, etc.

With this logs we can monitor and troubleshoot connectivity issues such as: Subnet to the internet, subnet to subnet, internet to subnet.

We can export our logs to S3 Bucket and/or CloudWatch Logs as well.

## VPC Peering

With VPC Peering we can connect two VPCs, privately using AWS Network and make them behave as if they are in the same network.

> A VPC peering connection is a networking connection between two VPCs that enables you to route traffic between them privately. Instances in either VPC can communicate with each other as if they are within the same network. You can create a VPC peering connection between your VPCs, with a VPC in another AWS account, or with a VPC in a different AWS Region.

- This must not overlap CIDR (IP ranges)
- VPC peering is not transitive, this means if we have 3 VPCs, A, B and C, Then we create a VPC peering from A to B, And we create another VPC peering from B to C

  - the connection between A and C is not in the same network, because A and C does not have the peering between them, if we want to connect these two as well, we need to create the VPC peering following the bellow example.

  <p align="center" width="100%"><img src="assets/vpc-peering.jpg" alt="drawing" width="300"/></p>

## VPC Endpoints

Usually when we connect our services we use the public internet, but we have private subnets, there is no reason to make them communicate between the public internet. For example, an EC2 instance inside a private subnet needs to communicate with S3 or Dynamo. We can use the internal AWS network. For this we need to create an VPC Endpoint.

VPC Endpoints allows us to connect to AWS services using a private network instead of the public. We have two types of Endpoints. This gives you enhanced security and lower latency to access AWS services.

> VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection.

**VPC Endpoint Gateway**: Dynamo and S3

- A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service.
  **VPC Endpoint Interface**: All others AWS services
- An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service. Interface endpoints are powered by AWS PrivateLink, a technology that enables you to privately access services by using private IP addresses.

  <p align="center" width="100%"><img src="assets/vpc-endpoints.jpg" alt="drawing" width="300"/></p>

## Site to Site VPN

> AWS VPN - AWS Virtual Private Network (VPN) solutions establish secure connections between on-premises networks, remote offices, client devices, and the AWS global network. AWS VPN is comprised of two services: AWS Site-to-Site VPN and AWS Client VPN. Together, they deliver a highly-available, managed, and elastic cloud VPN solution to protect your network traffic.

Site to Site VPN connects On-Premise servers to our VPC into AWS. The connection is automatically encrypted, but this Site to Site VPN goes over the **public internet**.

We have to configure our VPC with a Virtual Private Gateway (VGW) and our On-Premise server with a Customer Gateway (CGW), then the site to Site VPN will communicate through them,

<p align="center" width="100%"><img src="assets/site-to-site-vpn.jpg" alt="drawing" width="700"/></p>

> AWS Site-to-Site VPN creates a secure connection between your data center or branch office and your AWS cloud resources. This connection goes over the public internet. Site to Site VPN cannot be used to interconnect VPCs.

## Direct Connect

Establish a physical connection between on-premises and AWS as well, but this one is through a **private internet connection**. To do so, we need a physical connection between our server and a AWS partner that provides direct connect. (it is more expansive and takes up to a month to be ready).

- Private, secure and faster
- Expansive
<p align="center" width="100%"><img src="assets/vpn.jpg" alt="drawing" width="300"/></p>

## Transit Gateway

Our Topologies can became very complicated through time, for this we have the transit gateway.

With Transit Gateway we can connect thousands of VPC and on-premises networks together using a central hub to manage it all. This one use a star model (hub-and-spoke).

- One single gateway can peering, multiples connections to multiple VPCs.
- Works with Direct Connect Gateway, VPNs

<p align="center" width="100%"><img src="assets/transit-gateway.jpg" alt="drawing" width="300"/></p>

## Summary

- VPC Structure:
  - VPC: Virtual Private Cloud
  - Subnets: It is tied to an AZ, is a partition of VPC (can be private or public)
- VPC Connectivity:
  - Internet Gateway: at VPC level, allow internet access
  - NAT Gateway: at the public subnet level, to allow access to the internet for the private one.
- VPC Security:
  - Network ACL (NACL): At subnet level, it is a firewall, Stateless, subnet rules for inbound and outbound
  - Security Groups: at instance level, it is a firewall, stateful. subnet rules (only allow rules) for inbound and outbound
  - VPC Flow Logs: Enable logs to all network interfaces of all internet traffic.
- Connect multiple VPCs:
  - VPC Peering: Connect two VPC with non overlapping IP ranges, intransitive
  - VPC Endpoints: For private subnets, Provide private access to AWS Services within VPC (Interface and Gateway [S3 and Dynamo])
- (VPN) Connect VPC with On Premise
  - Site to Site VPN: connect on premises server with our vpc, through VPN using the public internet.
  - Direct Connect: connect on premises server with our vpc, though VPN, using a private connection (needs physical devices)
  - Transit Gateway: Connect thousands of VPCs and on premise servers using a central hub to manage traffic and peering.

[UP](#-virtual-private-cloud---vpc)



# 📝Security and Compliance

- [AWS Shared Responsibility Model](#aws-shared-responsibility-model)
- [AWS Security Token Service](#aws-security-token-service)
- [AWS Shield](#aws-shield) [Standard and Advanced, layer 3 and 4]
- [AWS Web Application Firewall](#aws-web-application-firewall) [WAF, layer 7]
- [AWS Penetration Testing](#aws-penetration-testing)
- [AWS Key Management Service](#aws-key-management-service) [Encryption]
- [AWS CloudHSM](#aws-cloudhsm) [Encryption]
- [Types of Customer Master Keys](#types-of-customer-master-keys) [CMK Encryption]
- [AWS Certificate Manager](#aws-certificate-manager) [Encryption and Certificate]
- [AWS Secrets Manager](#aws-secrets-manager)
- [AWS Artifact](#aws-artifact)
- [Amazon GuardDuty](#amazon-guardduty) [Threat Discovery into account]
- [Amazon Inspector](#aws-inspector) [EC2 Security Assessments]
- [AWS Config](#aws-config) [Record Configuration for resources on AWS]
- [Amazon Macie](#amazon-macie) [protect sensitive data in S3 Bucket]
- [CloudTrail](#CloudTrail) [Audit and compliance tool regarding api calls]
- [AWS Security Hub](#aws-security-hub)
- [Amazon Detective](#amazon-detective) [Root cause]
- [AWS Abuse](#aws-abuse)
- [Root user privileges](#root-user-privileges)
- [Summary](#summary)

## AWS Shared Responsibility Model

AWS responsibility - Security **of the Cloud**:

- Infrastructure (hardware, software, facilities and network)
- Managed Services like S3, DynamoDB, RDS

Customer Responsibility - Security **in the Cloud**:

- For EC2 instance, customer is responsible for management of the guest OS
  (including security patches and updates), firewall & network configuration, IAM
- Encrypting application data

Shared controls:

- Patch Management, Configuration Management, Awareness & Training

### Shared Responsibility Examples:

**AWS Responsibility Examples:**

- Cloud infrastructure management is the responsibility of AWS.
- Ensuring AWS employees cannot access customer data.
- Compliance validation of Cloud infrastructure

**Customer Responsibility Examples:**

- Operating system patches and updates of an EC2 instance
- Enabling data encryption of data stored in S3 buckets

**Shared Responsibility Examples:**

- For abstracted services, such as Amazon S3 and Amazon DynamoDB, AWS operates the infrastructure layer, the operating system, and platforms, and customers access the endpoints to store and retrieve data.

<p align="center" width="100%"><img src="assets/shared-responsibility.jpg" alt="shared-responsibility" width="500"/></p>

RDS examples of shared responsibility

- AWS responsibility:
  - Manage the underlying EC2 instance, disable SSH access
  - Automated DB patching
  - Automated OS patching
  - Audit the underlying instance and disks & guarantee it functions
- Your responsibility:
  - Check the ports / IP / security group inbound rules in DB’s SG
  - In-database user creation and permissions
  - Creating a database with or without public access
  - Ensure parameter groups or DB is configured to only allow SSL connections
  - Database encryption setting

S3 examples of shared responsibility

- AWS responsibility:
  - Guarantee you get unlimited storage
  - Guarantee you get encryption
  - Ensure separation of the data between different customers
  - Ensure AWS employees can’t access your data
- Your responsibility:

  - Bucket configuration
  - Bucket policy / public setting
  - IAM user and roles
  - Enabling encryption

## AWS Security Token Service

AWS Security Token Service (STS) is one of the most important services of AWS. It enables you to create temporary, limited-privileges credentials to access your AWS resources.
Short-term credentials: you configure expiration period.

**Use cases**

- Identity federation: manage user identities in external systems, and provide them with STS tokens to access AWS resources
- Assume Roles
  - IAM Roles for cross/same account access
  - IAM Roles for Amazon EC2: provide temporary credentials for EC2 instances to access AWS resources

<p align="center" width="100%"><img src="assets/sts.jpg" alt="sts" width="300"/></p>

## AWS against DDoS Attack

In a Distributed Denial of Service (DDoS) attack, an attacker uses multiple sources—such as distributed groups of malware infected computers, routers, IoT devices, and other endpoints—to orchestrate an attack against a target. This is a example of how we can get protected into AWS using firewall and other security services.

  <p align="center" width="100%"><img src="assets/ddos.jpg" alt="ddos" width="500"/></p>

- AWS Shield Standard: protects against DDOS attack for your website and applications, for all customers at no additional costs
- AWS Shield Advanced: 24/7 premium DDoS protection
- AWS WAF: Filter specific requests based on rules
- CloudFront and Route 53:
  - Availability protection using global edge network
  - Combined with AWS Shield, provides attack mitigation at the edge

## AWS Shield

> AWS Shield Standard is activated for all AWS customers, by default. For higher levels of protection against attacks, you can subscribe to AWS Shield Advanced. With Shield Advanced, you also have exclusive access to advanced, real-time metrics and reports for extensive visibility into attacks on your AWS resources. With the assistance of the DRT (DDoS response team), AWS Shield Advanced includes intelligent DDoS attack detection and mitigation for not only for network layer (layer 3) and transport layer (layer 4) attacks but also for application layer (layer 7) attacks.

AWS Shield Standard:

- It is a free service available for every AWS Customer and it provides a protection from common attacks such as SYN/UDP floods, reflection attacks and other layer 3 and 4 attacks (tcp/ip). It can be deployed on HTTP friendly services (ALB, API Gateway, CloudFront)

AWS Shield Advanced:

- It is a option DDoS mitigation ($3000 month/organization) and it protects against the most sophisticated attacks on EC2, ELB, CloudFront, Global Accelerator and Route53. It is a high level defense.
- 24/7 access to AWS DDoS response team (DRP)
- Protect against higher fees during spikes of DDoS
- AWS Shield Advanced provides expanded DDoS attack protection for web applications running on the following resources: Amazon Elastic Compute Cloud, Elastic Load Balancing (ELB), Amazon CloudFront, Amazon Route 53, AWS Global Accelerator.

## AWS Web Application Firewall

AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that block common attack patterns, such as SQL injection or cross-site scripting, and rules that filter out specific traffic patterns you define.

- WAF protects our web apps from common web exploit attacks (layer 7, http).
- Define a Web Access Control List (Web ACL):
  - Rules can include IP addresses, HTTP headers, HTTP body or strings
  - protection from common attacks (SQL Injection and Cross-Site Scripting)
  - Size constraints, geo-match (block a few countries)
  - Rate-based rules (count occurrence of events) - this one is against DDoS attacks
- WAF Can be deployed on services that AWS customers commonly use to deliver content for their websites and applications:

  - CloudFront (Global)
  - Application Load Balancer (ALB) (Regional)
  - API Gateway (Regional)
  - AWS AppSync (Regional)

  When we deploy on Global Services such CDN/CloudFront, it will run the rules in all edge locations, this means the unintended traffic will be blocked before reaching the server. And when we deploy on regional services such as ALB, it will run the rules in the region where the traffic is coming from and protects the internet facing resources.

## Penetration Testing

AWS customers are welcome to carry out security assessments or penetration tests against their AWS infrastructure without prior approval for 8 services. For any other simulated events, contact aws-security-simulatedevent@amazon.com.

This kind of testing can be done for 8 services:

- Amazon EC2 instances, NAT Gateways, and Elastic Load Balancers
- Amazon RDS
- Amazon CloudFront
- Amazon Aurora
- Amazon API Gateways
- AWS Lambda and Lambda Edge functions
- Amazon Lightsail resources
- Amazon Elastic Beanstalk environments

And we have some Prohibited Activities such as:

- DNS zone walking via Amazon Route 53 Hosted Zones
- Denial of Service (DoS), Distributed Denial of Service (DDoS), Simulated DoS, Simulated DDoS
- Port flooding
- Protocol flooding
- Request flooding (login request flooding, API request flooding)

[Read more](https://aws.amazon.com/security/penetration-testing/)

## AWS Key Management Service

We have two types of encryptions:

- Encryption at Rest: data stored or archived on a device somewhere (On Hard Disk, S3, RDS, Deep Archive)

- Encryption in Transit (in motion): incoming data, while upload data, while the data are in the network. (Transfer from on-premises to AWS, EC2 to DynamoDB, etc)

<p align="center" width="100%"><img src="assets/encryption.jpg" alt="encryption" width="500"/></p>

Anytime we hear about encryption in AWS it is possible to be most likely KMS (Key Management Service). KMS manages the encryption keys for us.

**Encryption Opt-in**: we can enable encryption for the bellow services. it is optional.

- EBS volumes: encrypt volumes
- S3 buckets: Server-side encryption of objects
- Redshift database: encryption of data
- RDS database: encryption of data
- EFS drives: encryption of data

**Encryption automatically enabled**: theses services has encryption by default, due security requirements:

- CloudTrail logs
- S3 Glacier
- Storage Gateway

## AWS CloudHSM

CloudHSM is a dedicated hardware provisioned by AWS. Compared to KMS which provide a software who manages our keys, CloudHSM is a hardware provisioned by AWS where we manage our own keys.

HSM device is tamper resistant, FIPS 140-2 Level 3 compliance. HSM = Hardware Security Module.

<p align="center" width="100%"><img src="assets/cloudhsm.jpg" alt="cloudhsm" width="500"/></p>

### Types of Customer Master Keys

**Customer Managed CMK:**

- Create, manage and used by the customer, can enable or disable
- Possibility of rotation policy (new key generated every year, old key preserved)
- Possibility to bring-your-own-key

**AWS managed CMK:**

- Created, managed and used on the customer’s behalf by AWS
- Used by AWS services (aws/s3, aws/ebs, aws/redshift)
- When AWS ask if you want to encrypt, it creates one of theses AWS managed CMK

**AWS owned CMK:**

- Collection of CMKs that an AWS service owns and manages to use in multiple accounts
- AWS can use those to protect resources in your account (but you can’t view the keys)

**CloudHSM Keys (custom keystore):**

- Keys generated from your own CloudHSM hardware device
- Cryptographic operations are performed within the CloudHSM cluster

## AWS Certificate Manager

AWS Certificate Manager (ACM) is a service to easily provision, manage, and deploy
SSL/TLS Certificates.

Used to provide in-flight encryption for websites (HTTPS)

- Supports both public and private TLS
  certificates
- Free of charge for public TLS certificates
- Automatic TLS certificate renewal
- Integrations with (load TLS certificates on)
- Elastic Load Balancers
- CloudFront Distributions
- APIs on API Gateway

<p align="center" width="100%"><img src="assets/acm.jpg" alt="acm" width="300"/></p>

## AWS Secrets Manager

It is an AWS service to store secret keys of any type. The secrets are encrypted using KMS.

- With AWS Secrets Manager we have the capability to rotate the secret keys every X days
- We can automate generation of secrets on rotation (uses Lambda)
- It has full integration with RDS (relational databases) and we can store secrets there (such as user and password of the database)

## AWS Artifact

It is not really a service. It is a way to download AWS compliance documentations. Is a Portal that provides customers with on-demand access to AWS compliance documentation and AWS agreements.

- Artifact Reports - Allows you to download AWS security and compliance documents from third-party auditors, like AWS ISO certifications, Payment Card Industry (PCI), and System and Organization Control (SOC) reports
- Artifact Agreements - Allows you to review, accept, and track the status of AWS agreements such as the Business Associate Addendum (BAA) or the Health Insurance Portability and Accountability Act (HIPAA) for an individual account or in your organization
- Can be used to support internal audit or compliance

## Amazon GuardDuty

Intelligent and continuos threat discovery service to protect AWS Account. It uses machine learning algorithms to anomaly detection. We can setup cloudwatch events rules to be notified in case of any anomaly detection. These cloudwatch event rules can trigger lambdas or sns topics.

Input data includes:

- CloudTrail Logs: unusual API calls, unauthorized deployments
- VPC Flow Logs: unusual internal traffic, unusual IP address
- DNS Logs: compromised EC2 instances sending encoded data within DNS queries

<p align="center" width="100%"><img src="assets/guardduty.jpg" alt="guardduty" width="500"/></p>

## Amazon Inspector

Amazon Inspector is an automated security assessment service for EC2 instances. It analyzes the running OS against known vulnerabilities and unintended network access.

- Amazon Inspector must be installed on OS in EC2 Instances. The assessment can run in scheduled time and in target groups.
- After the assessment it sends/provides a report of vulnerabilities.

> Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on AWS. Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices.

> Amazon Inspector security assessments help you check for unintended network accessibility of your Amazon EC2 instances and for vulnerabilities on those EC2 instances.

> Amazon Inspector also offers predefined software called an agent that you can optionally install in the operating system of the EC2 instances that you want to assess. The agent monitors the behavior of the EC2 instances, including network, file system, and process activity. It also collects a wide set of behavior and configuration data (telemetry).

## AWS Config

With AWS Config we can track, audit and record the resources configurations and the compliance of them over time.

- Possibility of storing the configuration data into S3 (analyzed by Athena)
- Example of tracking in AWS Config: Check HTTP port if is public. Require to all SHH port to be restricted.
- We can receive alerts (SNS notifications) for any changes
- Config per-region
- Aggregated across regions and accounts
- View compliance of a resource over time, View configuration of a resource over time and View CloudTrail API calls if enabled

## Amazon Macie

Amazon Macie is a fully managed data security and data privacy service to protect sensitive data in AWS, using machine learning.

Macie helps identify and alert about sensitive data (such as PII, personal identifiable information)

We can customize our own sensitive data types

<p align="center" width="100%"><img src="assets/macie.jpg" alt="macie" width="500"/></p>

## CloudTrail

CloudTrail Track API calls made by users within account. It is part of [Monitoring](../cloud-monitoring/README.md/#cloudtrail) services.

## AWS Security Hub

It is a centralized security service that allows to do security checks across multiple accounts. Integrated dashboards showing current security and compliance status to quickly
take actions.

- Automatically aggregates alerts in predefined or personal findings from various accounts and services within AWS, such as: GuardDuty (Threat discovery), Inspector (EC2 OS security), Macie (Sensitive Data), IAM Access Analyzer, AWS Systems Manager, AWS Firewall Manager, AWS Partner Network Solutions.

To use this service we must first enable AWS Config (Predefine and record rules and resources configurations)

We can integrate with EventBridge events and Amazon Detective.

<p align="center" width="100%"><img src="assets/securityhub.jpg" alt="securityhub" width="500"/></p>

## Amazon Detective

It is a service to identify the root cause of security issues or suspicious activities.

Why do amazon have this service? With GuardDuty, Macie and Security Hub we can identify multiple security issues, but sometime we need a deeper analysis to detect what is causing that problem. So Amazon Detective analyzes, investigates and quickly identify the root cause.

- Use machine learning algorithms and graphs
- Automatically collect data and processes events from VPC Flow Logs, CloudTrail, GuardDuty and create a unified view of it.
- Produces visualizations with details and context to get to the root cause.

## AWS Abuse

It is a way to report suspect acts coming from hosted services that use aws resources. We need to contact the AWS abuse team.

Prohibited and Abusive behaviors:

- Spam – receiving undesired emails from AWS-owned IP address, websites & forums spammed by AWS resources
- Port scanning – sending packets to your ports to discover the unsecured ones
- DoS or DDoS attacks – AWS-owned IP addresses attempting to overwhelm or crash your servers/softwares
- Intrusion attempts – logging in on your resources
- Hosting objectionable or copyrighted content – distributing illegal or copyrighted content without consent
- Distributing malware – AWS resources distributing softwares to harm computers or machines

## Root User Privileges

Root user is the main account registered in AWS. It has complete access to all AWS resources, but we should not use the main account to common tasks, to do so we must create users within our account. But there a few actions allowed ONLY in the root account:

- **Change Account Settings** (name, email, address, root user password, root user access keys)
- View certain taxes invoices
- Close AWS account
- Restore IAM user permissions
- **Change or Cancel the AWS support plan**
- **Register as a seller in the reserved instance Marketplace**
- Configure an Amazon S3 Bucket to enable MFA
- Edit or delete Amazon S3 bucket policy that includes a invalid VPC or VPC endpoint ID
- SignUp to GovCloud

## Summary

- AWS Shared Responsibility Model: AWS security OF the cloud, user security IN the cloud
- Security Token Service (STS): Temporary, limited-privileges credentials to access AWS resources
- DDoS + other attacks protection:
  - AWS Shield: Automatic protection against DDoS attacks (Standard and Advanced)
  - AWS Web Application Firewall: Firewall to filter incoming requests based on rules. Protection against attacks on layer 7, http
  - AWS Penetration Testing: Allow penetration tests within AWS
- Encryption:
  - AWS Key Management Service: Encryption service and the keys are managed by AWS
  - AWS CloudHSM: Encryption Device. Keys is managed by the user
  - Types of Customer Master Keys: Customer Managed CMK, AWS Managed CMK, AWS Owned CMK and CloudHSM Keys
  - AWS Secrets Manager: Store secrets and encrypt them. (application secrets)
  - AWS Certificate Manager: provision, manage, and deploy SSL/TLS Certificates
- Security:
  - AWS Artifact: Get access to compliance reports such as PCI, ISO, etc
  - Amazon GuardDuty: Threat Discovery on AWS account and Find malicious behavior with VPC, DNS & CloudTrail Logs
  - Amazon Inspector: EC2 only, install the agent to find vulnerabilities on OS.
  - AWS Config: Track and record configuration rules and check if resources are compliant with. (What did my Resource look like in a point of time?)
  - Amazon Macie: Find sensitive data on S3 Buckets.
  - CloudTrail: Track API calls on the account (Compliance, Governance and Audit) - (Who made an API call to modify the resource?)
  - AWS Security Hub: is a central service to security on multiple accounts
  - Amazon Detective: is a service to get the root cause of issues or suspicious activities.
  - AWS Abuse: Report AWS resources used for abusive or illegal purposes
- Root user privileges:
  - Change account settings
  - Change AWS support plan
  - Delete account
  - Register as seller on reserved instance marketplace

[UP](#security-and-compliance)


# 🤖 Machine Learning

Amazon provide multiple services on Machine Learning

- [Amazon Rekognition](#amazon-rekognition): Automate images and videos analysis with ML.
- [Amazon Transcribe](#amazon-transcribe): Transcribe audio to text with deep learning (subtitles)
- [Amazon Polly](#amazon-polly): Text to Voice
- [Amazon Translate](#amazon-translate): translations of languages
- [Amazon Lex](#amazon-lex): Get intent of voice and create bots
- [Amazon Connect](#amazon-connect): Cloud contact center
- [Amazon Comprehend](#amazon-comprehend): Natural Language Processing to understand and interpret texts
- [Amazon SageMaker](#amazon-sageMaker): Environment to developers and data scientists build models
- [Amazon Forecast](#amazon-forecast): Create forecast using machine learning
- [Amazon Kendra](#amazon-kendra): document search service
- [Amazon Personalize](#amazon-personalize): personalized recommendations
- [Summary](#summary)

## Amazon Rekognition

Amazon Rekognition is a fully managed service to work with image and video analysis with deep learning.

With Amazon Rekognition we can fund objects, people, text, scenes, animals in images and videos, using machine learning.

Use cases:

- Facial Analysis and facial search to do user verification and people counting
- Create a database of familiar faces or compare against celebrities
- Labeling
- Content moderation, text detection
- Face detection, search, verification and analysis (gender, age, emotions)
- Pathing (real time analysis is sports games)

## Amazon Transcribe

Amazon Transcribe is a service to automatically convert speech to text using deep learning process called Automatic Speech Recognition (ASR) to covert the text with precision.

Use cases:

- transcribe customer service calls
- automate closed captioning (subtitles)
- generate metadata for media assets to create a fully searchable archive

## Amazon Polly

Amazon Polly is a service to create voice based on a text. Turn text into lifelike speech using deep learning allowing you to create applications that talk

## Amazon Translate

Amazon Translate is a Natural and accurate language translation service.

Amazon Translate allows you to localize content - such as websites and applications - for international users, and to easily translate large volumes of text efficiently.

## Amazon Lex

Same technology of Alexa and it is a Automatic Speech Recognition (ASR) to convert speech to text and it helps to build chatbot and call center bots. We can integrate with any application.

- Natural Language Understanding to recognize the intent of text

## Amazon Connect

It is a omnichannel cloud contact center.

- Receive calls, create contact flows
- Can integrate with other CRM systems or AWS
- No upfront payments, 80% cheaper than traditional contact center solutions

<p align="center" width="100%"><img src="assets/lex-connect.jpg" alt="lex-connect" width="600"/></p>

## Amazon Comprehend

It is a Natural Language Processing (NLP) service. It is fully managed and serverless. Uses machine learning to do understand of text:

- Language of the text
- Extracts key phrases, places, people, brands, or events
- Understands how positive or negative the text is
- Analyzes text using tokenization and parts of speech
- Automatically organizes a collection of text files by topic

Sample use cases:

- Analyze customer interactions (emails) to find what leads to a positive or negative experience
- Create and groups articles by topics that Comprehend will uncover

## Amazon SageMaker

Amazon SageMaker is a fully managed service to developers and data scientists to build ML models. Normally it is a difficult process, we have to provision multiple servers and configurations, with SageMaker it is easier.

- Helps with all the steps of Machine Learning
  - Label data
  - Build models
  - Train and Tune
  - Apply Model and do Predictions

## Amazon Forecast

Amazon forecast is a fully managed service that uses Machine Learning to create forecasts based on data.

Use cases: Product Demand Planning, Financial Planning, Resource Planning...

<p align="center" width="100%"><img src="assets/forecast.jpg" alt="forecast" width="600"/></p>

## Amazon Kendra

It is a Fully Managed **document search service** that uses machine learning. It is used to extract answers from documents (text, pdf, word, etc.)

It indexes the documents and kendra get answers within them.

<p align="center" width="100%"><img src="assets/kendra.jpg" alt="kendra" width="600"/></p>

## Amazon Personalize

It is a full-managed machine learning service to build real time and personalized recommendations. This is the same technology used by Amazon.com

- Integrates into existing websites, applications, SMS, email marketing systems, …
- Implement in days, not months (you don’t need to build, train, and deploy ML solutions)
- Use cases: retail stores, media and entertainment…

<p align="center" width="100%"><img src="assets/personalize.jpg" alt="personalize" width="600"/></p>

## Summary

- Amazon Rekognition: Image and Video analysis with ML
- Amazon Transcribe: Audio to Text
- Amazon Polly: Text to Audio
- Amazon Translate: Translate text from a language to another
- Amazon Lex: Chatbots based on speech to text, build conversational bots
- Amazon Connect: Cloud contact center
- Amazon Comprehend: natural language processing
- Amazon SageMaker: machine learning for every developer and data scientist
- Amazon Forecast: Create forecast using machine learning
- Amazon Kendra: document search service
- Amazon Personalize: A Machine Learning service to build personalized recommendations

[UP](#-machine-learning)


# Account Management and Support

- [AWS Organizations](#aws-organizations)
- [Multi Account Strategies](#multi-account-strategies)
- [Service Control Policy](#service-control-policy)
- [AWS ControlTower](#aws-controlTower)
- [AWS Support Plans](#aws-support-plans)
- [Account Best Practices Summary](#account-best-practices-summary)
- [Billing Summary](#billing-summary)

## AWS Organizations

It is a global service that allows to manage multiple AWS Accounts. The main account is the Master account and the other are the child accounts.

- It has an API to automate the creation of child accounts.
- Since we can have multiple accounts, we can restrict actions within them with SCP (Service Control Policies)

Cost Benefits of AWS Organizations:

- Consolidate Billing across all accounts - which generates a single payment method
- Benefits of aggregated usage (use massive volumes of services generates discounts)
- Shared (pooling) EC2 Reserved Instances for optimal savings.

> AWS Organizations helps you to centrally manage billing; control access, compliance, and security; and share resources across your AWS accounts. Using AWS Organizations, you can automate account creation, create groups of accounts to reflect your business needs, and apply policies for these groups for governance. You can also simplify billing by setting up a single payment method for all of your AWS accounts. AWS Organizations is available to all AWS customers at no additional charge.

## Multi Account Strategies

We have various modes to create accounts in AWS:

- per Department
- per Environment (DEVL, QUAL, PROD)
- based on regulatory restrictions (using Service Control Policy)
- for better isolation (using different VPC per account)
- to have separate per account service limits
- account for loggings
- use Organization Units (OU)

<p align="center" width="100%"><img src="assets/organizational-units.jpg" alt="organizational-units" width="500"/></p>

Besides this strategies, we can also monitor all accounts by:

- using tags standards to billing purposes
- enable CloudTrail in all accounts to monitor all API Calls and send it to central S3 account
- enable cloudwatch logs to central account logging

## Service Control Policy

Service Control Policy (SCP) allows us to create Whitelist or Blacklist to IAM actions. We can apply it on Organization Unit (OU) or Account Level.

- **Does not apply to the root account**
- SCP is applied to all users and roles of the account (even the root user of the account)
  - Example: a rule saying that X account cannot create EC2 instances. Not even the root user of the account can create it.
- Must have EXPLICIT allow to any service, by default nothing is allowed.
- Deny in a higher level has precedence

The use cases for Service Control Policy (SPC):

- Restrict access to specific services
- Enforce PCI compliance by explicitly disabling services

Example of Service Control Policy:

<p align="center" width="100%"><img src="assets/service-control-policy.jpg" alt="service-control-policy" width="700"/></p>

- Here we have our root Organizational Unit (OU) and the master account. The root OU allows all services, and there is a DenyAccessAthena SCP on master account. This deny will not work, because the master account is not affected by SCP.
- Inside our root OU we have a PROD OU that explicitly deny redshift access (DenyRedshiftAccess). It will make all accounts inside it to not have access to redshift, even the Account A that tries to access Redshift with a AuthorizeRedshift SCP. But the higher one is a deny and it has precedence in this case.
- HR OU has no access to redshift and has no access to Lambda (due DenyAWSLambda SCP)
- Finance OU has no access only to Deny

[Examples](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_policies_scps_examples.html) of SCP allowing access to all resources but not to DynamoDB in all accounts.

```JSON
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowsAllActions",
      "Effect": "Allow",
      "Action": "*",
      "Resource": "*"
    },
    {
      "Sid": "DenyDynamoDB",
      "Effect": "Deny",
      "Action": "dynamodb:*",
      "Resource": "*"
    }
  ]
}
```

## AWS ControlTower

AWS ControlTower is a easy way to setup and govern a secure and compliant multi-account AWS environment based on best practices. Control Tower is an AWS native service providing a pre-defined set of blueprints and guardrails to help customers implement a landing zone for new AWS accounts.

With ControlTower we can:

- automate the setup of the environment with a few clicks
- automate ongoing policies applying guardrails
  - detect policy violations
- monitor compliance in a dashboard.
- automatically sets up AWS Organizations to organize accounts and implement SCPs (Service Control Policies)
- it creates three shared accounts: Master Account, Log Archive account and Audit account

## AWS Support Plans

AWS Has multiple types of customer support plans, the pricing of each one is variable as the use.

<p align="center" width="100%"><img src="assets/support-plans-pricing.jpg"  alt="support-plans-pricing" width="400"></p>

**Basic Support:**

- Free for all customers
- Has Customer Services & Communities - 24x7 access to customer service, documentation, whitepapers and support forums.
- In **Trusted Advisor** we have access to the seven core checks and guidance to provision your resources following the best practices to increase performance and security.
- In **AWS Personal Health Dashboard** we have a personalized view of the health of AWS Services and we get alerts when something is going to impact our infrastructure.
- This plan **does not support any architectural guidance**.

**Developer Support:**
AWS recommends Developer Support if you are testing or doing early development on AWS and want the ability to get email-based technical support during business hours as well as general architectural guidance as you build and test. You do not get access to Infrastructure Event Management with this plan. This plan only supports general architectural guidance.

- All the basic plan +
- Business hours email access to Cloud Support Associates
- Unlimited cases and we have 1 primary contact in AWS
- Depending on Severity of the problem the response time may be variable:
  - General architectural guidance up to 24 business hours
  - Systems impaired up to 12 business hours

**Business Support:**
AWS recommends Business Support if you have production workloads on AWS and want 24x7 phone, email and chat access to technical support and architectural guidance in the context of your specific use-cases. You get full access to AWS Trusted Advisor Best Practice Checks. You also get access to Infrastructure Event Management for an additional fee.

- All the Basic + Support +
- 24/7 phone, email and chat access to Cloud Support Engineers
- Trusted Advisor - Full set of checks + API access
- Unlimited Cases / Unlimited contacts
- Infrastructure Event Management for an additional fee
- Depending on Severity of the problem the response time may be variable:
  - General architectural guidance up to 24 business hours
  - Systems impaired up to 12 business hours
  - Production system impaired up to 4 business hours
  - Production system down < 1 business hour

**Enterprise Support:**
AWS Enterprise Support provides customers with concierge-like service where the main focus is helping the customer achieve their outcomes and find success in the cloud. With Enterprise Support, you get 24x7 technical support from high-quality engineers, tools and technology to automatically manage the health of your environment, consultative review and guidance based on your applications, and a designated Technical Account Manager (TAM) to coordinate access to proactive/preventative programs and AWS subject matter experts. This plan supports architectural guidance contextual to your application.

- All the business support features +
- Access to a **Technical Account Manager (TAM)**
- **Concierge Support Team** for billing and account best practices
- **Infrastructure Event Management** included
- Well architected and Operations Reviews
- Depending on Severity of the problem the response time may be variable:
  - General architectural guidance up to 24 business hours
  - Systems impaired up to 12 business hours
  - Production system impaired up to 4 business hours
  - Production system down < 1 business hour
  - Business-Critical system down < 15 minutes to response

## Account Best Practices Summary

- Operating with multiple accounts use AWS Organizations
- Restricting power into the account use Service Control Policy
- Setup multiple accounts with best-practices with AWS ControlTower
- Use tags and Cost allocation tags for easy billing/management
- IAM guidelines: MFA, Password policies, Least privilege principle
- Use Config to record all the resources and configurations and do compliance over time
- Use CloudFormation to deploy the stack across the regions
- Use CloudTrail to track all the api calls in our account
- Trusted Advisor is great tool to get insight to get the best cost optimization and the support plan
- Send Services Logs and Access Logs to S3 or CloudWatch Logs (Maybe have an account just to logging)
- If anything compromises the account: change the root password, delete and rotate all passwords and keys, and get in touch to AWS Support.

[UP](#account-management-and-support)


# AWS Billing

- [AWS Pricing Models](#aws-pricing-models)
  - [Free Services and Free Tier](#free-services-and-free-tier)
  - [EC2 Pricing](#ec2-pricing)
  - [Lambda Pricing](#lambda-pricing)
  - [ECS Pricing](#ecs-pricing)
  - [Fargate Pricing](#fargate-pricing)
  - [S3 Pricing](#s3-pricing)
  - [EBS Pricing](#ebs-pricing)
  - [Database Pricing](#Database-pricing)
  - [CloudFront Pricing](#cloudfront-pricing)
  - [Network Pricing](#network-pricing)
- [Reserved Instances to Cost Optimization](#reserved-instances-to-cost-optimization)
- [AWS Savings Plan](#aws-savings-plan)
- [AWS Compute Optimizer](#aws-compute-optimizer)
- [Billing and Costing Tools](#billing-and-costing-tools)
  - [Estimating costs in the cloud](#estimating-costs-in-the-cloud)
    - [TCO Calculator](#tco-calculator): On-prem to Cloud
    - [AWS Pricing Calculator](#aws-pricing-calculator): Cloud pricing
  - [Tracking costs in the cloud](#tracking-costs-in-the-cloud)
    - [AWS Billing Dashboard](#aws-billing-dashboard): Simple dashboard
    - [Cost Allocation Tags](#cost-allocation-tags): Track by tag
    - [Cost and Usage Reports](#cost-and-usage-reports): The most detailed report
    - [Cost Explorer](#cost-explorer): Visual tool
  - [Monitoring against costs plans](#monitoring-against-costs-plans)
    - [Billing Alarms on CloudWatch](#billing-alarms-on-cloudwatch)
    - [AWS Budgets](#aws-budgets)
- [AWS Trusted Advisor](#aws-trusted-advisor)
- [Summary](#summary)

## AWS Pricing Models

AWS has four pricing models:

- **Pay as you go:** You pay for what you use, remain agile, responsive, meet the scale demands
- **Save when you reserve:** for longer term requirements, you save more when you reserve (such as using databases, ec2 instances). This one minimize risks and we have a predictably manage budgets
- **Pay less by using more:** The more you use, more discount. Based on volume.
- **Pay less as AWS grows:** As AWS grows, they save costs and services gets cheaper, so we are affected by it.

### Free Services and Free Tier

- Free Services: IAM, VPC, Consolidated Billing, DynamoDB (25gb)
- Free Services But you per resources: Elastic Beanstalk, CloudFormation, AutoScaling Groups
- [Free Tier](https://aws.amazon.com/pt/free/): free for a period or volume of use (EC2 t2.micro, S3, EBS)

### EC2 Pricing

On EC2 we are only charged on what we use:

- Number of instances
- Instance configuration:
  - Physical capacity
  - Region
  - OS and software
  - Instance type
  - Instance size
- ELB running time and amount of data processed
- Detailed monitoring

We have multiple types of EC2 Purchasing Options. (more detailed in [EC2 section](../ec2/README.md/#EC2-Instances-Purchasing-Options))

**On-demand instances:**

- Minimum of 60s of use
- Pay per second (Linux) or per hour (Windows)

**Reserved instances:**

- Up to 75% discount compared to On-demand on hourly rate
- 1- or 3-years commitment
- All upfront, partial upfront, no upfront

**Spot instances:**

- Up to 90% discount compared to On-demand on hourly rate
- Bid for unused capacity

**Dedicated Host:**

- On-demand
- Reservation for 1 year or 3 years commitment

**Savings plans** as an alternative to save on sustained usage

### Lambda Pricing

- Pay per call
- Pay per duration (max duration 15 minutes)

### ECS Pricing

- When we use ECS behind the scenes it will get an EC2 instance so, will only pay for the EC2 instance and the resources configured to run our application.

### Fargate Pricing

- When we use Fargate it does not runs for us an EC2 instance, so we don't have to manage nothing about server, it is serverless. We pay for Fargate Launch Type Model which means: CPU and Memory allocated to run the application into the containers.

### S3 Pricing

In S3 we have multiple types of [Storage classes](../s3/README.md/#s3-storage-classes): S3 Standard, S3 Infrequent Access, S3 One-Zone IA, S3, Intelligent Tiering, S3 Glacier and S3 Glacier Deep Archive

In S3 we pay for:

- Number and size of objects: Price can be tiered (based on volume, the more volume more discount)
- Number and type of requests (pay for requests in and out)
- Data transfer OUT of the S3 region (Inbound data transfer in the S3 region is free)
- S3 Transfer Acceleration
- Lifecycle transitions between storage classes
- Similar service: EFS (pay per use, has infrequent access & lifecycle rules)
- Retrieval Fee
  - S3 Standard does not charge any data retrieval fee.
  - S3 Intelligent-Tiering does not charge any data retrieval fee.
  - All other storage classes have a retrieval fee.

### EBS Pricing

In Elastic Block Storage we pay for

- Volume type (based on performance)
- Storage volume in GB per month provisioned
- IOPS:
  - General Purpose SSD: Included
  - Provisioned IOPS SSD: Provisionned amount in IOPS
  - Magnetic: Number of requests
- Snapshots:
  - Added data cost per GB of snapshot per month (The added data storage by EBS Snapshots are added cost in GB per month to EBS pricing. Other EBS pricing factors are: Volume type, Provisioned storage volume, IOPS, etc.)
- Data transfer:
  - Outbound data transfer are tiered for volume discounts
  - Inbound is free

### Database Pricing

- Per hour billing
- Database characteristics:
  - Engine
  - Size
  - Memory class
- Purchase type:
  - On-demand
  - Reserved instances (1 or 3 years) with required up-front
- Backup Storage: There is no additional charge for backup storage up to 100% of your total database storage for a region.

**RDS Pricing:**

- Additional storage (per GB per month)
- Number of input and output requests per month
- Deployment type (storage and I/O are variable):
  - Single AZ
  - Multiple AZs
- Data transfer:
  - Outbound data transfer are tiered for volume discounts
  - Inbound is free
- Reserved Instances are good and more cost-effective (up to 69% discount compared to On-demand pricing, depending on the upfront) for long workloads. You can reserve instances for 1 or 3 years in RDS.

### CloudFront Pricing

- Pricing is different across different geographic regions
- Aggregated for each edge location, then applied to your bill (the more you use in a edge location, bigger the discount)
- Data Transfer Out (volume discount)
- Data in is always free
- Number of HTTP/HTTPS requests

### Network Pricing

- All the traffic inbound traffic is free.
- In same region and same AZ: if we have an EC2 instance that uses the free traffic and we have another instance that communicates with this one, the communication is free using the **private ip**.
- In different AZs communication via **private ip** is $0.01 (cheaper) and via **public ip** is $0.02 (expensive).
- In different regions: $0.02 because of the inter-region communication

<p align="center" width="100%"><img src="assets/network-pricing.jpg" alt="network-pricing" width="500"/></p>

- Use Private IP instead of Public IP for good savings and better network performance
- Use same AZ for maximum savings (but you loose the high availability)

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer. In most cases, there is no charge for inbound data transfer or data transfer between other AWS services within the same region. Outbound data transfer is aggregated across services and then charged at the outbound data transfer rate.

## Reserved Instances to Cost Optimization

The following AWS services support reservations to optimize costs:

- Amazon EC2 Reserved Instances: You can use Amazon EC2 Reserved Instances to reserve capacity and receive a discount on your instance usage compared to running On-Demand instances.
- Amazon DynamoDB Reserved Capacity: If you can predict your need for Amazon DynamoDB read-and-write throughput, Reserved Capacity offers significant savings over the normal price of DynamoDB provisioned throughput capacity.
- Amazon ElastiCache Reserved Nodes: Amazon ElastiCache Reserved Nodes give you the option to make a low, one-time payment for each cache node you want to reserve and, in turn, receive a significant discount on the hourly charge for that node.
- Amazon RDS RIs: Like Amazon EC2 RIs, Amazon RDS RIs can be purchased using No Upfront, Partial Upfront, or All Upfront terms. All Reserved Instance types are available for Aurora, MySQL, MariaDB, PostgreSQL, Oracle, and SQL Server database engines.
- Amazon Redshift Reserved Nodes: If you intend to keep an Amazon Redshift cluster running continuously for a prolonged period, you should consider purchasing reserved-node offerings. These offerings provide significant savings over on-demand pricing, but they require you to reserve compute nodes and commit to paying for those nodes for either a 1- or 3-year duration.

## AWS Savings Plan

AWS Savings Plans is a way to save more money by getting more discounts. And to do so, we need to commit with a amount of dollar per hour during 1 or 3 years. (With upfront, partial upfront and no upfront). This is the easiest way to setup long terms commitments in AWS.

There are two types of savings plans

**EC2 Savings Plan**

- Up to 72% discount compared to On-Demand and we commit to usage of individual instance families in a region (e.g. C5 or M5)
- Regardless of AZ, size (m5.xl to m5.4xl), OS (Linux/Windows) or tenancy

**Compute Savings Plan:**

- Up to 66% discount compared to On-Demand
- Regardless of Family, Region, size, OS, tenancy, compute options
- Compute Options: EC2, Fargate, Lambda

## AWS Compute Optimizer

AWS Compute Optimizer is a service to help save costs of compute services by analyzing the use of each one of them (using machine learning) and sending us recommendations of improvement.

> AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon EC2 instance types, Amazon EBS volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer delivers recommendations for selected types of EC2 instances, EC2 Auto Scaling groups, EBS volumes, and Lambda functions.

- Helps you choose optimal configurations and right-size your workloads (over/under provisioned)
- Uses Machine Learning to analyze your resources’ configurations and their utilization CloudWatch metrics
- Supported resources: EC2 instances, EC2 Auto Scaling Groups, EBS volumes and Lambda functions
- Lower your costs by up to 25%
- Recommendations can be exported to S3

Compute Optimizer calculates an individual performance risk score for each resource dimension of the recommended instance, including CPU, memory, EBS throughput, EBS IOPS, disk throughput, disk throughput, network throughput, and network packets per second (PPS).

- AWS Compute Optimizer provides EC2 instance type and size recommendations for EC2 Auto Scaling groups with a fixed group size, meaning desired, minimum, and maximum are all set to the same value and have no scaling policy attached.
- AWS Compute Optimizer supports IOPS and throughput recommendations for General Purpose (SSD) (gp3) volumes and IOPS recommendations for Provisioned IOPS (io1 and io2) volumes.
- Compute Optimizer helps you optimize two categories of Lambda functions. The first category includes Lambda functions that may be over-provisioned in memory sizes. The second category includes compute-intensive Lambda functions that may benefit from additional CPU power.

## Billing and Costing Tools

AWS Has multiple types of tools to Billing and Cost, and we can split in three types

- Estimating costs in the cloud:
- Tracking costs in the cloud
- Monitoring against costs plans

### Estimating costs in the cloud

First we can estimate the costs in the cloud with TCO Calculator and Pricing Calculator

#### TCO Calculator

TCO stands to Total Cost of Ownership and it is a tool to calculate the cost of moving ownership of on-premises server to the cloud.

> TCO calculator helps to compare the cost of your applications in an on-premises or traditional hosting environment to AWS. AWS helps reduce Total Cost of Ownership (TCO) by reducing the need to invest in large capital expenditures and providing a pay-as-you-go model that empowers to invest in the capacity you need and use it only when the business requires it. Once you describe your on-premises or hosting environment configuration, it produces a detailed cost comparison with AWS. TCO calculator can be used from https://awstcocalculator.com/.

- AWS Helps reduce CAPEX (capital expenditures) and providing a pay-as-you-go model
- The TCO calculators allow you to estimate the cost savings when using AWS and provide a detailed set of reports that can be used in executive presentations.
- It compares all the costs with having a on-premises server vs using AWS infrastructure (Server, Storage, Network, IT Labor)

**This tools is deprecated.**

#### AWS Pricing Calculator

AWS Pricing Calculator is a tool to calculate the pricing of Solutions Architecture on AWS.

Here we can select all the infra we want and understand the billing before start our architecture.

### Tracking costs in the cloud

Now we have tools to track our costs in the cloud: We have: AWS Billing Dashboard, Cost Allocation Tags, Cost and Usage Reports, Cost Explorer

#### AWS Billing Dashboard

AWS Billing Dashboard is a high level tool, but great for an overview of costs in AWS.

- It shows Month-to-Date costs
- Summaries
- Last month cost
- Forecast
- Free tier dashboard to understand the usage of the free tier services.

#### Cost Allocation Tags

Use Cost Allocation Tags to track costs on detailed level and categorize.

The tags are used to organize resources and group them together with these tags in AWS and we can give any name we want. The most common are: name, environment, team.

We can manage it with `Tag Editor`. We can also create Resources Groups in this Tag Editor tool.

- We can use auto generated tags by AWS (prefix `aws`)
- User defined tags (prefix `user`)
- You must activate both AWS generated tags and user-defined tags separately before they can appear in Cost Explorer or on a cost allocation report
- For each resource, each tag key must be unique, and each tag key can have only one value

#### Cost and Usage Reports

Cost and Usage Reports is a tool to dive deeper into our AWS costs and usage of resources.

- This is **the most** detailed report in AWS with the most comprehensive data report available.
- The AWS Cost & Usage Report lists AWS usage for each service category used by an account and its IAM users in hourly or daily line items, as well as any tags that you have activated for cost allocation purposes.
- Can be integrated with Athena, Redshift and Quicksight
- You can use Cost and Usage Reports to publish your AWS billing reports to an Amazon Simple Storage Service (Amazon S3) bucket that you own.
- You can receive reports that break down your costs by the hour or month, by product or product resource, or by tags that you define yourself.
- AWS updates the report in your bucket once a day in comma-separated value (CSV) format.

#### Cost Explorer

Cost Explorer is a visual tool to understand and manage the cost and usage overtime in AWS.

> AWS Cost Explorer has an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time. AWS Cost Explorer includes a default report that helps you visualize the costs and usage associated with your top five cost-accruing AWS services, and gives you a detailed breakdown of all services in the table view. The reports let you adjust the time range to view historical data going back up to twelve months to gain an understanding of your cost trends.

> The rightsizing recommendations feature in Cost Explorer helps you identify cost-saving opportunities by downsizing or terminating EC2 instances. You can see all of your underutilized EC2 instances across member accounts in a single view to immediately identify how much you can save.

- We can create custom reports
- Analyze your data at a high level: total costs and usage across all accounts
- Or Monthly, hourly, resource level granularity
- It suggest savings plans based on the usage
- Forecast usage up to 12 months
- Check underutilized EC2 Instances

The rightsizing recommendations feature in Cost Explorer helps you identify cost-saving opportunities by downsizing or terminating EC2 instances. You can see all of your underutilized EC2 instances across member accounts in a single view to immediately identify how much you can save.

### Simple Month Calculator

> The Simple Monthly Calculator helps customers and prospects estimate their monthly AWS bill more efficiently. The Simple Monthly Calculator cannot be used to compare the cost of running the IT infrastructure on-premises vs AWS Cloud.

### Monitoring against costs plans

On AWS we can monitor and trigger actions related to our budget.

#### Billing Alarms on CloudWatch

Billing Alarms on CloudWatch only available and stored in us-east-1, but we can consolidate all the costs of our account in all regions.

This one is for actual costs, not projected costs. And it sends an email notification if we pass a threshold.

#### AWS Budgets

AWS Budgets is a powerful tool about create and send alarms when costs exceeds the budgets

- We have three types of budgets: Based on Costs, Usage and Reservation
- Up to 5 SNS notifications per budget (can trigger events based on notification)
- Can filter by: Service, Linked Account, Tag, Purchase Option, Instance Type, Region, Availability Zone, API Operation, etc…
- Same options as AWS Cost Explorer!
- 2 budgets are free, then $0.02/day/budget

> AWS Budgets gives you the ability to set custom budgets that alert you when your costs or usage exceed (or are forecasted to exceed) your budgeted amount. Difference with CloudWatch Billing Alarms: CloudWatch Billing Alarms only send alerts when your costs and usage are exceeding your budget, not when it is forecasted to exceed your budget, while AWS Budgets does both.

Supported Types of Budget:

- Cost Budget - Helps you plan how much you want to spend on a service.
- Usage Budget - Helps you plan how much you want to use one or more services.
- Reservation Budget - This helps you track the usage of your Reserved Instances (RI). Two ways of doing it - RI utilization budgets (This lets you see if your RIs are unused or under-utilized), RI coverage budgets (This lets you see how much of your instance usage is covered by a reservation).
  - You can also use AWS Budgets to set reservation utilization or coverage targets and receive alerts when your utilization drops below the threshold you define. You can define a utilization threshold and receive alerts when your RI usage falls below that threshold. This lets you see if your RIs are unused or under-utilized.

## AWS Trusted Advisor

Trusted Advisor is a assessment on AWS account with the purpose of advise possible savings, checks and cost optimizations within AWS account.

- For all customer it is free the **core checks** of AWS
- We can enable weekly reports/email notifications about the recommendations
- The full version of trusted-advisor requires a **Business and Enterprise Supports Plan**
  - You get access to advisor to all categories
  - Ability to use CloudWatch Alarms when reach limits
  - **Programmatic access using AWS Support API**

AWS Trusted Advisor provides multiple types of recommendations and after that a few examples:

<p align="center" width="100%"><img src="assets/trusted-advisor.jpg" alt="trusted-advisor" width="400"/></p>

**Cost Optimization**:

- Low utilization of EC2 Instances, idle Load Balancers, under-utilized resources (EBS Volumes)
- Reserved instances and savings plans optimizations

**Performance**:

- High utilization of EC2 Instances, CloudFront CDN Optimizations
- EC2 to EBS throughput optimizations, Alias records recommendations

**Security**

- MFA enabled on Root Account, IAM key rotations, exposed access keys
- S3 Bucket permissions for public access, security groups with unrestricted access
- Send alerts when AWS CloudTrail is not activated (To get user activity logging)

**Fault Tolerance**

- Age of EBS snapshots
- AZ balance
- ASG multi-az, ELB Configurations

**Services Limits(Quotas)**:

- Helps to understand if we are reaching a limit of a service and advises if is needed to increase before we have problems.

## Summary

- TCO Calculator: Calculate the price of moving from on premises to the cloud and get reports of the the moving
- Pricing Calculator: Calculate the price of the architecture on the cloud
- Billing Dashboard: Simple tool to overview the billings
- Cost Allocation Tags: Group tags together and get report by grouped tags
- Cost and Usage Reports: Most comprehensive report in AWS
- Cost Explorer: Visual Billing dashboard with detailed + forecast 12 usage up to 12 months
- Billing Alarms: use CloudWatch to run the billings alarms when some metric is passed (located in us-east-1)
- Budgets: more advanced alarm and notification regarding Budget. Integrated with SNS.
- Savings Plan: Easy-way to save money based on long term commitment with AWS.
- Compute Optimizer: recommends resources’ configurations to reduce cost

[UP](#aws-billing)



# 🔑 Advanced Identity

- [Amazon Cognito](#amazon-cognito)
- [Active Directory Services](#active-directory-services)
  - [AWS Managed Microsoft AD](#aws-managed-microsoft-ad)
  - [AD Connector](#ad-connector)
  - [Simple AD](#simple-ad)
- [Amazon Single Sign-On](#amazon-single-sign-on)

## Amazon Cognito

Provide identity for our Web/Mobile applications. Cognito will create the users for us and save on specific database of users.

<p align="center" width="100%"><img src="assets/cognito.jpg" alt="cognito" width="400"/></p>

## Active Directory Services

Microsoft Active Directory is found on any Windows Server with AD Domain Services and it is a Database of Objects. The main function of AD is to be a centralized service to manage users accounts, create users and assign permissions:

- With a central Domain Computer we have all the credentials stored, so any computer that belongs to that domain can have the user logged in.

<p align="center" width="100%"><img src="assets/windows-ad.jpg" alt="windows-ad" width="300"/></p>

AWS Also provides AD Services within AWS:

### AWS Managed AD

Create our own AD in AWS, manage user locally and support MFA authentication.

It works by establishing a "trust" connection with our on-premises server and they will trust each other in authentication.

<p align="center" width="100%"><img src="assets/aws-managed-ad.jpg" alt="aws-managed-ad" width="300"/></p>

### AD Connector

Is a proxy, it works by redirecting the requests from AWS windows services to our on premise to get the AD authentication.

<p align="center" width="100%"><img src="assets/ad-connector.jpg" alt="ad-connector" width="300"/></p>

### Simple AD

AD-Compatible managed Active Directory on AWS. This one is not connected with on-premises servers, it is a standalone service.

<p align="center" width="100%"><img src="assets/simple-ad.jpg" alt="simple-ad" width="150"/></p>

## Amazon Single Sign-On

One single point of access to multiple applications using SSO portal on AWS.

> AWS SSO is an AWS service that enables you to makes it easy to centrally manage access to multiple AWS accounts and business applications and provide users with single sign-on access to all their assigned accounts and applications from one place.

- Integrated with AWS organizations
- Supports SAML 2.0 markup
- Integration with on-premise Active Directory

<p align="center" width="100%"><img src="assets/sso.jpg" alt="sso" width="500"/></p>

## Summary

- IAM
  - Identity and Access Management inside your AWS account
  - For users that you trust and belong to your company
- Organizations: manage multiple AWS accounts
- Cognito: create a database of users for your mobile & web applications
- Directory Services: integrate Microsoft Active Directory in AWS
- Single Sign-On (SSO): one login for multiple AWS accounts & applications


# Other AWS Services

Services worth to know about

- [Amazon Workspaces](#amazon-workspaces)
- [Amazon AppStream 2.0](#amazon-appstream-20)
- [Amazon Sumerian](#amazon-sumerian)
- [AWS IoT Core](#aws-ioT-core)
- [AWS Elastic Transcoder](#aws-elastic-transcoder)
- [AWS Device Farm](#aws-device-farm)
- [AWS Backup](#aws-backup)
- [CloudEndure Disaster Recovery](#cloudEndure-disaster-recovery)
- [Summary](#summary)

## Amazon Workspaces

Is a managed Desktop as a Service (DaaS). It is a solution to easily provision Windows/Linux desktops.

Amazon WorkSpaces is a fully managed, secure cloud desktop service. You can use Amazon WorkSpaces to provision either Windows or Linux desktops in just a few minutes and quickly scale to provide thousands of desktops to workers across the globe.

- It is great to eliminate the management of on-premises VDI (Virtual Desktop Infrastructure)
- Fast and Scalable
- Secure data (KMS integration)
- Pay-as-you-go service with monthly or hourly rates

<p align="center" width="100%"><img src="assets/amazon-workspaces.jpg" alt="amazon-workspaces" width="700"/></p>

## Amazon AppStream 2.0

This is a Desktop Application Stream service, delivery to any computer (no need of acquiring or provision infrastructure). The application is delivered within a browser on the web.

**Amazon AppStream 2.0 vs WorkSpaces**

- Fully managed VDI and desktop available
- The users connect to the VDI and open native or WAM applications
- Workspaces are on-demand or always on

**AppStream 2.0**

Amazon AppStream 2.0 is a fully managed non-persistent application and desktop streaming service that provides users instant access to their desktop applications from anywhere.

- Stream a desktop application to web browsers (no need to connect to a VDI)
- Works with any device (that has a web browser)
- Allow to configure an instance type per application type (CPU, RAM, GPU)

## Amazon Sumerian

Amazon Sumerian is a set of browser-based tools for creating high-quality virtual reality (VR), augmented reality (AR), and 3D applications easily without requiring any programming or 3D graphics expertise. With Sumerian, you can construct an interactive 3D scene without any programming experience, test it in the browser, and publish it as a website that is immediately available to users.

- Ready-to-use templates and assets - no programming or 3D expertise required
- Accessible via a web-browser URLs or on popular hardware for AR/VR

## AWS IoT Core

IoT stands for “Internet of Things” – the network of internet-connected devices that are able to collect and transfer data. AWS IoT Core allows you to easily connect devices with AWS Cloud services.

AWS IoT Core lets you securely connect IoT devices to the AWS Cloud and other devices without the need to provision or manage servers.

- Serverless, secure and scalable to billions of devices and trillions of messages
- Your applications can communicate with your devices even when they aren’t connected
- Integrates with a lot of AWS services (Lambda, S3, SageMaker, etc.)
- Build IoT applications that gather, process, analyze, and act on data

<p align="center" width="100%"><img src="assets/iot-core.jpg" alt="iot-core" width="300"/></p>

## AWS Elastic Transcoder

Amazon Elastic Transcoder is media transcoding in the cloud. It is used to convert media files from their source format into versions that will play back on devices like smartphones, tablets, and PCs.

Converts S3 files within a bucket and convert to many formats and save into a target bucket.

- Benefits:
  - Easy to use
  - Highly scalable – can handle large volumes of media files and large file sizes
  - Cost effective – duration-based pricing model
  - Fully managed & secure, pay for what you use

<p align="center" width="100%"><img src="assets/elastic-transcoder.jpg" alt="elastic-transcoder" width="600"/></p>

## AWS Device Farm

Fully managed service that tests our application (web and mobile) in multiple desktop browsers and real mobile devices and tablets.

- Run tests concurrently on multiple devices
- Can configure any settings we want (bluetooth, gps, etc.)
- We can interact with all devices
- We receive reports and logs of all tests

<p align="center" width="100%"><img src="assets/device-farm.jpg" alt="device-farm" width="600"/></p>

## AWS Backup

It is a Fully managed service to centrally manage and automate backups across AWS services.

- Supports On demand and scheduled backups
- Supports Point-In-Recovery (PITR)
- It allows creation of Retention Policies, Lifecycle Management, Backup Policies and more...
- Supports Cross-Region and Cross-Account backups

<p align="center" width="100%"><img src="assets/aws-backup.jpg" alt="aws-backup" width="600"/></p>

## CloudEndure Disaster Recovery

CloudEndure is a company acquired by AWS and AWS has its services now.

CloudEndure Disaster Recovery Quickly and easily recover your physical, virtual and cloud-based servers in AWS.

- Continuos block level replication for the servers.
- Example: You have a data center with CLoudEndure agent. It will continuously replicate the data to AWS Cloud in a Staging area with low-cost EC2 instances and EBS Volumes. In case of failovers, in minutes, it starts run more powerful EC2 instances with the most recent data until the datacenter is recovered. Since it is recovered it does a failback process and release the Production EC2 instance (just keep the staging to keep replicating data).
- Use cases: Protect most critical databases, enterprise apps and protect data from Ransomware attacks.

<p align="center" width="100%"><img src="assets/aws-cloudendure.jpg" alt="aws-cloudendure" width="600"/></p>

## Summary

- Amazon Workspaces: Desktop as a Service and provides a windows or linux desktop
- Amazon AppStream 2.0: Access any application within a browser
- Amazon Sumerian: Create 3D/VR applications (browser app)
- AWS IoT Core: Connect billions of IoT devices with AWS
- AWS Elastic Transcoder: Convert media to multiple formats (s3 stored media)
- AWS Device Farm: Service to test our applications in multiple devices (it is a farm of devices on AWS)
- AWS Backup: centrally manage and automate backups across AWS services
- CloudEndure Disaster Recovery:


# AWS Architecting & Ecosystem

AWS Well Architected Framework has general guiding principles to be applied:

- Stop guessing capacity of our needs and start scaling our services
- Test our systems at scale
- Automate to make architectural experimentation easier (using cloudformation, beanstalk, or other for example)
- Allow for evolutionary architectures designing based on changing requirements (using IaaS)
- Drive architectures using data
- Improve through game days: Simulate applications for flash sale days

## AWS Cloud Best Practices – Design Principles

- Scalability: vertical & horizontal
- Disposable Resources: servers should be disposable & easily configured
- Automation: Serverless, Infrastructure as a Service, Auto Scaling…
- Loose Coupling: Monolith are applications that do more and more over time, become bigger. So we need to Break it down into smaller, loosely coupled components. So, a change or a failure in one component should not cascade to other components.
- Services, not Servers: Don’t use just EC2, use managed services, databases, serverless, etc.

# Well Architected Framework

The Well Architected Framework has five Pillar:

- [1st Pillar - Operational Excellence](#1st-pillar---operational-excellence)
- [2nd Pillar - Security](#2nd-pillar---security)
- [3rd Pillar - Reliability](#3rd-pillar---reliability)
- [4th Pillar - Performance Efficiency](#4th-pillar---performance-efficiency)
- [5th Pillar - Cost Optimization](#5th-pillar---cost-optimization)
- [Well Architected Tool](#well-architected-tool)
- [AWS Ecosystem - Free resources](#aws-ecosystem---free-resources)
- [Summary](#Summary)

<p align="center" width="100%"><img src="assets/pillars.jpg" alt="pillars" width="700"/></p>

## 1st Pillar - Operational Excellence

A well architected framework with Operational Excellence includes the ability to run and monitor the applications to deliver value to the business and continually improve supporting processes and procedures.

The design principles:

- Perform Infrastructure as a Code (IaaC) - CloudFormation
- Documentation - Automate the creation of annotated docs after every build
- Make frequent, small and reversible changes: this will avoid issues in case you need to rollback
- Refine operations procedures frequently
- Anticipate failures and learn from them all

AWS Services to Operational Excellence:

- Prepare phase: Use CloudFormation to have the IaaC, AWS Config to evaluate compliance
- Operate: CloudFormation and AWS Config to perform the resources configuration and AWS CloudTrail and CloudWatch to monitor how it is going and if anything is gone manually
- Evolve: AWS CloudFormation and CI/CD Tools allows to evolve quickly

<p align="center" width="100%"><img src="assets/1st-pillar-operational-excellence.jpg" alt="1st-pillar-operational-excellence" width="700"/></p>

## 2nd Pillar - Security

Security includes the ability to protect the information, applications and assets while delivering business value trough risk assessment and mitigation strategies. It will also save costs from avoidable disasters and failures.

> "Who did what" is nothing but traceability of action by any user on the system. It tells us which user performed what action on the system. Traceability is part of the Security design principle of AWS Cloud. So this is the correct option.

Design Principles:

- Implementing a Strong Identity Foundation: Centralized Privileges and Management. Rotate credentials often.
- Enable Traceability: integrate logs and metrics with systems to automatically respond and take actions.
- Apply security at all layers:
- Automate security best practices
- Protect data in transit and at rest - Encryption, tokenization, and access control
- Keep people away from data - eliminate or reduce the need of direct access to manual data processing
- Prepare for security events - Run incident response simulations and use tools with automation to increase your speed for detection, investigation, and recovery

<p align="center" width="100%"><img src="assets/2nd-pillar-security.jpg" alt="2nd-pillar-security" width="700"/></p>

## 3rd Pillar - Reliability

Ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues.

> Foundations are part of the Reliability pillar of the AWS Well-Architected Framework. AWS states that before architecting any system, foundational requirements that influence reliability should be in place. The services that are part of foundations are: Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (earlier known as AWS Service Limits).

> AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement. Whether establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally.

> Service Quotas enables you to view and manage your quotas for AWS services from a central location. Quotas, also referred to as limits in AWS, are the maximum values for the resources, actions, and items in your AWS account. Each AWS service defines its quotas and establishes default values for those quotas.

**Design Principles**:

- Test recovery procedures: Use automation to simulate different failures or to recreate scenarios that led to failures before
- Automatically recover from failures: Anticipate and remediate failures before they occur
- Stop guessing capacity: Auto scaling whenever is possible (Horizontal scaling) Load Balancing (Distribute requests across multiple, smaller resources to ensure that they don't share a common point of failure)
- Management changes through automation: Use automation to make changes to infrastructure

<p align="center" width="100%"><img src="assets/3rd-pillar-reliability.jpg" alt="3rd-pillar-reliability" width="700"/></p>

## 4th Pillar - Performance Efficiency

Includes the ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.

Design Principles:

- Democratize advanced technologies - Advance technologies become services and hence you can focus more on product development
- Go global in minutes - Easy deployment in multiple regions
- Use serverless architectures - Avoid burden of managing servers
- Experiment more often - Easy to carry out comparative testing
- Mechanical sympathy - Be aware of all AWS services

<p align="center" width="100%"><img src="assets/4th-pillar-performance-efficiency.jpg" alt="4th-pillar-performance-efficiency" width="700"/></p>

## 5th Pillar - Cost Optimization

Includes the ability to run systems to deliver business value at the lowest price point.

Design Principles

- Adopt a consumption mode - Pay only for what you use
- Measure overall efficiency - Use CloudWatch
- Stop spending money on data center operations - AWS does the infrastructure part and enables customer to focus on organization projects
- Analyze and attribute expenditure - Accurate identification of system usage and costs, helps measure return on investment (ROI) - Make sure to use tags
- Use managed and application level services to reduce cost of ownership - As managed services operate at cloud scale, they can offer a lower cost per transaction or service

<p align="center" width="100%"><img src="assets/5th-pillar-cost-optimization.jpg" alt="5th-pillar-cost-optimization" width="700"/></p>

## Well Architected Tool

It is a Free tool to review your architectures against the 5 pillars Well-Architected Framework and adopt architectural best practices.

How does it work?

- Select your workload and answer questions
- Review your answers against the 5 pillars
- Obtain advice: get videos and documentations, generate a report, see the results in a dashboard

## AWS Ecosystem

Free Resources

- AWS Blogs: https://aws.amazon.com/blogs/aws/
- AWS Forums (community): https://forums.aws.amazon.com/index.jspa
  - AWS Forums is an AWS community platform where people can help each other. It is not used to deploy technologies on AWS.
- AWS Whitepapers & Guides: https://aws.amazon.com/whitepapers
  - AWS Whitepapers are technical content authored by AWS and the AWS community to expand your knowledge of the cloud. They include technical whitepapers, technical guides, reference material, and reference architectures diagrams. You can find useful content for your deployment, but it is not a service that will deploy technologies.
- AWS Quick Starts: https://aws.amazon.com/quickstart/

  - Quick Starts are built by AWS solutions architects and partners to help you deploy popular technologies on AWS, based on AWS best practices for security and high availability. These accelerators reduce hundreds of manual procedures into just a few steps, so you can build your production environment quickly and start using it immediately.
  - Each Quick Start includes AWS CloudFormation templates that automate the deployment and a guide that discusses the architecture and provides step-by-step deployment instructions.

- Automated, gold-standard deployments in the AWS Cloud
- Build your production environment quickly with templates
- Example: WordPress on AWS https://fwd.aws/P3yyv?did=qs_card&trk=qs_card
- Leverages CloudFormation
- AWS Solutions: https://aws.amazon.com/solutions/
- Vetted Technology Solutions for the AWS Cloud
- Example - AWS Landing Zone: secure, multi-account AWS environment
- https://aws.amazon.com/solutions/implementations/aws-landing-zone/
- “Replaced” by AWS Control Tower

Payed Resources

- AWS Support
- AWS Marketplace
- AWS Training
- AWS Professional Services & Partner Network (global team of experts APN [AWS Technology Partners])

## AWS Support

More in account, billing and support [section](../account-billing-support/README.md/#aws-support-plans)

- Basic
  - Free support
  - Has Customer Services & Communities - 24x7 access to customer service, documentation, whitepapers and support forums.
- Developer: Business Hours email access to Cloud Support Associates
  - General Guidance: <24 business hours
  - System impaired: <12 business hours
- Business: 24x7 Phone, Mail and chat support from Cloud Support Engineers
  - Production System impaired: <4 business hours
  - Production System down: <1 business hours
- Enterprise: Access to Technical Account Manager (TAM) and Concierge Support Team
  - Business Critical Systems down <15 minutes

## AWS Professional Services & Partner Network

- The AWS Professional Services organization is a global team of experts
- They work alongside your team and a chosen member of the APN
- APN = AWS Partner Network
- APN Technology Partners: providing hardware, connectivity, and software
- APN Consulting Partners: professional services firm to help build on AWS
- APN Training Partners: find who can help you learn AWS
- AWS Competency Program: AWS Competencies are granted to APN
  Partners who have demonstrated technical proficiency and proven
  customer success in specialized solution areas.
- AWS Navigate Program: help Partners become better Partners

## Summary

- **1st Pillar - Operational Excellence**: Ability to run and Monitor applications/systems while deliver business value + improvement through time. (Have great operations and deployment options)
- **2nd Pillar - Security**: Ability to protect the data, applications and assets + risk management. (Make secure environments)
- **3rd Pillar - Reliability**: Ability to recover from infrastructure issues and scale/get elastic to meet demand. (Ensure the application runs no matter what)
- **4th Pillar - Performance Efficiency**: Meet system requirements and maintain efficiency while adapting to technologies (Adapting and providing the best performance and look for new technologies)
- **5th Pillar - Cost Optimization**: Means cost reduction while delivering the best quality
- Well Architected Tool: Free AWS Tool
- AWS Ecosystem - Free resources
- AWS Support - Basic, Developer, Business and Enterprise

[UP](#aws-architecting--ecosystem)




