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

