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

Before you launch an instance, you need to select a key pair which is then required for SSH access to the Server.

To create a new key-pair, Select "Create a new key-pair" from the drop down menu, give a name to the key-pair, and download it.

IMPORTANT - save your private key (.pem file) securely and do not share it with anyone! If you lose it, you will not be able to connect to your server ever again!

As for me, I already created a key-pair, so I selected "Choose an existing key-pair" and i checked the acknowledgment box


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

**Next:Review Instance Launch**

![image](https://user-images.githubusercontent.com/84423958/127693935-a1b4de94-d7c2-4bb1-b413-323dca3aa859.png)

Before you launch an instance, you need to select a key pair which is then required for SSH access to the Server.

To create a new key-pair, Select "Create a new key-pair" from the drop down menu, give a name to the key-pair, and download it.

IMPORTANT - save your private key (.pem file) securely and do not share it with anyone! If you lose it, you will not be able to connect to your server ever again!

As for me, I already created a key-pair, so I selected "Choose an existing key-pair" and i checked the acknowledgment box


![image](https://user-images.githubusercontent.com/84423958/127694403-6bea779f-d03a-415a-a9ec-1ba45f830e78.png)


Click on "View Instance" to check the Instance State and other details.

![image](https://user-images.githubusercontent.com/84423958/127694579-b7aa0fe2-f689-470f-a231-9e66b4276475.png)


**The next phase is to view your instance state, click on your instance to view it. At this stage, you will see if your instance is running or still pending. mine is running, now i can view my instance details**

![image](https://user-images.githubusercontent.com/84423958/127694793-50d6fdc3-0480-4ae3-97bb-aaa088ab14ca.png)

Next is to connect my instance to an SSH Client. In my own case, am using MOBAXTERM, you can decide to use PUTTY or any other existing ones. And to connect to MOBAXTERM, you need to copy the public ip address of the instance you want to ssh to
Next i opened my MOBAXTERM, i clicked on SESSION, SSH, on the REMOTE HOST i pasted my public-ip address i copied from my instance. i checked the box and i specify username as (ubuntu)

![image](https://user-images.githubusercontent.com/84423958/127695219-63f9bb7e-8b0a-4ad3-87c4-558aafe6f433.png)


Next i clicked on ADVANCE SSH settings, i checked the box for private key, and i browse my downloaded key.pem next i clicked on OK

![image](https://user-images.githubusercontent.com/84423958/127695676-27876298-0db5-4d55-9451-87aa0e53162c.png)















