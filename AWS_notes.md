## 1. AWS IAM - Identity & Acces Management

1. IAM is a service that helps you securely control access to AWS resourses.
2. It allows us to manage users, roles, and pertmissions to define who can access what within your AWS environment.
3. Free.
4. Global service.
5. root account created by default, should'nt be used or shared.

## 2. AWS CLI

1. AWS CLI provides a command line, scripting approach
   a. aws configure - to configure user
   b. aws iam list-users - to list active users.

## 3. AWS EC2 - Elastic Cloud Compute

1. service that provides scalable, on-demand virtual servers, called "instances," in the cloud, allowing users to rent computing power (CPU, memory, storage) to run applications without managing physical hardware.

## 4. AWS EBS - Elastic Block storage

1.  It is a cloud based storage service that provides durable, high performance block storage for use with Amazon EC2 instances.
2.  Works as a vertual hard drive, allowing you to store and access data even when your EC2 isnatnce are stopped or terminated.

for ex. hosting MySQL ddatabase, need of reliable high performance storage.

NOTE-

1. In EBS we can create storages and differnet sizes.
2. volumes, can be attached and detached to different servers.
3. snapshots - We can make copy of them also in different regions also.
4. can be backed up.
5. backup lifecycle can be enabled to automate backup.

## 5. AMI - Amazon Machine Image

It is a preconigured template that provides the necessar information to launch an EC2 instance in AWS.

It includes:

1. operating system(eg. Linux, windows)
2. Application server(Apache, Nginx)
3. Pre-installed softwares ad configurations.

### Template VS AMI

1. Template stores configuration settings for launching EC2 instance where as, AMI is like a snapschot of EC2
2. AMI is launches new EC2 instance with same config where as Template provides a standar way to define instance.
3. Template does not have OS or software, it refers API and adds details from there.
4. Template is for reusing same config.
