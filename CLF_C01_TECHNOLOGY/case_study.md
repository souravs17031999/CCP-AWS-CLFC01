* Technology

** methods of deploying and operating in the AWS Cloud:   
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


