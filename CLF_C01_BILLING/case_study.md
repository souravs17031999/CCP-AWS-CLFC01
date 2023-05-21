#  Billing and Pricing

## Pricing models 

**On-Demand**  
- On-Demand Instances let you pay for compute capacity by the hour or second with no long-term commitments. 
- recommended for 
- Users that prefer the low cost and flexibility of EC2 without any upfront payment or long-term commitment
- Applications with short-term, spiky, or unpredictable workloads that cannot be interrupted
- Applications being developed or tested on EC2 for the first time

**Amazon EC2 Spot Instances**  
- Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud and are available at a discount of up to 90% compared to On-Demand prices.
- recommended for 
- Fault tolerant or stateless workloads
- Applications that can run on heterogeneous hardware
- Applications that have flexible start and end times

**reserved capacity**
- Capacity Reservations enable you to reserve compute capacity for your EC2 instances in a specific Availability Zone for any duration. Capacity reservations mitigate against the risk of being unable to get On-Demand capacity in case of capacity constraints and ensure that you always have access to EC2 capacity when you need it, for as long as you need it.
- recommended for:
- Business-critical events or workloads that require capacity assurance
- Workloads that need to meet regulatory requirements for high availability
- Disaster recovery

**Per-second billing**   
- EC2 per-second billing removes the cost of unused minutes and seconds from your bill. Focus on improving your applications instead of maximizing hourly usage, especially for instances running over irregular time periods such as dev/testing, data processing, analytics, batch processing, and gaming applications.

**Reserved instances (Savings Plans)**  
- Reserved Instances are not physical instances, but rather a billing discount that is applied to the running On-Demand Instances in your account.
-  flexible pricing model that can help you reduce your bill by up to 72% compared to On-Demand prices, in exchange for a commitment to a consistent amount of usage (measured in $/hour) for a 1- or 3-year term.
-  recommended for:
- Committed and steady-state usage
- Users looking to innovate faster by using the newest instance families, generations, and Regions while continuing to save
- All Upfront, Partial Upfront, No upfront (requires billing history)
- When you purchase a Reserved Instance, you determine the scope of the Reserved Instance. The scope is either regional or zonal.

_Types of reserved instances_: 

- Standard and Convertible: 
- you can't exchange a Standard Reserved Instance. You can exchange Convertible Reserved Instances.
- You can modify Standard and Convertible Reserved Instances.
- A Standard Reserved Instance provides a more significant discount than a Convertible Reserved Instance

- Your RI applies to any instance in its family of its same size or smaller. For example, if you purchase an RI for an m3.large instance, the RI also applies to m3.medium instances.
- Multiple smaller RIs combine to apply to larger instances. For example, if you purchase two RIs for two m3.medium instances, these RIs also apply to an m3.large instance.
- RI discounts apply to accounts in an organization's consolidated billing family depending upon whether RI sharing is turned on or off for the accounts   
If RI sharing is turned on for an account in an organization, then:
- At least one account in the organization's consolidated billing family must be running an instance that matches the specifications of the RI for the discount to apply to the management account's bill.
- The discount for any RIs purchased on that account is applied to the combined usage for that instance type on the management account's bill.
- The RI discount applies to the total usage of the instance type for the full duration of the RI. The RI discount applies even if the purchasing member account is closed.
- The discount on the RIs purchased on a member account doesn't apply to the consolidated bill if the member account leaves the organization or is removed from the organization by the management account.
- The account that originally purchased the RI receives the discount first. If the purchasing account has no instances that match the terms of the RI, then the discount for the RI is assigned to any matching usage on another account in the organization.

If RI sharing is turned off for an account in an organization, then:
- RI discounts apply only to the account that purchased the RIs.
- RI discounts from other accounts in the organization's consolidated billing family don't apply.
- The charges accrued on that account are still added to the organization's consolidated bill and are paid by the management account.

**various account structures in relation to AWS billing and pricing**   

_Consolidated billing for AWS Organizations_ 
- You can use the consolidated billing feature in AWS Organizations to consolidate billing and payment for multiple AWS accounts or multiple Amazon Web Services India Private Limited (AWS India) accounts
- Every organization in AWS Organizations has a management account that pays the charges of all the member accounts.
- One bill, Easy tracking, Combined usage
- Volume discounts: For billing purposes, AWS treats all of the accounts in the organization as if they were one account. Some services, such as AWS Data Transfer and Amazon S3, have volume pricing tiers across certain usage dimensions that give you lower prices the more you use the service. 

**Benefits of multiple accounts**   
- you can align the ownership and decision making with those accounts and avoid dependencies and conflicts with how workloads in other accounts are secured and managed.
- Workloads often have distinct security profiles that require separate control policies and mechanisms to support them.
- When you limit sensitive data stores to an account that is built to manage it, you can more easily constrain the number of people and processes that can access and manage the data store. 
- If an issue occurs within one account, impacts to workloads contained in other accounts can be either reduced or eliminated.
- using different accounts for different business units and groups of workloads can help you more easily report, control, forecast, and budget your cloud expenditures.
- When you require fine-grained cost allocation, you can apply cost allocation tags to individual resources in each of your accounts.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/5f064a35-ead7-4efa-87e2-3a0221fffe3c)  

**Billing support**   

_AWS Price List API_
- This API provides you with access to prices in JSON and CSV form. You can download and process this information on an as-needed basis. You can also elect to receive notification via Amazon Simple Notification Service (Amazon SNS) each time we make a price change.

_AWS Pricing Calculator_
- web-based planning tool that you can use to create estimates for your AWS use cases. You can use it to model your solutions before building them, explore the AWS service price points, and review the calculations behind your estimates.
- Use groups to organize services together. You can add one or more services to each group. You can also use groups to organize your estimate in different ways. For example, you can organize your estimate by cost center, service stack, product architecture, or client.

_Product_pages_
- The Products page shows the applications, tools, and cloud resources that your administrator assigned to you. You can use the Products page to launch an instance of those products.

_AWS cost explorer_
- AWS Cost Explorer is a tool that enables you to view and analyze your costs and usage. You can explore your usage and costs using the main graph, the Cost Explorer cost and usage reports, or the Cost Explorer RI reports.
- forecast how much you're likely to spend for the next 12 months, and get recommendations for what Reserved Instances to purchase
- Identify trends in expenditure 

_AWS budgets_
- You can use AWS Budgets to track and take action on your AWS costs and usage. You can use AWS Budgets to monitor your aggregate utilization and coverage metrics for your Reserved Instances (RIs) or Savings Plans.

_AWS Cost and Usage reports (CUR)_
- The AWS Cost and Usage Reports (AWS CUR) contains the most comprehensive set of cost and usage data available. You can use Cost and Usage Reports to publish your AWS billing reports to an Amazon Simple Storage Service (Amazon S3) bucket that you own.
- AWS Cost and Usage Reports tracks your AWS usage and provides estimated charges associated with your account.

_Amazon QuickSight_
- Amazon QuickSight is a cloud-scale business intelligence (BI) service that you can use to deliver easy-to-understand insights to the people who you work with, wherever they are.
- In a single data dashboard, QuickSight can include AWS data, third-party data, big data, spreadsheet data, SaaS data, B2B data, and more.
- Saves you time and money with automated and customizable data insights, powered by machine learning (ML).   
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/04139eb5-a7a0-4dc9-908d-32ed8b8492b5)  

_AWS Managed Service Provider (MSP) Partner?_
- AWS Managed Service Providers (MSP) provide end-to-end AWS solutions to customers at any stage of the cloud journey—from consultation on initial solution design, to building applications, through to ongoing optimization and support.  
![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/fd6d4ddf-18f7-40ce-8aec-71520373bfcc)  

**Cost Allocation Via Tagging**  
- A tag is a label that you or AWS assigns to an AWS resource. Each tag consists of a key and a value.
-  You can use tags to organize your resources, and cost allocation tags to track your AWS costs on a detailed level.
-  The user-defined tags use the user prefix, and the AWS-generated tag uses the aws: prefix.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/226021a1-fdb1-41f9-8a90-6a1cc85dc0d9)   

- You can apply tags that represent business categories (such as cost centers, application names, or owners) to organize your costs across multiple services.

![image](https://github.com/souravs17031999/CCP-AWS-CLFC01/assets/33771969/82649295-4572-4fc5-bc6a-3ce5ef53dc48)  

**Billing Alarms**
- You can monitor your estimated AWS charges by using Amazon CloudWatch. When you enable the monitoring of estimated charges for your AWS account, the estimated charges are calculated and sent several times daily to CloudWatch as metric data.
- The alarm triggers when your account billing exceeds the threshold you specify. It triggers only when the current billing exceeds the threshold. It doesn't use projections based on your usage so far in the month.
- If you create a billing alarm at a time when your charges have already exceeded the threshold, the alarm goes to the ALARM state immediately.

