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

_AWS  CodeBuild_
- You just specify the location of your source code and choose your build settings, and CodeBuild will run your build scripts for compiling, testing, and packaging your code.
- Automate continuous integration and delivery (CI/CD) pipelines

_AWS  CodeDeploy_
- Automate and consistently deploy your applications  across your development, test, and production environments.
- Support multiple deployment types, including in-place, canary, and blue/green deployments.

_AWS  CodePipeline_
- AWS CodePipeline is a fully managed continuous delivery service that helps you automate your release pipelines for fast and reliable application and infrastructure updates.
- Update existing pipelines and provide templates for creating new pipelines with a declarative JSON document.

_AWS  CodeStar_
- AWS CodeStar enables you to quickly develop, build, and deploy applications on AWS. AWS CodeStar provides a unified user interface, enabling you to easily manage your software development activities in one place. 
- With AWS CodeStar, you can set up your entire continuous delivery toolchain in minutes, allowing you to start releasing code faster.   

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

### Analytics
**Amazon Athena**
- Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL. Athena is serverless, so there is no infrastructure to manage, and you pay only for the queries that you run.
- Analyze data or build applications from an Amazon Simple Storage Service (S3) data lake and 30 data sources, including on-premises data sources or other cloud systems using SQL or Python.
- Analyze petabyte-scale data where it lives with ease and flexibility

**Amazon Kinesis**
- Collect, process, and analyze real-time video and data streams
- Build apps for application monitoring, fraud detection, and live leaderboards. Analyze data and emit the results to any data store or application.
- Perform real-time analytics on data that has been traditionally analyzed using batch processing.
- Process streaming data from IoT devices, and then use the data to programmatically send real-time alerts and respond when a sensor exceeds certain operating thresholds.

## Application integration

**Amazon SNS (Simple Notification service)**
- Fully managed Pub/Sub service
- Deliver application-to-application (A2A) notifications to integrate and decouple distributed applications.
- Distribute application-to-person (A2P) notifications to your customers with SMS texts, push notifications, and email.
- Push mechanism

**Amazon SQS (Simple Queue service)**
- Fully managed message queuing for microservices
- Separate frontend from backend systems, such as in a banking application. Customers immediately get a response, but the bill payments are processed in the background.
- Amazon SQS provides a simple and reliable way for customers to decouple and connect components (microservices) together using queues.
- Pull mechanism

## Customer Engagement
**Amazon Connect**  
- Provide superior customer service at a lower cost with an easy-to-use cloud contact center
- Set up a cloud contact center in just a few clicks and onboard agents to help customers right away.
- Improve agent productivity and customer experience across voice and digital channels with the all-in-one, AI- and ML-powered contact center.

## Management, Monitoring, and Governance:
**Amazon EventBridge**
- Easily build loosely coupled, event-driven architectures to help you deploy new features faster.  

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/f8b819e7-6893-4d2d-b469-a736a38ee0b2)  

**AWS License Manager**
- License Manager makes it easier for you to manage your software licenses from vendors, such as Microsoft, SAP, Oracle, and IBM, across AWS and your on-premises environments.
- Switch between license types and automate the discovery, tracking, and reporting of existing licenses.
- Automate the distribution and activation of software entitlements and workloads across AWS accounts for end users.

**AWS Secrets Manager**
- Centrally manage the lifecycle of secrets
- AWS Secrets Manager helps you manage, retrieve, and rotate database credentials, API keys, and other secrets throughout their lifecycles.

**AWS systems manager**
- Improve visibility and control in the cloud, on premises, and at the edge.
- Shorten the time to detect and resolve operational issues.
- Automate configuration and ongoing management of your applications and resources.
- AWS Systems Manager Parameter Store: provides secure, hierarchical storage for configuration data management and secrets management. You can store data such as passwords, database strings, Amazon Machine Image (AMI) IDs, and license codes as parameter values. You can store values as plain text or encrypted data. 

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

**Amazon WorkSpaces**
- Amazon WorkSpaces is a fully managed desktop virtualization service for Windows, Linux, and Ubuntu, that allows you to access resources from any supported device.  
- Facilitate remote work, learning environments for students and educators   
- Allow devs to test quickly their code across multiple environments 

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

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/5841dd11-1331-4380-bbcf-c3671c51d426)  


**S3 (Amazon Simple Storage Service)**
- Scale storage resources to meet fluctuating needs with 99.999999999% (11 9s) of data durability.
- Protect your data with unmatched security, compliance, and audit capabilities.
- object storage service offering industry-leading scalability, data availability, security, and performance.
- Amazon S3 is the best place to build data lakes because of its unmatched durability, availability, scalability, security, compliance, and audit capabilities.
- provides strong read-after-write consistency for PUT and DELETE requests of objects in your Amazon S3 bucket in all AWS Regions.

_S3 storage classes_
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/9080c265-6b53-414d-9d60-02c8e94fb92b)   

_storage management_
- S3 Lifecycle – Configure a lifecycle configuration to manage your objects and store them cost effectively throughout their lifecycle.
- S3 Object Lock – Prevent Amazon S3 objects from being deleted or overwritten for a fixed amount of time or indefinitely.
- S3 Replication – Replicate objects and their respective metadata and object tags to one or more destination buckets
- S3 Batch Operations – Manage billions of objects at scale with a single S3 API request or a few clicks in the Amazon S3 console

_How it works_
- An object is a file and any metadata that describes the file. A bucket is a container for objects.
- To store your data in Amazon S3, you first create a bucket and specify a bucket name and AWS Region. Then, you upload your data to that bucket as objects in Amazon S3. Each object has a key (or key name), which is the unique identifier for the object within the bucket.
- Every object is contained in a bucket. For example, if the object named photos/puppy.jpg is stored in the DOC-EXAMPLE-BUCKET bucket in the US West (Oregon) Region, then it is addressable by using the URL https://DOC-EXAMPLE-BUCKET.s3.us-west-2.amazonaws.com/photos/puppy.jpg   
DOC-EXAMPLE-BUCKET is the name of the bucket and photos/puppy.jpg is the key.
- can have up to 100 buckets in your account
- Versioning in Amazon S3 is a means of keeping multiple variants of an object in the same bucket. You can use the S3 Versioning feature to preserve, retrieve, and restore every version of every object stored in your buckets.
- Individual Amazon S3 objects can range in size from a minimum of 0 bytes to a maximum of 5 TB. The largest object that can be uploaded in a single PUT is 5 GB.
- The total volume of data and number of objects you can store in Amazon S3 are unlimited.

**Amazon S3 Glacier**
- Amazon S3 Glacier (S3 Glacier) is a secure and durable service for low-cost data archiving and long-term backup.
- S3 Glacier is a REST-based web service. In terms of REST, vaults and archives are the resources.
- In S3 Glacier, a vault is a container for storing archives. A vault is similar to an Amazon S3 bucket.
- An archive can be any data, such as a photo, video, or document. An archive is similar to an Amazon S3 object, and is the base unit of storage in S3 Glacier.
- ex. https://region-specific-endpoint/account-id/vaults/vault-name/archives/archive-id
- Retrieving archives and vault inventories (lists of archives) are asynchronous operations in S3 Glacier, in which you first initiate a job, and then download the job output after S3 Glacier completes the job.
- Because jobs take time to run, S3 Glacier supports a notification mechanism to notify you when a job is completed. You can configure a vault to send a notification to an Amazon Simple Notification Service (Amazon SNS) topic when a job is completed.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/1f2ac5eb-a45d-4c50-b56f-c288787088de)  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/95ab3c3b-df06-4e86-a16d-e65a86fcbf53)   
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/4f22ebd5-344e-4a83-9358-63192bad49e7)    

**Amazon Elastic Block Store (Amazon EBS)**
- block level storage volumes for use with EC2 instances. EBS volumes behave like raw, unformatted block devices. You can mount these volumes as devices on your instances.
- EBS volumes that are attached to an instance are exposed as storage volumes that persist independently from the life of the instance.
- EBS volumes are particularly well-suited for use as the primary storage for file systems, databases, or for any applications that require fine granular updates and access to raw, unformatted, block-level storage.
- Block storage provides low latency and high-performance values in various use cases. Its features are primarily useful for structured database storage, VM file system volumes, and high volumes of read and write loads. Object storage is best used for large amounts of unstructured data, especially when durability, unlimited storage, scalability, and complex metadata management are relevant factors for overall performance.
- Run relational or NoSQL databases: Oracle, Microsoft SQL Server, PostgreSQL, MySQL, Cassandra, and MongoDB etc...
- Right-size your big data analytics engines : Hadoop, Spark etc..
- Attach high-performance and high-availability block storage for mission-critical applications, on-premises storage area network (SAN workloads)
- EBS volumes: SSD, HDD etc....
- EBS snapshots:  You can back up the data on your Amazon EBS volumes to Amazon S3 by taking point-in-time snapshots. Snapshots are incremental backups, which means that only the blocks on the device that have changed after your most recent snapshot are saved.
- 
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/be64b5b0-ebc5-4569-b3c5-8d736654e7e1)  

**Amazon Elastic File System (EFS)**
- Amazon Elastic File System (EFS) automatically grows and shrinks as you add and remove files with no need for management or provisioning.
- managed file system designed for 99.999999999 percent (11 9s) durability and up to 99.99 percent (4 9s) of availability.
- Simplify persistent storage for modern content management system (CMS) workloads.
- Persist and share data from your AWS containers and serverless applications with zero
management required.
- Powerful combination of lambda serverless with EFS.
- Stateful microservices, allowing data to persist application state.
- Amazon Elastic File Service (EFS) is the solution you can use to provide users with NFS capabilities.

**Amazon S3 File Gateway**
- Store and access objects in Amazon S3 from NFS or SMB file data with local caching    
- File gateway, FsX file gateway, Tape gateway, Volume gateway 
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/0438ce41-073c-407a-875f-3c7e7d35b6cd)   

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/5e47f302-631d-4fa2-ad18-7d8fae42ac84)   

## AWS Networking Services   

**VPC (Amazon Virtual Private Cloud)**

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/c991b728-6052-4410-8f14-94104e24374b)    

- you can launch AWS resources in a logically isolated virtual network that you've defined.  
- A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone.
- Each subnet must be associated with a route table, which specifies the allowed routes for outbound traffic leaving the subnet.  
- You can assign IP addresses, both IPv4 and IPv6, to your VPCs and subnets.
- Use route tables to determine where network traffic from your subnet or gateway is directed.
- A gateway connects your VPC to another network. For example, use an internet gateway to connect your VPC to the internet. Use a VPC endpoint to connect to AWS services privately   
- An internet gateway enables resources in your public subnets (such as EC2 instances) to connect to the internet if the resource has a public IPv4 address or an IPv6 address. Similarly, resources on the internet can initiate a connection to resources in your subnet using the public IPv4 address or IPv6 address.  
- Use a VPC peering connection to route traffic between the resources in two VPCs.
_VPC PEERING CONNECTION_  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/4a888b9d-eecc-4b6e-9039-95eebcfb89de)     

- Use a transit gateway, which acts as a central hub, to route traffic between your VPCs, VPN connections, and AWS Direct Connect connections
_AWS TRANSIT GATEWAY_  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/d5f18a11-1c7e-4f66-99d9-2660c972ac85)   

- An Elastic IP address is a static, public IPv4 address designed for dynamic cloud computing. You can associate an Elastic IP address with any instance or network interface in any VPC in your account.
- A NAT gateway is a Network Address Translation (NAT) service. You can use a NAT gateway so that instances in a private subnet can connect to services outside your VPC but external services cannot initiate a connection with those instances. Each NAT gateway is created in a specific Availability Zone.
- Internet traffic from the instances in the private subnet is routed to the NAT instance, which then communicates with the internet. Therefore, the NAT instance must have internet access. It must be in a public subnet (a subnet that has a route table with a route to the internet gateway), and it must have a public IP address or an Elastic IP address.
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/bd27b072-7ad2-4e5c-8a6c-fdd12b40e57a)    

_Subnet types_
- Public subnet – The subnet has a direct route to an internet gateway. Resources in a public subnet can access the public internet.
- Private subnet – The subnet does not have a direct route to an internet gateway. Resources in a private subnet require a NAT device to access the public internet.
- The subnet has a route to a Site-to-Site VPN connection through a virtual private gateway. The subnet does not have a route to an internet gateway.
- Isolated subnet – The subnet has no routes to destinations outside its VPC. Resources in an isolated subnet can only access or be accessed by other resources in the same VPC.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/e0f049ac-e9b3-418b-959c-4c7841161588)   

**Security Groups**
- A security group controls the traffic that is allowed to reach and leave the resources that it is associated with. 
- A security group acts as a firewall that controls the traffic allowed to and from the resources in your virtual private cloud (VPC). You can choose the ports and protocols to allow for inbound traffic and for outbound traffic.  
- For example, after you associate a security group with an EC2 instance, it controls the inbound and outbound traffic for the instance.  
- The following table summarizes the basic differences between security groups and network ACLs.    
- When you first create a security group, it has no inbound rules, it has an outbound rule that allows all outbound traffic from the resource.   

_Network ACL_
- A network access control list (ACL) allows or denies specific inbound or outbound traffic at the subnet level.
-  By default, it allows all inbound and outbound IPv4 traffic and, if applicable, IPv6 traffic.

Security group	Network ACL   
Operates at the instance level	Operates at the subnet level  
Applies to an instance only if it is associated with the instance	Applies to all instances deployed in the associated subnet (providing an additional layer of defense if security group rules are too permissive)  
Supports allow rules only	Supports allow rules and deny rules  
Evaluates all rules before deciding whether to allow traffic	Evaluates rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic  
Stateful: Return traffic is allowed, regardless of the rules	Stateless: Return traffic must be explicitly allowed by the rules  

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/3a2718ee-be49-4969-9b35-03740e1b747f)   

**Route 53**

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/50941470-5dd2-4018-abdd-f630b93819e0)     

- Amazon Route 53 is a highly available and scalable Domain Name System (DNS) web service.
_In the following order:_ 
- Register domain names: Route 53 lets you register a name for your website or web application, known as a domain name.
- Route internet traffic to the resources for your domain: When a user opens a web browser and enters your domain name (example.com) or subdomain name (acme.example.com) in the address bar, Route 53 helps connect the browser with your website or web application.
- Check the health of your resources: Route 53 sends automated requests over the internet to a resource, such as a web server, to verify that it's reachable, available, and functional.   


- top-level domain (TLD): The last part of a domain name, such as .com, .org, or .ninja.
- The Domain Name System translates easily understood names such as example.com into the numbers, known as IP addresses, that allow computers to find each other on the internet.
- DNS resolver: A DNS server, often managed by an internet service provider (ISP), that acts as an intermediary between user requests and DNS name servers.
- A CIDR block is an IP range used with IP-based routing. In Route 53 You can specify CIDR block from /0 to /24 for IPv4 and/0 to /48 for IPv6.
- DNS record: An object in a hosted zone that you use to define how you want to route traffic for the domain or a subdomain. For example, you might create records for example.com and www.example.com that route traffic to a web server that has an IP address of 192.0.2.234.
- TTL (time to live): The amount of time, in seconds, that you want a DNS resolver to cache (store) the values for a record before submitting another request to Route 53  
_Multiple routing policy:_

Simple routing policy – Use to route internet traffic to a single resource that performs a given function for your domain, for example, a web server that serves content for the example.com website.  

Failover routing policy – Use when you want to configure active-passive failover.   

Geolocation routing policy – Use when you want to route internet traffic to your resources based on the location of your users.  

Geoproximity routing policy – Use when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another.   

Latency routing policy – Use when you have resources in multiple locations and you want to route traffic to the resource that provides the best latency.   

IP-based routing policy – Use when you want to route traffic based on the location of your users, and have the IP addresses that the traffic originates from.   

Multivalue answer routing policy – Use when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random.    

Weighted routing policy – Use to route traffic to multiple resources in proportions that you specify.    

**Amazon API Gateway**
- APIs act as the "front door" for applications to access data, business logic, or functionality from your backend services.
- fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale
- you can create RESTful APIs and WebSocket APIs that enable real-time two-way communication applications.

## AWS Databases Services

- AWS Database Migration Service (AWS DMS) is a managed migration and replication service that helps move your database and analytics workloads to AWS quickly, securely, and with minimal downtime and zero data loss.

**INSTALLED DATABASES ON EC2 VS MANAGED DATABASES**
- Amazon RDS enables you to run a fully featured relational database while offloading database administration. Whereas, for more control and flexibility, EC2 will be better for your relational database.
- The entire process of configuration, management, maintenance, and security is automated by AWS. RDS is easy to set up, cost-effective and allows you to focus on more important tasks.
- EC2 gives you full control over your database, OS and software stack. It allows you to hire your own database administrators. 
- Security (data at Rest, and at transit), Availibility, automated backups (snapshots), scalibility and performance comes out of the box with RDS, with EC2 everything has to be configured.
- Compatibility: RDS supports Aurora, SQL Server, MySQL, MariaDB, PostgreSQL, and Oracle. With EC2, you can configure any database you want.
- Preferred for EC2 reasons: More control on the configuration, High Performance: It allows you to exceed your maximum database size and performance needs.

**RDS**
- Deploy and scale the relational database engines of your choice in the cloud or on-premises.
- Achieve high availability with Amazon RDS Multi-AZ deployments.
- Amazon RDS database instances are preconfigured with parameters and settings appropriate for the engine and class you have selected.
- In a few steps, Blue/Green Deployments create a staging environment that mirrors the production environment and keeps the two environments in sync using logical replication
- The AWS Nitro System makes RDS Optimized Writes possible.
- When your RDS for MySQL database uses RDS Optimized Writes, it can achieve up to two times higher write transaction throughput.
- An RDS for MariaDB DB instance that uses RDS Optimized Reads can achieve up to 2x faster query processing compared to a DB instance that doesn't use it.
- A DB instance is an isolated database environment running in the cloud. It is the basic building block of Amazon RDS. A DB instance can contain multiple user-created databases.
- Blue/green deployment: A blue/green deployment creates a staging environment that copies the production environment. In a blue/green deployment, the blue environment is the current production environment. The green environment is the staging environment. The staging environment stays in sync with the current production environment using logical replication.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/519b7914-cd76-40fb-a179-0353dc95f7cc)  
- Read Replicas make it easier to elastically scale out beyond the capacity constraints of a single DB instance for read-heavy database workloads. 
- By default, Amazon RDS creates and saves automated backups of your DB instance securely in Amazon S3 for a user-specified retention period.
- In an Amazon RDS Multi-AZ deployment, Amazon RDS automatically creates a primary database (DB) instance and synchronously replicates the data to an instance in a different AZ. When it detects a failure, Amazon RDS automatically fails over to a standby instance without manual intervention.
- Multi-Az: Two types: one standby replica, two standby replicas 

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/e91d3802-8813-4296-bbac-aa524c546877)    

- Amazon RDS allows you to encrypt your databases using keys you manage through AWS Key Management Service (KMS). Amazon RDS supports the use of SSL to secure data in transit.
- Amazon RDS provides Amazon CloudWatch metrics for your database instances.


_Amazon Aurora_
- Power performance-intensive applications and critical workloads while maintaining full compatibility with MySQL and PostgreSQL
- Aurora gives you the performance and availability of commercial-grade databases at one-tenth the cost.
- 5x faster than mysql, 3x faster than postgresql
- Amazon Aurora provides built-in security, continuous backups, serverless compute, up to 15 read replicas, automated multi-Region replication  

**DYNAMODB**
- Fast, flexible NoSQL database service for single-digit millisecond performance at any scale
- Create data schemas and tables in DynamoDB using sample data model templates and datasets available in NoSQL Workbench.
- Use PartiQL, a SQL-compatible query language, to query, insert, update, and delete table data in DynamoDB.
- DynamoDB supports both key-value and document data models. This enables DynamoDB to have a flexible schema, so each row can have any number of columns at any point in time.
- DynamoDB Accelerator (DAX) is an in-memory cache that delivers fast read performance: taking the time required for reads from milliseconds to microseconds
- DynamoDB provides native, server-side support for transactions
- DynamoDB supports high-traffic, extreme-scaled events and can handle millions of queries per second.

**REDSHIFT**
- Best price-performance for cloud data warehousing
- Amazon Redshift uses SQL to analyze structured and semi-structured data across data warehouses, operational databases, and data lakes
- Run and scale analytics in seconds on all your data without having to manage your data warehouse infrastructure.
- Query editor to run queries and share it across team members 
- Build insight-driven reports and dashboards using Amazon QuickSight, Tableau, Microsoft PowerBI, or other business intelligence tools.
- Amazon Redshift also is optimized for high-performance batch analysis and reporting of datasets.
- Cluster – The core infrastructure component of an Amazon Redshift data warehouse is a cluster. A cluster is composed of one or more compute nodes. The compute nodes run the compiled code. he leader node handles external communication with applications, such as business intelligence tools and query editors.
- Database – A cluster contains one or more databases. User data is stored in one or more databases on the compute nodes. Your SQL client communicates with the leader node, which in turn coordinates running queries with the compute nodes.

_data ingestion layer_: different types of data sources continuously upload structured, semistructured, or unstructured data to the data storage layer.
_data processing layer_: the source data goes through preprocessing, validation, and transformation using extract, transform, load (ETL) or extract, load, transform (ELT) pipelines
_data consumption layer_: data is loaded into your Amazon Redshift cluster, where you can run analytical workloads.  

**Amazon ElastiCache** 
- Realize microsecond response times across hundreds of millions of operations per second and up to 1 pebibyte of data
- Achieve cost-optimized performance by adding a cache for frequently read data to optimize resources and lower total cost of ownership
- Build applications quickly using popular open-source technologies, Redis and Memcached  

----------------------------------------------------------------------------------------------------------------------------  

## technology support

- there is documentation (best practices, whitepapers, AWS Knowledge Center, forums, blogs
- includes AWS Official Knowledge Center articles and videos covering the most frequent questions and requests that we receive from AWS customers.

**AWS Support**   
- The AWS Trust & Safety team can assist you when AWS resources are implicated in the following abuse types:
- Web content/non-copyright intellectual property that's objectionable content hosted on an AWS resource
- Email abuse that's an abusive email sent from an AWS resource or spam content hosted on, or sent from an AWS resource.
- Network activity that's originating from an AWS resource that causes problematic network traffic. This can be an intrusion attempt, denial-of-service (DoS) attack, port scanning, or any other abusive network activity.
- Copyright that's subject to content removal requests regarding the Digital Millennium Copyright Act.

In the AWS Management Console, you can create three types of customer cases in AWS Support:
- Account and billing
- Service limit increase requests are available to all AWS customers
- Technical support cases connect you to technical support for help with service-related technical issues 

**AWS premium support**:   
- A Technical Account Manager (TAM) provides consultative architectural and operational guidance delivered in the context of your applications and use-cases to help you achieve the greatest value from AWS. The TAM will work with you to provide tailored engagements including strategic Business Reviews, Security Improvement Programs, guided Well-Architected reviews, Cost Optimization workshops, and a range of proactive services.
- Get expert guidance and assistance achieving your objectives

**Types of Support plans**:   
- Developer: Recommended if you are experimenting or testing in AWS. Business hours** web access to Cloud Support Associates. System impaired: < 12 hours**
- Business: Minimum recommended tier if you have production workloads in AWS. 24/7 phone, web, and chat access to Cloud Support Engineers. Production system down: < 1 hour
- Enterprise on-ramp: Recommended if you have production and/or business critical workloads in AWS. 24/7 phone, web, and chat access to Cloud Support Engineers. Business-critical system down: < 30 minutes. Technical Account Management	
- Enterprise: Recommended if you have business and/or mission critical workloads in AWS. 24/7 phone, web, and chat access to Cloud Support Engineers. Business/Mission-critical system down: < 15 minutes. Access to AWS Incident Detection and Response for an additional fee. Technical Account Management	

**AWS Partner network**   
- The AWS Partner Network (APN) is a global community of partners that leverages programs, expertise, and resources to build, market, and sell customer offerings.
- As an AWS Partner, you are uniquely positioned to help customers take full advantage of all that AWS has to offer and accelerate their journey to the cloud.
- Independent Software Vendors (ISVs) and Channel Partners can take advantage of AWS Marketplace Channel features and enablement to build a scalable Marketplace business with AWS
- AWS Marketplace is a curated digital catalog that customers can use to find, buy, deploy, and manage third-party software, data, and services to build solutions and run their businesses
- You can use AWS Marketplace as a buyer (subscriber), seller (provider), or both.

**AWS Trusted Advisor**   
- AWS Trusted Advisor provides recommendations that help you follow AWS best practices.  
- These checks identify ways to optimize your AWS infrastructure, improve security and performance, reduce costs, and monitor service quotas
- AWS Basic Support and AWS Developer Support customers can access core security checks and checks for service quotas. AWS Business Support and AWS Enterprise Support customers can access all checks, including cost optimization, security, fault tolerance, performance, and service quotas.
- 
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/b386ad36-ad21-4b88-b1f4-15c3968f9c71)   
