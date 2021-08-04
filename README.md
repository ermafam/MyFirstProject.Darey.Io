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

For a web application to work smoothly, it has to include an operating system, a web server, a database, and a programming language. The name LAMP is an acronym of the following programs:

* Linux Operating System
* Apache HTTP Server
* MySQL database management system
* PHP programming language

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


For a web application to work smoothly, it has to include an operating system, a web server, a database, and a programming language. The name LAMP is an acronym of the following programs:

* Linux Operating System
* Apache HTTP Server
* MySQL database management system
* PHP programming language

## LAMP STACK IMPLEMENTATION IN AWS
The Four Layers of a LAMP Stack

Linux based web servers consist of four software components. These components, arranged in layers supporting one another, make up the software stack. Websites and Web Applications run on top of this underlying stack. The common software components that make up a traditional LAMP stack are:

**Linux**: The operating system (OS) makes up our first layer. Linux sets the foundation for the stack model. All other layers run on top of this layer.

**Apache**: The second layer consists of web server software, typically Apache Web Server. This layer resides on top of the Linux layer. Web servers are responsible for translating from web browsers to their correct website.

**MySQL**: Our third layer is where databases live. MySQL stores details that can be queried by scripting to construct a website. MySQL usually sits on top of the Linux layer alongside Apache/layer 2. In high end configurations, MySQL can be off loaded to a separate host server.

**PHP**: Sitting on top of them all is our fourth and final layer. The scripting layer consists of PHP and/or other similar web programming languages. Websites and Web Applications run within this layer.

* We can visualize the LAMP stack like so:

![image](https://user-images.githubusercontent.com/84423958/128258569-dc9804c8-7984-4484-b300-e2e30f1be914.png)


## In this project, I will implement a web solution based on LAMP stack on a Linux server by implementing the steps below:

# STEP 1 — INSTALLING APACHE AND UPDATING THE FIREWALL

* We need to Install Apache using Ubuntu’s package manager, apt:

```
$ sudo apt update 
$ sudo apt install apache2
```

# To verify that apache2 is running as a Service in our OS, use following command

# See my output:

![My Apache Server](https://user-images.githubusercontent.com/84423958/128259682-7a4e5b73-7dba-4ce8-8d49-1128c3031b04.PNG)

* We need to configure our firewall settings to allow HTTP traffic. UFW has different application profiles that we can leverage for accomplishing that. To list all currently available UFW application profile, **run:**

**See my output:**

![image](https://user-images.githubusercontent.com/84423958/128260279-49c680d4-f2c3-4d8b-a6f8-d1b0f6d5f39d.png)


Before we can receive any traffic by our Web Server, we need to open TCP port 80 which is the default port that web browsers use to access web pages on the Internet

To open our port 80, i went back to the instance, clicked on security, clicked on edit inbound rules and i add rules. i added port 80 for http and port 443 https and i cliked on save rules

**see my output:**


![image](https://user-images.githubusercontent.com/84423958/128260418-7845bed1-947c-4b67-8752-6ce4ef6f7d66.png)


## Our server is running and we can access it locally and from the Internet (Source 0.0.0.0/0 means ‘from any IP address’).

* To verify and check that we can access it locally in our ubuntu shell and from the internet,**run**
```
$ curl http://localhost:80
or
$ curl http://127.0.0.1:80
```

## As an output you can see some strangely formatted test, do not worry, we just made sure that our Apache web service responds to ‘curl’ command with some payload.

Open a web browser of your choice and try to access following **url
```
http://<Public-ip-address>:80
```

## Another way to retrieve your Public IP address, other than to check it in AWS Web Console, is to use the following command.
```

$ curl -s http://169.254.169.254/latest/meta-data/public-ipv4
```

* If you see the following page, then your web server is now correctly installed and accessible through your firewall.

## See my output:


![image](https://user-images.githubusercontent.com/84423958/128262262-754eb2fa-f653-4bac-b011-986adadf7099.png)

# STEP 2 - Installing MySQL

## We need to install the database system to be able to store and manage data for our website. MySQL is a popular database management system used within PHP environments.


* To install mysql-server, **run:**
```

sudo apt -y install mysql-server
```

* After the installation it is recommended that we run a security script that comes pre-installed with MySQL. This script will remove some insecure default settings and lockdown access to our database system.

* Start the interactive Script by running:
```

sudo mysql_secure_installation
```

* This will ask if you want to configure the VALIDATE PASSWORD PLUGIN.

## Note: Enabling this feature is something of a judgment call. If enabled, passwords which don’t match the specified criteria will be rejected by MySQL with an error. It is safe to leave validation disabled, but you should always use strong, unique passwords for database credentials.

Answer Y for yes, or anything else to continue without enabling.
```

VALIDATE PASSWORD PLUGIN can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD plugin?

Press y|Y for Yes, any other key for No:
```






















