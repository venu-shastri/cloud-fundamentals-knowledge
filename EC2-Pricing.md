# AWS EC2 Pricing: The Ultimate Guide

### How is AWS EC2 Priced?

Amazon Elastic Compute Cloud (Amazon EC2) provides cloud-based compute resources, designed especially for scalability. The service comes with a user-friendly interface that provides complete control over cloud resources, which are provisioned using EC2 instances. 

An EC2 instance acts as a virtual server hosted in the Amazon Web Services (AWS) cloud. There are many types of EC2 instances, each can be customized to the unique needs of the operation, using various operating systems (OS) and applications. 

Each EC2 instance type is priced differently, but there are other, additional, aspects that determine AWS EC2 pricing. Pricing tiers and models, for example, can significantly impact billing charges, as well as optimization features like Amazon EC2 Auto Scaling and AWS Compute Optimizer.

### Amazon EC2 Instance Pricing Models

- EC2 Free Tier
- EC2 On-Demand
- Spot Instances
- Reserved Instances (RIs)
- Dedicated Hosts

- Amazon EC2 Cost Components
  Estimating Costs with the EC2 Pricing Calculator
  4 Ways to Save on Amazon EC2
  AWS Savings Plans
  Saving Plans vs EC2 RI
  Amazon EC2 Auto Scaling
  AWS Compute Optimizer
  Leveraging EC2 Spot Instances with Spot by NetApp
  Amazon EC2 Instance Pricing Models
  AWS EC2 pricing gives you many instance types to choose from, as well as several pricing models that can help optimize your billing.

### EC2 Free Tier

Amazon offers new users a chance to check out various AWS services, free of charge, for up to 12 months. EC2 users with a Free Tier account can get 750 hours per month. 

The free tier provides t2.micro instances (or t3.micro for the regions in which t2.micro is unavailable), including Windows, Linux, RHEL, or SLES. You can opt to use mainly micro instances, to ensure you do not exceed the capacity offered by the free tier.

### EC2 On-Demand

EC2 offers an on-demand pricing model, which charges only for compute capacity usage. You can choose between billing per hour or per second, and pricing varies between instance types and regions. On-demand pricing eliminates long term commitments and upfront payments, providing a high level of scalability.

On-demand instances let you easily increase and decrease compute capacity, and are highly recommended for short-term workloads or operations experiencing frequent and unpredictable spikes in demand. You can also leverage on-demand instances for software development and testing.

### Spot Instances

EC2 spot instances let you request spare EC2 capacity, and pay significantly less (up to 90% off) the original on-demand price. Because they can be interrupted on short notice, spot instances are typically used for applications working at flexible start and end schedules, or to accommodate urgent spikes in demand for compute resources.  

### Reserved Instances (RIs)

Reserved instances can provide as much as 72% in savings. You can use RIs to significantly reduce your overall computing costs, in exchange for committing to use AWS EC2 for a long period of time (1 or 3 year terms). 

RIs are typically used for applications that operate with steady state usage. You can select RIs with Regional Scope, which lets you change the availability zone (AZ) and instance type over time, but does not reserve capacity. Alternatively, RIs can have Zonal Scope, which reserves capacity, but does not provide flexibility over AZ and instance type.

### Dedicated Hosts

Dedicated Hosts provide you with physical EC2 servers, which are entirely dedicated to your workloads. Dedicated Hosts let you use your own existing server-bound software licensing, including SQL Server, SUSE Linux Enterprise Server, and Windows Server. 

Using your own dedicated server and license can reduce your costs and help you meet compliance requirements. However, you should make sure that all of your existing license terms are compatible with the environment. 

### Amazon EC2 Cost Components

When you start estimating Amazon EC2 costs, you need to account for the following aspects:

- Clock hours of server time—EC2 resources start incurring charges once they are running. For example, billing starts from the time your EC2 instances are launched until the time the instances are terminated. Instances can also incur charges from the time the Elastic IP address is allocated until it is de-allocated.
- Instance type—instance types are composed of different combinations of resources, including central processing unit (CPU), memory, networking, and storage. Additionally, instance types can be scaled according to size, letting you customize resources according to the requirements of your workload.
- Number of instances—AWS EC2 lets you provision multiple instances, and pricing depends on the number of instances you run at any point in time.
- Load balancing—AWS offers a feature called Elastic Load Balancing, which lets you distribute traffic across EC2 Instances. The total number of hours during which Elastic Load Balancing runs contributes towards your monthly overall costs.
- Detailed monitoring—EC2 can integrate with Amazon CloudWatch, which provides capabilities for monitoring your instances. The default setup provides basic monitoring. However, you can also add detailed monitoring capabilities, which are charged at a fixed monthly rate.
- Elastic IP addresses—AWS provides one Elastic IP address for each running instance, at no additional charge.
  Licensing—AWS enables you to either obtain a software license from AWS or bring your own license. AWS licenses are fully compliant and are charged on a “pay as you go” basis. You can also use your own existing licenses and reduce total cost of ownership (TCO), but only if the agreements are compatible with the cloud. You can use AWS License Manager to manage your software licenses.

###  Estimating Costs with the EC2 Pricing Calculator

The AWS Pricing Calculator can help you estimate the costs of various AWS services. Before building your solution, you can explore price points for your model, calculate an estimated cost, and determine which contract terms and instance types suit your model best.

You can generate Amazon EC2 estimates using two methods:

- The quick estimate path—provides quick, but rough, cost estimates.
- The advanced estimate path—provides detailed cost estimates, accounting for data transfer and workload costs, additional storage types, and checks less common instance requirements. 
