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

## AWS ELB - Elastic Load Balancer

--> Terms

### Scalibility -

Means ability to grow your system's resources when your application or website gets more traffic or more users.

How to magnage heavy trafic?

1. vertical Scaling (scalling up)
   a. Vertical scalability means adding more power (CPU, RAM) to your existing server.
   b. EX. t2.micro to m5.large

2. Horizontal Scalling (Scaling out)  
   a. Horizontal scaling means adding more instances (servers) to distribute the load.
   b. You can add more EC2 machines behind a load balancer.

### High Availability(HA)

Means keeping the service up and running with minimal downtime, so its always accessable to users.
Ex. running resourses in multiple Availability Zones.

### Elasticity

Means the ability to automatically adjust resourses as the demand changes adding more when needed and removing when its no longer necessary.

Ex. ASG

## ELB summary:-

1. Distributes traffic :- splits traffic across multiple servers so no single server gets overloaded.
2. Improves availability:- in case server goes down - sends traffic automatically, ensuring app stays available
3. Scales Resourses :- helps manage high demand by adding more servers during peak times and distributing the load

## Types of ELB

1. Application load balancer(ALB):- perfect for web applications, handling HTTP & HTTPS requests(layer7)
2. Network load balancer(NLB):- high performance, low latency, - gaming, financial apps.
3. Gateway Load Balancer(GLB):- helps deploy, scale and manage third party virtual appliances, such as firewalls and monitoring solutions.

## AWS ASG - Auto Scaling Group

1. It is service that automatically "Adds" or "Remove" EC2 instance based on demand to ensure your application is always available.
2. Help scale up when more capacity is needed and scale down during low usage save costs, keeping the right no. of servers running at all times.

## Functions of ASG

1. Automatic Scaling - scale the no. of EC2 instances up or down based on demand.
2. Maintain Instance Health - Replace unhealthy instance automatically to ensure reliability.
3. Use Scaling policies - Set rules for scaling based on metrics like CPU usage or request count.
4. Ensure Availability - Always keep a defined no. of instances running to meet application needs.
5. Schedule Scaling - Pre-configure scaling activities for specific times (eg, traffic peaks).
6. Distribute Instances: Deploy instances acroess multiple availablity zones for high availability.
7. Integrate with ELB - Attach instances to an Elastic Load Balancer to automatically balance traffic.
8. Optimize Costs - Scale down during low demand to save on infra cost.

Steps:-

1. Launch Template or config
2. Create auto scaling grp
3. select VPC and subnets
4. attach LB(op.)
5. config scalling policies
6. health checks
7. add notifications
8. review and create

## AWS S3 Bucket
