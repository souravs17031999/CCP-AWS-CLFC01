# Technology

## methods of deploying and operating in the AWS Cloud:**
- Programmatic access, APIs: To connect programmatically to an AWS service, you use an endpoint. An endpoint is the URL of the entry point for an AWS web service. 
The AWS SDKs and the AWS Command Line Interface (AWS CLI) automatically use the default endpoint for each service in an AWS Region. But you can specify an alternate endpoint for your API requests.
- SDKs: Easily develop applications on AWS in the programming language of your choice
- AWS Management Console: Everything you need to access and manage the AWS Cloud — in one web interface
- CLI: The AWS Command Line Interface (AWS CLI) is an open source tool that enables you to interact with AWS services using commands in your command-line shell.
-  Infrastructure as Code: Practicing infrastructure as code means applying the same rigor of application code development to infrastructure provisioning. 
All configurations should be defined in a declarative way and stored in a source control system

_AWS Elastic Beanstalk_  
- high-level deployment tool, platform configuration defines the infrastructure and software stack to be used for a given environment.  
- Upload your code and Elastic Beanstalk automatically handles the deployment—from capacity provisioning, load balancing, and auto scaling to application health monitoring.  
- returns a production ready instance URL

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/22e17316-da85-4826-b78e-31463c8012fa)   

_AWS CloudFormation_  
- Create a template (JSON or YAML) that describes all the AWS resources that you want. It takes care of provisioning and configuring those resources for you. This file serves as the single source of truth for your cloud environment.
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/a6897c25-cec2-47d1-906c-2160cc22fff8)

Futbol Club Barcelona Case Study:   
- We are very happy with AWS CloudFormation, because it means we are able to use ‘one-click’ deployment of our whole infrastructure.AWS is really a game changer because it removes the need to devote a lot of the dedication and resources to micro-manage your own platform. AWS is key for us. As a service provider, it allows us to combine the best time to market and technical capability with very competitive prices and a pay-per-use model. Because AWS is strategic for us, we also have an AWS specialized team to provide services for our customers.  

Expedia Group:  
- From an architectural perspective, infrastructure, automation, and proximity to the customer were key factors,
- By deploying ESS on AWS, Expedia Group was able to improve service to customers in the Asia Pacific region as well as Europe. “Latency was our biggest issue,” says Chandramouli. “Using AWS, we decreased average network latency from 700 milliseconds to less than 50 milliseconds

_AWS OpsWorks_  
- Chef and Puppet are automation platforms that allow you to use code to automate the configurations of your servers. OpsWorks lets you use Chef and Puppet to automate how servers are configured, deployed, and managed across your Amazon EC2 instances or on-premises compute environments. 

_AWS CodeCommit_
- Makes it easy for companies to host secure and highly scalable private Git repositories.
- Maintain your repositories close to your build, staging, and production environments on AWS.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/b90c0c37-70f9-4923-848a-524836994f90)  

-----------------------------------------------------------------------------------------------------------------   
## cloud deployment models
**Hybrid :**   
AWS Outposts: 
- family of fully managed solutions delivering AWS infrastructure and services to virtually any on-premises or edge location for a truly consistent hybrid experience.
- ex. Riot was able to rapidly deploy game servers and reduce latency by 10 to 20 milliseconds, minimizing peeker’s advantage and creating a level playing field for all players.
- AWS Partner Network (APN) delivers and installs on-premises
- Racks: Deliver low-latency compute (single digit millisecond latency), • Includes integrated networking gear.
- Servers: Run AWS Outposts in locations with limited space or smaller capacity requirements, • Does not include integrated networking gear.
- Overall, they are connected to aws using direct connect or local gateway.

AWS Wavelength:
- Develop applications once and scale deployments to multiple Wavelength Zones across global 5G networks.
- Leverage proven AWS infrastructure and services to accelerate innovative 5G edge application development.

AWS local zones:
- Run applications that require single-digit millisecond latency or local data processing by bringing AWS infrastructure closer to your end users and business centers.
- ex. Netflix artistic collaboration in real time , remote workstations in cloud 
- ex. Couchbase Reduces Latency by 80% for Its Distributed Database Solutions Using AWS Local Zones
- Local Zones allow customers to gain all the benefits of having compute and storage resources closer to end-users, without the need to own and operate their own data center infrastructure.

AWS Snow:
- Move petabytes of data to and from AWS, or process data at the edge
- Purpose-built devices to cost effectively move petabytes of data, offline. Lease a Snow device to move your data to the cloud.
- encryption, AWS Snow devices feature a Trusted Platform Module (TPM) that provides a hardware root of trust. Each device is inspected after each use to ensure the integrity of the device and helps preserve the confidentiality of your data.
- Snowcone, Snowball, SnowMobile 

## connectivity options

**VPN**  
- Connect your on-premises networks and remote workers to the cloud
- Integrate with Mobile Device Management (MDM) solutions to reject devices that do not comply with your policies.
- Use Site-to-Site VPN connections to communicate securely between remote sites.

**AWS Direct Connect**   
- Create a dedicated network connection to AWS  
- Once you link your network to AWS Direct Connect, you can use SiteLink to send data between your locations. When using SiteLink, data travels over the shortest path between locations.
- The AWS Direct Connect cloud service is the shortest path to your AWS resources. While in transit, your network traffic remains on the AWS global network and never touches the public internet. This reduces the chance of hitting bottlenecks or unexpected increases in latency.   
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/015268c6-5bfb-478e-9589-4388c198e63e)


**Public Internet**  
- Connect to the internet using an internet gateway
- An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between your VPC and the internet. It supports IPv4 and IPv6 traffic.
------------------------------------------------------------------------------------------------------  

## AWS global infrastructure

**Regions, Availability Zones, and Edge Locations**
- physical location around the world where we cluster data centers. We call each group of logical data centers an Availability Zone. Each AWS Region consists of a minimum of three, isolated, and physically separate AZs within a geographic area.
- An Availability Zone (AZ) is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region.
- All AZs in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs.
- If an application is partitioned across AZs, companies are better isolated and protected from issues such as power outages, lightning strikes, tornadoes, earthquakes, and more. AZs are physically separated by a meaningful distance, many kilometers, from any other AZ, although all are within 100 km (60 miles) of each other.
- The code for Availability Zone is its Region code followed by a letter identifier. For example, us-east-1a.
- Edge location: A site that CloudFront uses to cache copies of your content for faster delivery to users at any location.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/2f518521-737a-44e7-8a0a-fc765fa237fd)

**how to achieve high availability through the use of multiple Availability Zones**
- Single points of failure (SPOF) are commonly eliminated with an N+1 or 2N redundancy configuration, where N+1 is achieved via load balancing among active–active nodes, and 2N is achieved by a pair of nodes in active–standby configuration.
- AWS has several methods for achieving HA through both approaches, such as through a scalable, load balanced cluster or assuming an active–standby pair.
- High availability for systems is represented through a sequence of “9s”.
- Three-nine availability, represented as 99.9%, allows 8 hours and 46 minutes of downtime per year.
- Four-nine availability, 99.99%, allows 52 minutes and 36 seconds of downtime per year.
- Five-nine availability, 99.999% which is the accepted standard for mission-critical operations, provides about 5 minutes and 15 seconds of downtime per year.

**Multi-Region Application Architecture**  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/c2eb9614-7e2c-4376-8569-92fe83532969)  

**Disaster recovery options in the cloud** 

*RTO stands for Recovery Time Objective and is a measure of how quickly after an outage an application must be available again
*RPO, or Recovery Point Objective, refers to how much data loss your application can tolerate.
*Another way to think about RPO is how old can the data be when this application is recovered? With both RTO and RPO, the targets are measured in hours, minutes, or seconds, with lower numbers representing less downtime or less data loss.

RTO questions: 
What is the impact if this application is unavailable? Does this impact change over time?  
Is there a financial cost? How much per hour?  
Is there a reputational cost? E.g. – A public facing corporate landing page  
Does this application have an SLA with internal or external customers?   
Are there external compliance or regulatory requirements this application is subject to?  
Does this application depend on any other applications? Do you know of any applications that depend on this application?  

RPO questions:
What is the impact of data loss for this application?  
Is there a financial cost? How much per hour?   
Is there a reputational cost?   
Does this application have an SLA with internal or external customers?   
Are there external compliance or regulatory requirements this application is subject to?   
Do other applications that depend on data from this application? What are their RPO requirements?  
Can lost data be recreated? How long would this take, and is this acceptable?   
How often does the data change?   

*AWS Resilience Hub
- AWS Resilience Hub was recently released to help customers establish RPO/RTO targets per application, and then analyze applications against those targets. 
- Resiliency Policies are assigned to one or more applications, creating a Tier.  Applications are then assessed against their Tier’s targets either via a direct request from a user, via a scheduled assessment, or as part of your CI/CD pipeline. 
- Following this assessment, Resilience Hub provides a breakdown of what individual components within your application meet, exceed, or fall short of the targeted objective.   

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/6380a8ff-93ca-4e06-9971-8357c27abdc9)   

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/d3b7b169-91c7-471c-babf-893230c6943f)   

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/de4837d1-bb63-4b38-b56a-54308232123c)  

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/dbfe0b1b-ff58-4429-a594-4cf9aa6e2bb3)   


_backup_and_restore_    
- suitable approach for mitigating against data loss or corruption. This approach can also be used to mitigate against a regional disaster by replicating data to other AWS Regions  
- Your workload data will require a backup strategy that runs periodically or is continuous. How often you run your backup will determine your achievable recovery point (which should align to meet your RPO). The backup should also offer a way to restore it to the point in time in which it was taken.     

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/da8cee29-f316-4c2a-a5f0-bbbd41de88ff)    


_pilot_light_
- you replicate your data from one Region to another and provision a copy of your core workload infrastructure.
- Resources required to support data replication and backup, such as databases and object storage, are always on
- Other elements, such as application servers, are loaded with application code and configurations, but are "switched off" and are only used during testing or when disaster recovery failover is invoked.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/1fea0294-ea1c-4cb7-9793-e793291c2553)    

_Warm standby_
- involves ensuring that there is a scaled down, but fully functional, copy of your production environment in another Region.   
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/74e5803c-6cbc-4d78-9916-c63f31c56bc8)

_Multi-site active/active_
- multi-site active/active or hot standby active/passive strategy
- Hot standby uses an active/passive configuration where users are only directed to a single region and DR regions do not take traffic.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/9dee3a81-2e23-4409-8e6f-1449b4bed785)
  
**High availability is not disaster recovery**

**Edge Locations**

_Amazon CloudFront_
- Reduce latency by delivering data through 450+ globally dispersed Points of Presence (PoPs) with automated network mapping and intelligent routing.
- AWS Shield Standard to defend against DDoS attacks at no additional charge.
- Customize the code you run at the AWS content delivery network (CDN) edge using serverless compute features
- Scale automatically to deliver software, game patches, and IoT over-the-air (OTA) updates at scale with high transfer rates.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/76d27703-ad2d-4522-9066-0c8ccf177101)   


_AWS Global Accelerator_
- Deliver highly available applications with fast failover for multi-Region and multi-AZ architectures.
- Achieve deterministic routing by removing DNS cache dependencies.
- Global Accelerator provides two global static public IPs that act as a fixed entry point to your application endpoints such as ALB etc...  
- Use traffic dials to route traffic to the nearest Region or achieve fast failover across Regions.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/9fe2e7b7-48f6-4f67-b031-2c3083097118)   


----------------------------------------------------------------------------

## AWS Compute Services

**different compute families**

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/169992e3-2237-4872-9a86-f31a8151f799)   

Instance families   
C – Compute  

D – Dense storage  

F – FPGA   

G – GPU   

Hpc – High performance computing  

I – I/O   

Inf – AWS Inferentia   

M – Most scenarios   

P – GPU   

R – Random access memory  

T – Turbo   

Trn – AWS Tranium  

U – Ultra-high memory  

VT – Video transcoding   

X – Extra-large memory  

Additional capabilities    
a – AMD processors   

g – AWS Graviton processors   

i – Intel processors   

d – Instance store volumes   

n – Network optimization    

b – Block storage optimization  

e – Extra storage or memory   

z – High frequency  

_general purpose_
- provide a balance of compute, memory and networking resources, and can be used for a variety of diverse workloads.
- ex. Applications built on open-source software such as application servers, microservices, gaming servers, midsize data stores, and caching fleets.  

_Compute Optimized_
- Compute Optimized instances are ideal for compute bound applications that benefit from high performance processors. high performance computing (HPC), scientific modeling, dedicated gaming servers, machine learning etc...
- ex. batch processing, ad serving, video encoding, gaming, scientific modelling

_Memory Optimized_
- Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.
- ex. open-source databases, in-memory caches, and real-time big data analytics.

_Storage Optimized_
- Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. IOPS applications.
- ex. MySQL, MariaDB, and PostgreSQL), and NoSQL databases (KeyDB, ScyllaDB, and Cassandra).

_Accelerated Computing_
- Accelerated computing instances use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing
- ex. Machine learning, high performance computing, computational fluid dynamics, computational finance, seismic analysis, speech recognition, autonomous vehicles, and drug discovery.

### Instances (virtual machines)

**EC2 (Amazon Elastic Compute Cloud)**
- Amazon EC2 delivers secure, reliable, high-performance, and cost-effective compute infrastructure to meet demanding business needs.
- Amazon EC2 delivers the broadest for ML projects 
- 4 9's availability SLA's
- The AWS Nitro System is the underlying platform for our next generation of EC2 instances: high security

**EC2 spot instances**
- Spot Instances are available at up to a 90% discount compared to On-Demand prices.
- You can run hyperscale workloads at a significant cost savings or you can accelerate your workloads by running parallel tasks.
- You also have the option to hibernate, stop or terminate your Spot Instances when EC2 reclaims the capacity back with two-minutes of notice.
- However, Spot does not guarantee that you can keep your running instances long enough to finish your workloads. Spot also does not guarantee that you can get immediate availability of the instances that you are looking for, or that you can always get the aggregate capacity that you requested. 

**EC2 Auto Scaling**
- Add or remove compute capacity to meet changing demand
- Follow the demand curve for your applications so that you don’t have to provision Amazon EC2 capacity in advance.
- An Auto Scaling group contains a collection of EC2 instances that are treated as a logical grouping for the purposes of automatic scaling and management.
- An Auto Scaling group also lets you use Amazon EC2 Auto Scaling features such as health check replacements and scaling policies.
- scaling options: Maintain current instance levels at all times, Scale manually where you specify only the change in the maximum, minimum, or desired capacity of your Auto Scaling group, Scale based on a schedule, Scale based on demand, Use predictive scaling.

**Load Balancers**
- Elastic Load Balancing automatically distributes your incoming application traffic across all the EC2 instances that you are running. Elastic Load Balancing helps to manage incoming requests by optimally routing traffic so that no one instance is overwhelmed.
- To use Elastic Load Balancing with your Auto Scaling group, attach the load balancer to your Auto Scaling group.

_Application Load Balancer_
- Routes and load balances at the application layer (HTTP/HTTPS), and supports path-based routing. WAF rules to protect against common attacks.

_Network Load Balancer_
- Routes and load balances at the transport layer (TCP/UDP Layer-4), based on address information extracted from the Layer-4 header.

_Gateway Load Balancer_
- Distributes traffic to a fleet of appliance instances. Provides scale, availability, and simplicity for third-party virtual appliances, such as firewalls, intrusion detection and prevention systems, and other appliances.

_Classic Load Balancer_
- Routes and load balances either at the transport layer (TCP/SSL), or at the application layer (HTTP/HTTPS).

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/ba33f4ca-82c2-43cc-89e8-c24d43e795cc)   

**Amazon LightSail**
- Use pre-configured development stacks like LAMP, Nginx, MEAN, and Node.js. to get online quickly and easily.
- Build and personalize your blog, ecommerce, or personal website in just a few clicks, with pre-configured applications like WordPress, Magento, Prestashop, and Joomla.
- Easily create and delete development sandboxes and test environments

**Amazon Batch**
- Run hundreds of thousands of batch and machine learning (ML) computing jobs without installing software or servers.
- AWS Batch lets developers, scientists, and engineers efficiently run hundreds of thousands of batch and ML computing jobs while optimizing compute resources
- Run financial services analyses, drugs and sequence genomes, render visual effects, ML training Jobs etc...

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/14b48264-0ffc-4bf8-9071-be70015173cf)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/2856695b-b81e-4fad-8325-18d99bdf98e6)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/c3e5efa0-e26f-44e8-8e4a-ca1efd58014b)   

### Containers 

**Amazon Elastic Container Service (Amazon ECS)**
- Run highly secure, reliable, and scalable containers. fully managed container orchestration service
- Automatically scale and run web applications in multiple Availability Zones with the performance, scale, reliability, and availability of AWS.
- Plan, schedule, and run batch computing workloads and train NLP, ML models without managing the infrastructure by using Amazon ECS with AWS Fargate.
- Amazon ECS supports Docker and enables you to run and manage Docker containers.
- Amazon ECS allows you to define tasks through a JavaScript Object Notation (JSON) template called a _Task Definition_. Within a Task Definition, you can specify one or more containers that are required for your task, including the Docker repository and image, memory and CPU requirements, shared data volumes, and how the containers are linked to each other.You can launch as many tasks as you want from a single Task Definition file that you can register with the service.

**Amazon ECS Anywhere**
- Run containers on your on-premises infrastructure
- Run containerized data-processing workloads at edge locations on your own hardware to maintain reduced latency.
- Use your existing Windows Server licenses to run Windows container workloads in on-premises environments.

**Amazon Elastic Container Registry**
- Push container images to Amazon ECR without installing or scaling infrastructure, and pull images using any management tool.
- Meet your image compliance security requirements using the tightly integrated Amazon Inspector vulnerability management service
- Access and distribute your images faster, reduce download times, and improve availability using a scalable, durable architecture.
- like Docker Hub etc...

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/e477eb63-f888-4984-a638-c5a482bd4bad)  

**Amazon Elastic Kubernetes Service (Amazon EKS)**
- The most trusted way to start, run, and scale Kubernetes. Leverage built-in integrations with AWS services such as EC2, VPC, IAM, EBS and more 
- Ensure a more secure Kubernetes environment with security patches automatically applied to your cluster’s control plane.

**AWS Fargate**
- Deploy and manage your applications, not infrastructure. Fargate removes the operational overhead of scaling, patching, securing, and managing servers.
- AWS Fargate is compatible with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS).
- abstracts the underlying infrastructure and can be used to launch and run containers without having to provision or manage EC2 instances.

**App Runner**
- AWS App Runner is a fully managed container application service that lets you build, deploy, and run containerized web applications and API services without prior infrastructure or container experience.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/95368ddc-5a1e-475f-afdd-ac910e4ad3ea)  

### Serverless

**AWS Lambda**
- Run code without provisioning or managing infrastructure. Simply write and upload code as a .zip file or container image.
- Automatically respond to code execution requests at any scale, from a dozen events per day to hundreds of thousands per second.
- Respond to high demand in double-digit milliseconds with Provisioned Concurrency.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/797c8230-a472-4c72-8621-3322f79d1e90)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/f717d5da-84d7-4ca8-b4c0-d840c37e2ccc)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/ec2dd29a-cefc-4722-8a92-ee6afdd76b98)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/40434a2a-9068-4d16-9875-10bd21ee426e)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/8260f2f7-a30a-4b58-805c-3b3659e5bbef)  


### Edge and Hybrid

- All covered earlier 

### Cost management

**EC2 Image Builder**
- EC2 Image Builder simplifies the building, testing, and deployment of Virtual Machine and container images for use on AWS or on-premises.
- providing a simple graphical interface, built-in automation, and AWS-provided security settings. With Image Builder, there are no manual steps for updating an image nor do you have to build your own automation pipeline.
- validate your images for functionality, compatibility, and security compliance with AWS-provided tests and your own tests before using them in production
- Examples of secure image with AWS-provided and/or custom templates includes: 1/ Ensure security patches are applied, 2/ Enforce strong passwords, 3/ Turn on full disk encryption, 4/ Close all non-essential open ports, 5/ Enable software firewall, 6/ Enable logging/audit controls.

**AMI**
- An Amazon Machine Image (AMI) is a supported and maintained image provided by AWS that provides the information required to launch an instance. You must specify an AMI when you launch an instance.
- It can be customized and published, registered or deregistered on Marketplaces open sourced.

## AWS Storage Services

## AWS Networking Services

## AWS Databases Services
