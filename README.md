#  MyFirstProject.Darey.Io

## WEB STACK IMPLEMENTATION (LAMP STACK) IN AWS
A technology stack is a set of frameworks and tools used to develop a software product. This set of frameworks and tools are very specifically chosen to work together in creating a well-functioning software. They are acronymns for individual technologies used together for a specific technology product. some examples are…

* LAMP (Linux, Apache, MySQL, PHP or Python, or Perl)
* LEMP (Linux, Nginx, MySQL, PHP or Python, or Perl)
* MERN (MongoDB, ExpressJS, ReactJS, NodeJS)
* MEAN (MongoDB, ExpressJS, AngularJS, NodeJS

## Step 0 
* you will need an AWS account 
* Select your preferred region (the closest to you) and launch a new EC2 instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM)

Once you successfully log into your AWS, you will see the main console with all the service listed as follows


![AWS Console](https://user-images.githubusercontent.com/84423958/127680745-429c26e4-84ba-4814-8e85-70d69ff92ae3.PNG)

**Before proceeding with the creation of an EC2 instance, Select the desired and closest region to you.**

**Let me list certain parameters when choosing an AWS region which factors should you consider:**

* Latency and proximity

* Security and regulatory compliance

* Service Level Agreements (SLA)

* And finally, the most important is the Cost

![Avalaibility zone](https://user-images.githubusercontent.com/84423958/127685975-af52e1f7-1568-4161-8a6a-cf45cb979717.PNG)


**Click on "Services" at the upper left corner and you will see the all the Services available on AWS. Click on "EC2"**

![EC2 Selection](https://user-images.githubusercontent.com/84423958/127687520-8cdb059b-fe3d-4f19-99ab-06a149daf8a4.PNG)

select ec2 stroll down, and Click on "Launch Instance."

![image](https://user-images.githubusercontent.com/84423958/127687845-da1e4f05-a772-4210-87cb-a5331ef57266.png)



**Launch a new "EC2" instance of t2.micro family with Ubuntu Server 20.04 LTS(HVM) 64 bit**

![Obuntu Server](https://user-images.githubusercontent.com/84423958/127685312-ceaf0b38-fe5e-4f6d-8f1a-97fc5e57c16d.PNG)

**Click on Next: to choose an instance type**

![image](https://user-images.githubusercontent.com/84423958/127688873-233ba6a4-fa13-4325-a873-655057447b05.png)


**Next: Configure Instance Details**

![image](https://user-images.githubusercontent.com/84423958/127689158-1a64683b-e079-42e7-9a29-e46fbacd67e4.png)

Next: Add Storage; to add or configure the Storage size and type. Every time you launch an instance from an AMI, a root storage device is created for that instance. The root storage device contains all the information necessary to boot the instance. You can specify storage volumes in addition to the root device volume when you create an AMI or launch an instance using block device.

![image](https://user-images.githubusercontent.com/84423958/127690076-00716498-1e80-414a-bbf1-334d93e8a63d.png)

Next: Add Tags. A tag is a label that you assign to an AWS resource. ... Tags enable you to categorize your AWS resources in different ways, for example, by purpose, owner, or environment. For example, you could define a set of tags for your account's Amazon EC2 instances that helps you track each instance's owner and stack level.

![image](https://user-images.githubusercontent.com/84423958/127690478-1a7cbf74-0aa1-4c88-967f-109e0a0cb058.png)


Click Next: Configure Security Group; A security group acts as a virtual firewall for your EC2 instances to control incoming and outgoing traffic. Inbound rules control the incoming traffic to your instance, and outbound rules control the outgoing traffic from your instance. When you launch an instance, you can specify one or more security groups.

![image](https://user-images.githubusercontent.com/84423958/127691533-75e49e26-6d91-46df-a6df-0e13114cbf22.png)












