**what is cloud computing?**
Cloud computing is the delivery of computing services including servers, storage, databases, networking, software, analytics, and intelligence-over the Internet ("the cloud") to offer faster innovation, flexible resources, and economies of scale

**Benifits of cloud-**
• Faster time to market
• Scalability and flexibility
• Cost savings
• Better collaboration
• Advanced security
• Data loss prevention

**Disadvantages of cloud**-
• risk of vendor lock-in
• less control over underlying cloud infrastructure
• concerns about security risks like data privacy and online threats
• integration complexity with existing systems
• unforeseen costs and unexpected expenses

Types of clouds- Public cloud , Private cloud and Hybrid cloud

**Public Cloud-**
• Hosted at Service provider Site.
• Supports connectivity over intemet
• Suitable for information not very sensitive
• Cheaper than private cloud
• Utitzes shared infrastructure
• Supports multiple customers
• Requires nigher level of secunty
• Shared servers
• No Dedicated proactive monitoring
• Fixed-cost
• Multitenant architecture

**Private Cloud-**
• Hosted at Enterprise or Service provider Site
• Supports connectivity over Internet Private network (WAN)
• Suitable for very sensitive information
• Costier than public cloud
• Doesn't utilize shared infrastructure
• Supports one customer
• Requines medium level of security
• Dedicated servers
• Dedicated proactive monitoring
• Dedicated customer architecture

**Hybrid cloud-**
• combination of both public and private cloud
• shared security responsibilities
• helps maintain higher controls over sensitive data and processes

Cloud service modals-
• Iaas
• Paas
• Saas

**Amazon Web Services-**
Amazon Web Services(AWS) is the world's most comprehensive and broadly adopted cloud platform, offering over 200 fully featured services from data centers globally.

Computer services-
• Elastic Computer Cloud-EC2
• ECS/EKS-Containerized Services
• Lambda-Serverless

**Storage Services-**
• Simple Storage Services-S3(Object Storage)
• Elastic Block Store-EBS
• Elastic File System-EFS(Shared File system)
• Archival Services-Glacier

**Network Services-**
• Virtual Private Cloud-VPC
• Domain Name Service-Route53
• Direct Connect

**S3-**
• Object Storage with durability of 99.999999999%, 11 9's
• Infinitely scaling storage
• Can keep files in buckets
• S3 is a global service but buckets are created in specific regions
• Globally unique bucket names

**EC2-**
• Most Popular AWS offering
• Infrastructure as a code service
• Provides rented Virtual Machines
• EC2 uses EBS and instance store to store data
• EC2 uses ELB to distribute data
• EC2 uses autoscaling for scaling purpose
• Bootstrapping can be done using userdata scripts

**EC2 Instance types-**
• t2.micro
• t2.xlarge
• c5d.4xlarge
• r5.16xlarge
• m5.8xlarge

**ELB(Elastic Load Balancer)-**
  • implementation of horizontal scaling
  • required high availability
  • Types of load balancers-
     • Classic load balancers -Layer 4 & 7
     • Appliccation load balancers - Layer 7
     • Network load balancer -Layer 4

**Autoscaling-**
  • Self healing implementation for dynamic loads
  • can create  or delete instances automatically
  • Types of scalings-
    • Simple/Step scaling
    • Target Trackling
    • Scheduled Scaling

**AWS CLI(Command Line Interface)-**
  • To interact wuith AWS services using commands in command line shell
  • Direct access to public APIs
  • Its open source and an alternative to AWS Management Console
  • AWS CLI is build  on AWS SDK for Python

#Docker- Its a service in which help to run various apps that are packaged in conntainers and can be deployed on any OS without  actually installl each of them

**AWS Conatinerization-**
  • ECS- Elastic Container Service
  • EKS- Elastic Kubernetes Service
  • Fargate- Amazon's serverless container platform

#CDN- Cloud Delivery Network

**Steps for hosting a sample web page with  a load balancer-**
step1 - Open your AWS console
step2 - Creating VM(Virtual Machine)-
    • create 2 VMs named instance 1, instance 2 respectively with ubuntu AMI.
    • Set t2.micro as the instance type.
    • Create a new key pair named "newkey"
    • Also allow https and http traffic from internet
    • After that click launch instance.
    • output-![Screenshot 2023-12-08 095755](https://github.com/userramanujan/notes/assets/145014171/4a153003-77c3-4e25-a0a1-4849e6b644fc)
step3 - Installing a server -
     • Connect to instance1 by selecting it and the clicking on the "connect" option 
     • After connecting to the instance1 write "sudo su" to go into root user.
     • Then write "sudo apt update" to install all necessarey updates to our VM.
     • Then write "sudo apt install nginx" then press "y" to install a server to our VM
step7 -Creating a sample html file to be displayed on our website
    • Then write "cd /var/www/html" which is the location of an html file in our VM.
    • Then write 'echo "This is VM1" > index.html' which basically write a sample text into our indexx.html file which is loacte in our VM
    • output instance 1 -![Screenshot 2023-12-08 102842](https://github.com/userramanujan/notes/assets/145014171/c05a6ec7-2564-4f81-90ca-907298406663)

step8 -Do similar steps with instance2
step9 - creating a Target group-
      • Here we are goung to create a group of targatted instances
      • Go to "Target Group" option available in "load balancing" section
      • Create a new target group with  name "NewTarget"
      • Then click on "Next".
      • Then select the needed instances to be targeted. and include them as pending below
      • Click on "Create target Group".
      • Then refresh the page several times to gett the status of instance as "Healthy".
      • Output- ![Screenshot 2023-12-08 105510](https://github.com/userramanujan/notes/assets/145014171/3d2ade16-a4c9-4ebc-a302-88b8c0a1d8d5)

step10 - creating a security group_
      • Click on "create Security Groups" and give a name and description to your security group
      • Add an inbound rule to allow all traffic and source from anywhere IPv4
      • click on "create security group"
      • Output- ![Screenshot 2023-12-08 104807](https://github.com/userramanujan/notes/assets/145014171/93723989-a928-4056-a9dd-15d8e30e44e6)

step10 - creating a load balancer-
      • click on "load balancer" available in "load balancing" section
      • click on "Create load balancer" and create an application load balancer
      • Give a name your load balancer
      • Then select the availability zones
      • Then select the security group thata we have created perviously
      • Then select the target group that wehave created.
      • Then click on create load balancer
      • Output- ![Screenshot 2023-12-08 105634](https://github.com/userramanujan/notes/assets/145014171/9c35fcf8-b6ce-410f-a18f-8aaf27476b6d)

step11 - Checking our load balacer-
      • copy the DNS name of the loadbalancer and open it in new tab 
      • output1 -![Screenshot 2023-12-08 105955](https://github.com/userramanujan/notes/assets/145014171/48bd16fc-3469-4dfd-8839-6b84f51e3599)
      • Then again refresh the page
      • output2 - ![Screenshot 2023-12-08 105940](https://github.com/userramanujan/notes/assets/145014171/37dd07e8-f277-4bf0-aaa7-69753ee56f44)
      • We can see that  the traffic is distributing once it goes to instance1 and then to instance2 and similar process happpens when more then one instances are there.
