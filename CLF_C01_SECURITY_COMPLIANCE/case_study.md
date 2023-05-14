* Applying the AWS Shared Responsibility Model in Practice  
Customer responsibility varies based on many factors, including the AWS services and Regions they choose, the integration of those services into their IT environment, and the laws and regulations applicable to their organization and workload.
** AWS Cloud Adoption Framework (AWS CAF)
- AWS Cloud Adoption Framework (AWS CAF) leverages AWS experience and best practices to help you digitally transform and accelerate your business outcomes through innovative use of AWS. AWS CAF groups its capabilities in six perspectives: Business, People, Governance, Platform, Security, and Operations.
- Review the security functionality and configuration options of individual AWS services within the security chapters of AWS service documentation.
- Determine external and internal security and related compliance requirements and objectives, and consider industry frameworks like the NIST Cybersecurity Framework (CSF) and ISO.
- The National Institute of Standards and Technology (NIST) 800-53 security controls are generally applicable to US Federal Information Systems.  AWS has received FedRAMP Authorizations to Operate (ATO) from multiple authorizing agencies for both AWS GovCloud (US) and the AWS US East/West Region.
- Provide your internal and external audit teams with cloud-specific learning opportunities by leveraging the Cloud Audit Academy training programs.
- Perform a Well-Architected Review of your AWS workloads to evaluate the implementation of best practices for security, reliability, and performance.
- Explore solutions available in the AWS Marketplace digital catalog with thousands of software listings from independent software vendors that enable you to find, test, buy, and deploy software that runs on AWS.
- Explore AWS Security Competency Partners offering expertise and proven customer success securing every stage of cloud adoption, from initial migration through ongoing day-to-day management

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/ee81511b-2ef9-4960-b8e6-28bd0f06750b)

Shared responsibility for NIST (National Institute of Standards and Technology)
Shared Responsibility: You will provide security and configurations of your software components and AWS will provide security for its infrastructure.
Customer-Only Responsibility: You are fully responsible for guest operating systems, deployed applications, and select networking resources (for example, firewalls). More specifically, you are solely responsible for configuring and managing your security in the cloud.
AWS-Only Responsibility: AWS manages the cloud infrastructure, including the network, data storage, system resources, data centers, physical security, reliability, and supporting hardware and software. Applications built on top of the AWS system inherit the features and configurable options that AWS provides. AWS is solely responsible for configuring and managing security of the cloud.

AWS has certification for compliance with ISO/IEC 27001:2013, 27017:2015, 27018:2019, 27701:2019, 22301:2019, 9001:2015, and CSA STAR CCM v4.0.

Shared responsbility model and how it changes based on services : 

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/9b9f9623-2107-444c-a698-4bc0a8273f86)  
  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/e8c3322a-eb23-4986-9fcb-3114acf1d561)

=============================================

* AWS Artifact
- Access AWS and ISV security and compliance reports
Use AWS Artifact reports to access several compliance reports from third-party auditors who have tested and verified our compliance with a variety of global, regional, and industry specific security standards and regulations.

* AWS Compliance Programs
- The AWS Compliance Program helps customers to understand the robust controls in place at AWS to maintain security and compliance of the cloud.
- Place to find all compliance related information 

** HIPPA (The Health Insurance Portability and Accountability Act)
- is legislation that is designed to make it easier for US workers to retain health insurance coverage when they change or lose their jobs. The legislation also seeks to encourage electronic health records to improve the efficiency and quality of the US healthcare system through improved information sharing.
- Along with increasing the use of electronic medical records, HIPAA includes provisions to protect the security and privacy of protected health information (PHI). PHI includes a very wide set of personally identifiable health and health-related data, including insurance and billing information, diagnosis data, clinical care data, and lab results such as images and test results.
- There is no HIPAA certification for a cloud service provider (CSP) such as AWS. In order to meet the HIPAA requirements applicable to our operating model, AWS aligns our HIPAA risk management program with FedRAMP and NIST 800-53, which are higher security standards that map to the HIPAA Security Rule.

** AWS SOC (AWS System and Organization Controls)
- Reports are independent third-party examination reports that demonstrate how AWS achieves key compliance controls and objectives. The purpose of these reports is to help you and your auditors understand the AWS controls established to support operations and compliance.

 At a high level, describe how customers achieve compliance on AWS

- AWS Audit Manager : Continuously audit your AWS usage to simplify how you assess risk and compliance with regulations and industry standards
- Amazon GuardDuty: Protect your AWS accounts and workloads with intelligent threat detection and continuous monitoring
- Amazon Artifact: No cost, self-service portal for on-demand access to AWS’ compliance reports
- Amazon Data Centers: Learn about our security approach to protect the data of millions of active monthly customers

AWS gives you control that can help you comply with the regional and
local data privacy laws and regulations applicable to your organization.
The design of our global infrastructure allows you to retain complete
control over the locations in which your data is physically stored,
which can help you meet data residency requirements. 

Reduce risk and enable growth by using our activity monitoring
services that detect configuration changes and security events across
your system, even integrating our services with your existing solutions
to help simplify your operations and compliance reporting. 

Ensure that your resources have the right level of access at all times by
leveraging fine-grain identity and access controls and continuous
monitoring for near real-time security information – regardless of
where your information in stored. 

You retain complete control over which AWS Region(s) your data is physically stored in, which can
help you meet your compliance and data residency requirements. For example, if you are a
European customer, you can choose to deploy your AWS services exclusively in the EU (Frankfurt)
Region. If you make this choice, your content will be exclusively stored in Germany unless you
select a different AWS Region. 

===================================================
Data Encryption

- Data at rest encryption capabilities available in most AWS services, such as Amazon EBS, Amazon S3, Amazon RDS, Amazon Redshift, Amazon ElastiCache, AWS Lambda, and Amazon SageMaker
- Flexible key management options, including AWS Key Management Service, that allow you to choose whether to have AWS manage the encryption keys or enable you to keep complete control over your own keys
- Dedicated, hardware-based cryptographic key storage using AWS CloudHSM, allowing you to help satisfy your compliance requirements
- Encrypted message queues for the transmission of sensitive data using server-side encryption (SSE) for Amazon SQS
- In addition, AWS provides APIs for you to integrate encryption and data protection with any of the services you develop or deploy in an AWS environment.

ategory	What is it	AWS service
Identity and access management	Securely manage identities and access to AWS services and resources  	AWS Identity and Access Management (IAM)
- Apply fine-grained permissions and scale with attribute-based access control, Manage per-account access or scale access across AWS accounts and applications, 

Centrally manage workforce access to multiple AWS accounts and applications	AWS IAM Identity Center (successor to SSO)
- Enable multi-account access to your AWS accounts, Enable single sign-on access to your AWS applications 

AWS ACCOUNTS AND ORGANIZATIONS BEST PRACTICES : 
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/de330689-ef8c-4fd2-bdfc-1d08cf869586)

AWS IAM VS IDENTIY CENTER 

AWS Identity and Access Management enables admins to manage access to AWS services and resources within an AWS account securely for what it calls “entities” — IAM users created from the AWS IAM admin console, federated users, application code, or another AWS service.

AWS IAM Identity Center manages access for all AWS accounts within an AWS Organization, as well as access to other cloud applications, e.g., Salesforce. AWS IAM Identity Center includes a user portal where end users can find and access their assigned AWS accounts, cloud applications, and custom applications in one place.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/a50fc633-1154-4a95-b1f6-7c25dc5d38e7)


Implement secure, frictionless customer identity and access management (CIAM) that scales	Amazon Cognito
- Engage customers: Allow customers to sign in directly, or through social or enterprise identity providers, to a hosted UI with your branding.
- Manage B2B identities: Use a variety of multi-tenancy options that provide different levels of policy and tenant isolation for your business.
- Secure machine-to-machine authentication: Develop modern, secure, microservice-based applications, and more easily connect your application to backend resources and web services.
- Get role-based access to AWS resources: Gain secure, role-based access to AWS services, such as Amazon S3, Amazon DynamoDB, and AWS Lambda.

Manage fine-grained permissions and authorization within custom applications	Amazon Verified Permissions (preview)
- gave developers provide the way to define their own permissions model using **cedar** policy

Gain efficiency with a fully managed Microsoft Active Directory service	AWS Directory Service
- Integrate your on-premises credentials

Simply and securely share your AWS resources across multiple accounts	AWS Resource Access Manager (AWS RAM)
- Share resources in multi-account environments

Centrally manage your environment as you scale your AWS resources	AWS Organizations
- Automate AWS account creation
- Enable proactive protection with a dedicated security group

Detection
Automate AWS security checks and centralize security alerts	AWS Security Hub
- Conduct Cloud Security Posture Management (CSPM), Security scanning, Triage and prioritize security issues, Correlate your security findings to discover new insights, Initiate Security Orchestration, Automation, and Response (SOAR) workflows

Protect AWS accounts with intelligent threat detection	Amazon GuardDuty
- Improve security operations visibility: unknonwn IP malicious, suspicious logins, unusual data access;
- Identify files containing malware: scan EBS 
- Identify and profile possible malicious or suspicious behavior in container workloads by analyzing Amazon EKS audit logs and container runtime activity.

Automated and continual vulnerability management at scale	Amazon Inspector
- Quickly discover vulnerabilities, Use up-to-date common vulnerabilities and exposures (CVE), Support compliance requirements and best practices for NIST CSF, PCI DSS; Identify zero-day vulnerabilities sooner
- Mean Time to Respond (MTTR) : Accelerate MTTR

Automatically centralize your security data in a few steps 	Amazon Security Lake (Preview)
- Analyze multiple years of security data quickly, Support on-demand analysis of petabyte-scale data

Assess, audit, and evaluate configurations of your resources	AWS Config
- Discover resources that exist in your account or publish the configuration data of third-party resources into AWS Config, record their configurations, and capture any changes
- Codify your compliance requirements as AWS Config rules and author remediation actions, automating the assessment of your resource configurations across your organization. (compliance as a code)
- Continually audit security monitoring and analysis  

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/294f56e2-6985-4be4-a055-bbd4e651c0e3)  

Observe and monitor resources and applications on AWS, on premises, and on other clouds	Amazon CloudWatch
- Visualize performance data, create alarms, and correlate data to understand and resolve the root cause of performance issues in your AWS resources.
- Analyze metrics, logs, logs analytics, and user requests to speed up debugging and reduce overall mean time to resolution.
- Find out exactly when your website is impacted and for how long by viewing screenshots, logs, and web requests at any point in time.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/c64bda19-d37f-4308-9248-7cd6e2cbd793)


Track user activity and API usage	AWS CloudTrail
- Audit activity: Monitor, store, and validate activity events for authenticity.
- Identify security incidents: Detect unauthorized access using the Who, What, and When information in CloudTrail Events.
- Troubleshoot operational issues: Continuously monitor API usage history using machine learning (ML) models to spot unusual activity in your AWS accounts, and determine root cause.
- prove compliance with regulations such as SOC, PCI, and HIPAA.
- Improve your security posture by recording user activity and events, and set up automated workflow rules with Amazon EventBridge.

Security management across your IoT devices and fleets	AWS IoT Device Defender
- Audit the security posture of IoT resources across your device fleet to easily identify gaps and vulnerabilities.
- Detect the use of insecure network services and protocols with known security weaknesses,

Network and application protection	Centrally configure and manage firewall rules across your accounts	AWS Firewall Manager
- Deploy managed rules, such as pre-configured WAF rules on your applications, across accounts.

Deploy network firewall security across your VPCs	AWS Network Firewall
- Inspect inbound internet traffic
- Filter outbound traffic
- Secure Direct Connect and VPN traffic from client devices and your on-premises environments supported by AWS Transit Gateway.

Maximize application availability and responsiveness with managed DDoS protection	AWS Shield
- Protect applications and APIs from SYN floods, UDP floods, or other reflection attacks.
- AWS automatically mitigates network and transport layer (layer 3 and layer 4) Distributed Denial of Service (DDoS) attacks.
- For application layer (layer 7) DDoS attacks, AWS attempts to detect and notify AWS Shield Advanced customers through CloudWatch alarms. By default, it doesn't automatically apply mitigations, to avoid inadvertently blocking valid user traffic.
- The SRT (Shield Response Team (SRT)) helps you triage the DDoS attack to identify attack signatures and patterns. With your consent, the SRT creates and deploys AWS WAF rules to mitigate the attack.

Provide secure access to corporate applications without a VPN	AWS Verified Access (Preview)
- verified each request with access token in real time as per rules defined 

Protect your web applications from common exploits	AWS Web Application Firewall (WAF)
- you can create security rules that control bot traffic and block common attack patterns such as SQL injection or cross-site scripting (XSS).
- Create rules to filter web requests based on conditions such as IP addresses, HTTP headers and body, or custom URIs.

Filter and control outbound DNS traffic for your VPCs	Amazon Route 53 Resolver DNS Firewall

Data protection	Discover and protect your sensitive data at scale	Amazon Macie
- machine learning (ML) and pattern matching to discover and help protect your sensitive data.

Create and control keys to encrypt or digitally sign your data	AWS Key Management Service (AWS KMS)
- Encrypt data within your applications with the AWS Encryption SDK data encryption library.
- Perform signing operations using asymmetric key pairs to validate digital signatures.
- Securely generate hash-based message authentication codes (HMACs) that ensure message integrity and authenticity.
- Protect your data at rest

Manage single-tenant hardware security modules (HSMs) on AWS	AWS CloudHSM


Provision and manage SSL/TLS certificates with AWS services and connected resources	AWS Certificate Manager
- to provision, manage, and deploy public and private SSL/TLS certificates for use with AWS services and your internal connected resources. ACM removes the time-consuming manual process of purchasing, uploading, and renewing SSL/TLS certificates.
- 

Create private certificates to identify resources and protect data	AWS Private Certificate Authority 
- AWS Private CA) is a highly available, versatile CA that helps organizations secure their applications and devices using private certificates.

Centrally manage the lifecycle of secrets	AWS Secrets Manager
- Securely encrypt and centrally audit secrets such as database credentials and API keys.
- Rotate secrets automatically to meet your security and compliance requirements.
- Centrally store and manage credentials, API keys, and other secrets.

Incident response	Analyze and visualize security data to investigate potential security issues	Amazon Detective
- Analyze and visualize security data to investigate potential security issues
- Determine the extent of malicious activity, its impact, and the underlying cause by analyzing relevant historical activities for patterns.

Scalable, cost-effective application recovery to AWS	AWS Elastic Disaster Recovery
- Quickly recover operations after unexpected events such as software issues or datacenter hardware failures. AWS DRS enables RPOs of seconds and RTOs of minutes.

Compliance	No cost, self-service portal for on-demand access to AWS’ compliance reports	AWS Artifact
- Find auditor-issued reports, certifications, accreditations, and other third-party attestations of AWS in a comprehensive resource.
- Review, accept, and manage your agreements with AWS
- Perform due-diligence of ISVs that sell products on AWS Marketplace, with on-demand access to their security and compliance reports.

Continually audit your AWS usage to simplify risk and compliance assessment	AWS Audit Manager
- Automatically collect evidence, monitor your compliance posture, and proactively reduce risk by fine-tuning your controls.
- Avoid the need to collect, review, and manage evidence with automated evidence collection.

==============================================================================

AWS IAM IN DETAIL

When you create an AWS account, you begin with one sign-in identity that has complete access to all AWS services and resources in the account. This identity is called the AWS account root user and is accessed by signing in with the email address and password that you used to create the account. 

- Set and manage guardrails and fine-grained access controls for your workforce and workloads.
- Manage identities across single AWS accounts or centrally connect identities to multiple AWS accounts.
- Grant temporary security credentials for workloads that access your AWS resources.
- Continually analyze access to right-size permissions on the journey to least privilege.


Attribute-Based Access Control (ABAC) : authorization strategy that lets you create fine-grained permissions based on user attributes, such as department, job role, and team name. With ABAC, multiple users using the same IAM role can still get unique, fine-grained access because permissions are based on user attributes. 

A tag is a custom attribute label that you can assign to an AWS resource. Each tag has two parts:
A tag key (for example, CostCenter, Environment, Project, or Purpose). Tag keys are case sensitive.
An optional field known as a tag value (for example, 111122223333, Production, or a team name). Omitting the tag value is the same as using an empty string. Like tag keys, tag values are case sensitive.


** Temporary security credentials: You can use the AWS Security Token Service (AWS STS) to create and provide trusted users with temporary security credentials that can control access to your AWS resources.

- Access keys are long-term credentials for an IAM user or the AWS account root user. You can use access keys to sign programmatic requests to the AWS CLI or AWS API
Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY). You must use both the access key ID and secret access key together to authenticate your requests.

- You can set a custom password policy on your AWS account to specify complexity requirements and mandatory rotation periods for your IAM users' passwords. 
If you don't set a custom password policy, IAM user passwords must meet the default AWS password policy. The IAM password policy does not apply to the AWS account root user password or IAM user access keys. 
If a password expires, the IAM user can't sign in to the AWS Management Console but can continue to use their access keys. 

The default password policy enforces the following conditions:

Minimum password length of 8 characters and a maximum length of 128 characters

Minimum of three of the following mix of character types: uppercase, lowercase, numbers, and non-alphanumeric character (! @ # $ % ^ & * ( ) _ + - = [ ] { } | ')
Not be identical to your AWS account name or email address
Never expire password

You can't create a "lockout policy" to lock a user out of the account after a specified number of failed sign-in attempts.


MFA 

for scenarios in which you need an IAM user or root user in your account, require MFA for additional security. With MFA, users have a device that generates a response to an authentication challenge. Each user's credentials and device-generated response are required to complete the sign-in process.

You can enable MFA for the AWS account root user and IAM users. When you enable MFA for the root user, it affects only the root user credentials. 
IAM users in the account are distinct identities with their own credentials, and each identity has its own MFA configuration. 
You can register up to eight MFA devices of any combination of the currently supported MFA types with your AWS account root user and IAM users. 

How to acheive it ?

- FIDO security key – FIDO Certified hardware security keys are provided by third-party providers.: Public key cryptography
- Virtual MFA devices – A virtual authenticator application that runs on a phone or other device and emulates a physical device. Virtual authenticator apps implement the time-based one-time password (TOTP) algorithm and support multiple tokens on a single device. The user must type a valid code from the device on a second webpage during sign-in.
- A hardware device that generates a six-digit numeric code based on the time-based one-time password (TOTP) algorithm. The user must type a valid code from the device on a second webpage during sign-in.


IAM terms : 

An AWS Identity and Access Management (IAM) user is an entity that you create in AWS. The IAM user represents the human user or workload who uses the IAM user to interact with AWS.
An IAM user with administrator permissions is not the same thing as the AWS account root user.

An Amazon Resource Name (ARN) for the IAM user. You use the ARN when you need to uniquely identify the IAM user across all of AWS.

Each IAM user is associated with one and only one AWS account.'

An IAM role is an IAM identity that you can create in your account that has specific permissions. An IAM role is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS. However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it.


Roles can be used by the following:

An IAM user in the same AWS account as the role
An IAM user in a different AWS account than the role
A web service offered by AWS such as Amazon Elastic Compute Cloud (Amazon EC2)
An external user authenticated by an external identity provider (IdP) service that is compatible with SAML 2.0 or OpenID Connect, or a custom-built identity broker.

AWS service role: A service role is an IAM role that a service assumes to perform actions on your behalf. An IAM administrator can create, modify, and delete a service role from within IAM
AWS service role for an EC2 instance: This role is assigned to the EC2 instance when it is launched

A service-linked role is a unique type of IAM role that is linked directly to an AWS service. Service-linked roles are predefined by the service and include all the permissions that the service requires to call other AWS services on your behalf.

You manage access in AWS by creating policies and attaching them to IAM identities or AWS resources.
During authorization, the AWS enforcement code uses values from the request context to check for matching policies and determine whether to allow or deny the request.
AWS checks each policy that applies to the context of the request. If a single policy denies the request, AWS denies the entire request and stops evaluating policies. This is called an explicit deny.

- An AWS managed policy is a standalone policy that is created and administered by AWS. Standalone policy means that the policy has its own Amazon Resource Name (ARN) that includes the policy name. 
AWS managed policies make it convenient for you to assign appropriate permissions to users, groups, and roles. It is faster than writing the policies yourself, and includes permissions for many common use cases. 
You cannot change the permissions defined in AWS managed policies. AWS occasionally updates the permissions defined in an AWS managed policy.

- You can create standalone policies in your own AWS account that you can attach to principal entities (users, groups, and roles). You create these customer managed policies for your specific use cases, and you can change and update them as often as you like.

- An inline policy is a policy created for a single IAM identity (a user, group, or role). Inline policies maintain a strict one-to-one relationship between a policy and an identity. They are deleted when you delete the identity. 

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/3a5c2692-522f-43c2-b215-6dcbb2007d9a)
The first Resource element specifies arn:aws:s3:::test for the ListBucket action so that applications can list all objects in the test bucket. The second Resource element specifies arn:aws:s3:::test/* for the GetObject, PutObject, and DeletObject actions so that applications can read, write, and delete any objects in the test bucket.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/b49044d6-c17a-4671-9019-bd042c34add4)
With the additional statement, users can view the test bucket by using the console. Without those permissions, access is denied. The console lists all buckets in the account, but users cannot view the contents of any other bucket. The read-write permissions are specified only for the test bucket, just like in the previous policy. If a user tries to view another bucket, access is denied.

Tasks that require root user credentials

- Change your account settings: This includes the account name, email address, root user password, and root user access keys
- Restore IAM user permissions.
- Activate IAM access to the Billing and Cost Management console.
- View certain tax invoices. 
- Close your AWS account.
- Register as a seller in the Reserved Instance Marketplace.
- Configure an Amazon S3 bucket to enable MFA (multi-factor authentication).
- Edit or delete an Amazon Simple Storage Service (Amazon S3) bucket policy 
- Sign up for AWS GovCloud (US). Request AWS GovCloud (US) account root user access keys from AWS Support.

One of the best ways to protect your account is to not have access keys for your AWS account root user.

==============================================================
AWS TRUSTED ADVISOR 

- Cost optimization:  Examples include identifying idle RDS DB instances, underutilized EBS volumes, unassociated Elastic IP addresses, and excessive timeouts in Lambda functions.
- Performance: Examples include analyzing EBS throughput and latency, compute usage of EC2 instances, and configurations on CloudFront.
- Security: Examples include identifying RDS security group access risk, exposed access keys, and unnecessary S3 bucket permissions.
- Fault tolerant: Examples include examining Auto scaling EC2 groups, deleted health checks on Route 53, disabled Availability Zones, and disabled RDS backups.
- Service Quotas: Trusted Advisor will notify you once you reach more than 80% of a service quota. 

A security group controls the traffic that is allowed to reach and leave the resources that it is associated with. For example, after you associate a security group with an EC2 instance, it controls the inbound and outbound traffic for the instance. You can associate a security group only with resources in the VPC for which it is created.
You can add rules to the security group for the load balancer to allow HTTP and HTTPS traffic from the internet. You can add rules to the security group for the web servers to allow traffic only from the load balancer. You can add rules to the security group for the database servers to allow only database requests from the web servers.

A network access control list (ACL) allows or denies specific inbound or outbound traffic at the subnet level.
Your VPC automatically comes with a modifiable default network ACL. By default, it allows all inbound and outbound IPv4 traffic and, if applicable, IPv6 traffic.
A network ACL has inbound rules and outbound rules. Each rule can either allow or deny traffic.
We evaluate the rules in order, starting with the lowest numbered rule, when deciding whether allow or deny traffic. If the traffic matches a rule, the rule is applied and we do not evaluate any additional rules.

The following are the parts of a network ACL rule: rule number, type, port, port range, source, destination, allow/deny 

Compare security groups and network ACLs
The following table summarizes the basic differences between security groups and network ACLs.

Security group	                | Network ACL
Operates at the instance level	| Operates at the subnet level
Applies to an instance only if it is associated with the instance	 | Applies to all instances deployed in the associated subnet (providing an additional layer of defense if security group rules are too permissive)
Supports allow rules only	| Supports allow rules and deny rules
Evaluates all rules before deciding whether to allow traffic	| Evaluates rules in order, starting with the lowest numbered rule, when deciding whether to allow traffic
Stateful: Return traffic is allowed, regardless of the rules	| Stateless: Return traffic must be explicitly allowed by the rules
 

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/432490b7-c98b-400e-a009-fc818b3345b9)

Strengthen your portfolio, predict risk, accelerate fraud detection, and augment advisory services all from a single destination, AWS Marketplace
Security orchestration, automation, and response (SOAR) paradigm
The AWS Knowledge Center helps answer the questions most frequently asked by AWS Support customers. 

An AWS system integrator has to play an important role in helping prospect customers/clients migrate. Specifically, the AWS system integrator role becomes vital when it comes to optimizing the work pressure on the AWS platform while dealing with things at a greater scale. An AWS system integrator role is to assist the customers of the concerned organization in terms of exploring AWS the best way.




