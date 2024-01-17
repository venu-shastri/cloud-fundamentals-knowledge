# Region


## Regions are independent from other, Data or information is not replicated from one region to another without explicit consent and authorization

## Contains-Cluster-of 

### Availability Zone(AZ)

- Contains-Cluster-of

	- DataCenter

		- Redundant Power

		- Networking

		- Connectivity

		- Operate in discrete facilities with undisclosed locations

		- Connected using high speed and low-latency links

- Addressed using code name

	- Us-east-1c

		- Resource is located in AZ c of the us-east-1 region

## Criteria

### Data Compliance

- Choose a region that meets companies compliance requirements

### Latency

- Choose a region that is close to user base

### Cost

- Pricing vary based on local economy and the physical nature of operating data centres

- Aws charges based on financial factors specific to the region

### Service Availability

- All services are not available in all regions

## Regions are geographic locations worldwide where AWS hosts its data centers.

## Each AWS Region is associated with a geographical name and a Region code


# Interacting With AWS


## Management Console

## AWS-CLI

## SDK(AWS Software Development Kits)


# IAM


## IAM Supports identity federation

## Identity and Access Management 

### A Service that manage access to AWS Account and Resources

## Every Access in AWS is “API” Call

### All Api Calls in AWS must be signed and authenticated

## IAM is global and not specific to region

## IAM Role

### Provide Permissions to identities that are federated from IDP(identity provider)

### Enables temporary access to AWS credentials

## 

### IAM supports MFA

## Authorization

### IAM Policy

- Grant or Deny Permission to specific Actions within AWS Account

- IAM policies are JSON documents

	- Major Elements

		- Version

		- Effect

			- Allow

			- Deby

		- Action

			- Specific Action that will be Allowed or Denied

		- Resource

			- Object /s that the policy covers

- Policy can be attached to an individual IAM User or Group

- Policy cannot be applied to the Root User


# User


## Root User

### Single Sign-in identity that has complete access to all AWS services and resources in the account

- First-time access only

### Has two sets of. Credentials 

- Email Address and Password 

	- Used to Access AWS Management Console

- Access Keys

	- Used to make Programmatic requests from the AWS CLI or AWS API

		- 

	- Parts of Keys

		- Key ID

		- Secret Access Key

### Protect Root User

- Choose a Strong Password 

- Never Engage Social Engineering

- Disable or Delete Access Keys Associated with the root user

	- Don’t create one unless you absolutely need to

- Don’t use root user for every day tasks

	- Administering Resources

- Assign MFA

	- Supported MFA Devices

		- Virtual MFA

			- Authenticator Apps

				- Authy , Microsoft Authenticator , Google Authenticator

		- Hardware

			- TOPT Token (one time six digit numeric code)

				- Key fob, Display Card

		- U2F (Universal Second Factor Security Keys)

			- USB Device

				- YubiKey

### When to use Root User Credentials ?

## IAM User

### Represents a Person or Service that interacts with AWS

### IAM users defined with in AWS Account

- Any Activity done by IAM user is billed to Account

### Has Name and Credentials

- UserName and Password

- Access Keys


# Compute as Service


## aws

### https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html

## Main types

### Virtual Machine

- Amazon Elastic Compute Cloud or Amazon EC2

	- AWS operates and manages the host machines and the hypervisor layer. AWS also installs the virtual machine operating system, called the guest operating system.

		- Amazon Machine Image (AMI)

			- Used to Create EC2 Instances

			- EC2 instances are placed in a network called the default Amazon Virtual Private Cloud (VPC).

			- purchasing options for EC2 instances

				- On Demand

				- Reserved

					- Payment Options

						- Up-front

						- Partial Up-front

						- No-upfront

				- Spot

					- Amazon EC2 Spot Instances allow you to take advantage of unused EC2 capacity in the AWS Cloud

### Container Services

### Server Less

- AWS Fargate

- AWS Lamda

	- Triggers

	- Under 15 minutes


# IP Address


## Notation

### IPV4 Notation

- 192.168.1.67

- 32 bits

### CIDR Notation

- Classless Inter-Domain Routing (CIDR) notation

- CIDR notation is a compressed way of specifying a range of IP addresses

- 192.168.1.0/24

	- In this example, the first 24 bits of the IP address are fixed. The rest are flexible

		- 32 - 24= 8 flexible bits

			- Providing 256 IP Addresses in that Range

- The higher the number after the /, the smaller the number of IP addresses in your network

	- For example, a range of 192.168.1.0/24 is smaller than 192.168.1.0/16

### AWS Cloud,  network size is choosen  using CIDR notation

- smallest IP range you can have is /28, which provides  16 IP addresses

- The largest IP range you can have is a /16, which provides  65,536 IP addresses


# VPC


## RouteTable

### Contains Set Of Rules Called Routes

### Determines Direction Of Network Traffic

### Applied at Subnet / VPC Level

## Subnet 

### Isolate or Optimise Network Traffic

### In Aws subnets are used for High Availability and Providing different connectivity options to resources

### Create Subnet

- VPC Name

- Availability Zone

- CIDR Block for Subnet

	- Should be subset of VPC CIDR Block

## gateway(Modem)

### internet Gateway

- Connects VPC to the internet

### Virtual Gateway

- VPN connection between VPC

## A VPC is an isolated network you create in the AWS cloud

## Create VPC

### Name

### Region

### Network Size (IP Range)

## Security

### Network Access Control List (ACL)

- Firewall @Subnet Level

### Security Groups

- Firewalls @EC2 Instance Level

## Reserved IPs

### Network Address

- 10.0.0.0

### VPC Local Router

- 10.0.0.1

### DNS Server

- 10.0.0.2

### Future Use

- 10.0.0.3

### Network Broadcast Address

- 10.0.3.255

### Ex: 10.0.0.0/22

- Total 1024 IP Addresses

- Divided in to 4 equal-sized subnets

- 10.0.0.0/24

	- 256 IP Range

## Each VPC Spans multiple Availability Zones within the Region

## CIDR Notation is used define IP Range

## Create VPC with IP range of /16 and create subnets with a IP range of /24


# Storage Types on AWS


## DynamoDB

### Fully managed NoSQL database service 

### Core Components

- table

	- A table is a collection of items, 

	- Item

		- each item is a collection of attributes

		- Attribute

			- fundamental data element

### DynamoDB uses primary keys to uniquely identify each item in a table and secondary indexes to provide more querying flexibility

### DynamoDB also offers encryption at rest

## Block Storage

###  Splits files into fixed-size chunks of data called blocks that have their own addresses.

### Outside of the address, there is no additional metadata 

### Block Storage solutions are fast and use less bandwidth.

### useCases

- Typical storage choice for high-performance enterprise workloads, such as databases or enterprise resource planning (ERP) systems, that require low-latency storage. 

### EBS

- External storage Attached to EC2 instance

- 1:1 mapping

- volume

	- hdd

		- Performance depends on MB/s.

		- Ideal for throughput-intensive workloads, such as big data, data warehouses, log processing, and sequential data I/O.

	- ssd

		- Performance depends on IOPS (input/output operations per second).

		- Ideal for transactional workloads such as databases and boot volumes.

- Backup 

	- Known as snapshots

		- Incremental backups and stored redundantly

- Write Storage types for workloads that require persistent storage

## File Storage

### centralized access to files that need to be easily shared and managed by multiple host computers.

###  storage is mounted onto multiple hosts

### usecases

- Large  content repositories  
  
  Development  environments  
  
  User  home directories

###  Files stored in hierarchy

## Object Storage

### single unit of data when stored

### stored in a flat structure instead of a hierarchy

### Each object is a file with a unique identifier.

### store almost any type of data,

### there is no limit to the number of objects stored,

### useCases

- Object storage is generally useful when storing large data sets, unstructured files like media assets, and static assets, such as photos.

### Amazon S3

- Storage for the internet

- Amazon Simple Storage Service

- concepts

	- Bucket

		- folder

			- object

				- Access by URL

		- Everything in Amazon S3 is private by default.

		- Policies

			- IAM policy

			- Bucket Policy

- encrypt

	- Server side encryption

	- Client Side Encryption

- Use Versioning to Preserve Objects

	- Versioning enables you to keep multiple versions of a single object in the same bucket.

	- Amazon S3 automatically generates a unique version ID for the object being stored.

	- Versioning States

		- Unversioned (the default): No new or existing objects in the bucket have a version.

		- Versioning-enabled: This enables versioning for all objects in the bucket.

		- Versioning-suspended: This suspends versioning for new objects

- Storage Classes

	- Amazon S3 Standard

		- This is considered general purpose storage for cloud applications, dynamic websites, content distribution, mobile and gaming applications, and big data analytics

	- Amazon S3 Intelligent-Tiering

		- useful if  data has unknown or changing access patterns.

		- stores objects in two tiers

			- a frequent access tier 

			- An Infrequent Access Tier

			- Amazon S3 monitors access patterns of your data, and automatically moves your data to the most cost-effective storage tier based on frequency of access.

	- Amazon S3 Standard-Infrequent Access (S3 Standard-IA):

		- S3 Standard-IA is for data that is accessed less frequently, but requires rapid access when needed

		- offers the high durability, high throughput, and low latency of S3 Standard, with a low per-GB storage price and per-GB retrieval fee

		- This storage tier is ideal if you want to store long-term backups, disaster recovery files

	- Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA):

		- S3 One Zone-IA stores data in a single AZ and costs 20% less than S3 Standard-IA

		-  S3 One Zone-IA is ideal for customers who want a lower-cost option for infrequently accessed data but do not require the availability and resilience of S3 Standard or S3 Standard-IA

		- It’s a good choice for storing secondary backup copies of on-premises data or easily re-creatable data.

	- 

		- Amazon S3 Glacier

			- S3 Glacier is a secure, durable, and low-cost storage class for data archiving

			- S3 Glacier provides three retrieval options that range from a few minutes to hours.

	- Amazon S3 Glacier Deep Archive:

		- lowest-cost storage class and supports long-term retention and digital preservation for data that may be accessed once or twice in a year

		- Designed for customers—particularly those in highly regulated industries, such as the Financial Services, Healthcare, and Public Sectors—that retain data sets for 7 to 10 years or longer to meet regulatory compliance requirements.

### Object Lifecycle Management

- actions

	- transition

		- define when should transition  objects to another storage class.

	- expiration

		- define when objects expire and should be permanently deleted.

	- Ex:

		- you might choose to transition objects to S3 Standard-IA storage class 30 days after you created them, or archive objects to the S3 Glacier storage class one year after creating them.

- Use cases

	- Periodic logs: 

		- If you upload periodic logs to a bucket, your application might need them for a week or a month. After that, you might want to delete them

	- Data that changes in access frequency

		- Some documents are frequently accessed for a limited period of time. After that, they are infrequently accessed. At some point, you might not need real-time access to them, but your organization or regulations might require you to archive them for a specific period. After that, you can delete them.

## Relational

### Amazon RDS

- Relational Database as service

	- Instance families

		- standard

		- Memory optimized

		- Burstable Performance

- DB instance uses Amazon Elastic Block Store (EBS) volumes as its storage layer. 

- Backup support

	- Automatic

		- automated backups can be retained between 0 and 35 days

		- The 0 days setting actually disables automatic backups from happening

		- Automated backups are beneficial for the point-in-time recovery.

	- Mannual

		- automated backups longer than 35 days

- Redundency

	- Amazon RDS Multi-AZ

		- Amazon RDS creates a redundant copy of your database in another AZ


# Monitoring


## CloudWatch Service

### Monitoring and Observability Service

- Detect Anomalous Behaviour in Environment

- Set Alarms to alert when something is not right

- Visulaize log and metrics with the AWS Management Console

- Take automated actions ex: Scalling 

- Trobuleshoot Issues

- Discover Insights to keep applications healthy


# AWS Devops


## CodeCommit

### Based on git

### Supports all the git commands

### Fully managed source control service

### Can Host Private git Repositories

### Act as Source Control Systems for Software projects

### Well integrated with CloudWatch Events

### How to connect ?

- Https

	- Port:443

- ssh

	- Port:22

- https(grc)

	- git-remote-codecommit (GRC).

		- Python utility

### Authenticated Access

- Managed through the use of an IAM user account

	- https git credential

	- SSh Public key

- Use IAM policy to manage fine grained access


# Branching Stratergies


## MainOnly

## Dev Isolation

### Separate and Parallel Branches

### Developer work with Dev Branch , Once the feature is implemented completely , then the code from Dev branch merged to Main Branch

### Any bug in the production , fixed and updated to the main branch and changes from main branch merged to dev branch

### Two truths of software code exists

### If modified Main branch code in the event off bug fix  is not merged back to dev code and later if the dev code to merged to the master , there is a possibility of Bug Occurring

## Feature isolation

### variant or evolution of development isolation

### its short-lived development branches that are dedicated to one feature

### The branch only exists, "or should only exist for a short time "before it's merged back into its parent

### There can be multiple feature branches running concurrently

## Release Isolation

### Release branches can coexist with development or feature branches. 

### When you want to release a new version of your software because the required features have been completed, tested and merged back into master, you create a release branch.

### Release Branches are readonly with One Exception

### If a bug is found in production code, it is fixed in the release branch and merged back into the main branch

### There can be multiple concurrent releases in existence and being supported


# Stratergies


## Github Flow

### The master branch is always deployable and should reflect what is in production

### Any new  dev work is created in a branch off master

### When the branch is ready or finished, open a pull request for the code to be reviewed.

### Once the branch has been reviewed and tested, it can be deployed into production

### If the deployed branch causes issues or has bugs, it can be rolled back by deploying the existing master,Otherwise, the branch can be merged with master.

## Git Flow

### Uses Two Main Branches

- The master branch is stable code that reflects what is deployed in production

- The development branch is the parent branch of most code changes

	- master branch for a set of features

### 

- When a change is required, a branch is created from the development branch.

	- Categories

		- Feature Branches

		- Branched from Development  merged to  Development

		- Release branches

		- branched from development merged to master and development

		- hotfix branches

		- branched from master merged to master and development

	- When a feature is finished, it is merged back to the development branch

	- Deployment Of New Functionality

		- A release branch is created from the development branch.

		- The release branch, typically named as the release version number, including any bug fixes and tweaks

		- The release brach is merged back into development and master branches after the release is deployed.

	- hotfix

		- If a critical bug is discovered in the live application that can't wait for the next release, a hotfix is required

		- A hotfix is branched off master and merged back into master as well as development, so both code threads get the fix.

## Release Flow

### All branches, be they features, bugs or hotfixes, are branched directly off the master trunk

###  Release Flow diverges from traditional trunk-based models is how and when the code is deployed

- 

	- This strategy puts emphasis on the release schedule, which is tied to deploying at the end of each sprint

- Designed around workflow, adhering to continuous integration and deployment processes, and projects at scale

- It fits with the sprint schedule

	- The sprints usually don't correspond to any one feature branch, is the time taken to do the actual deployment

	- how does it deal with half-completed features at the time of release deployment? 

		- use feature flags to turn off incomplete functionality within the code

	- hotfixes.

		- These are done on the main branch and then cherry-picked into the release branch.

### Deployment Not Tied up with Feature Branch Completion

- There are literally hundreds of developers working on hundreds of branches at any one time

- developers would spend too much time waiting for their queued release to be deployed before continuing with the next feature.

### Branch naming follows the convention of user name, then branch type, followed by description,

### The development or topic branches need to be as small as possible, so work is broken down into its smallest logical functional units.

- It makes reviewing and testing much easier and quicker, while limiting damage if something does go wrong


# 233819810445


# AWS Global Infrastructure


# AWS Shared Responsibility Model


## Managing Security and Compliance is a shared responsibility b/w AWS and Customer

## Customer

### Responsible for Security “IN” the cloud

- Customer Data

- Platform , Applications , Identity and Access Management

- Operating System , Network and Firewall Configuration

- Client Side Data Encryption and Data Integrity and Authentication 

- Server Side Encryption 

- Network Traffic Protection (Confidentiality, Integrity and Identity)

## AWS

### Responsible for Security “OF” the Cloud

- Protecting AWS Regions , AZ and DataCenters

- Physical Security of the buildings

- Managing the hardware , software and networking component that run AWS Services

