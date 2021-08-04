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

* If you answer “yes”, you’ll be asked to select a level of password validation. Keep in mind that if you enter 2 for the strongest level, you will receive errors when attempting to set any password which does not contain numbers, upper and lowercase letters, and special characters, or which is based on common dictionary words.

## If we enabled password validation, we’ll be shown the password strength for the root password we just entered and our server will ask if we want to continue with that password.
## If we are happy with our current password, enter Y for “yes” at the prompt:

## For the rest of the questions, We press Y and hit the ENTER key at each prompt. This will remove some anonymous users and the test database, disable remote root logins, and load these new rules so that MySQL immediately respects the changes we have made.

when you are done, you will get this output:

![image](https://user-images.githubusercontent.com/84423958/128263637-40a989bb-0d35-41cd-a52e-163c7715f814.png)

* When you're finished, test if you're able to login to the MySQL Console by typing:
````

sudo mysql
````

![image](https://user-images.githubusercontent.com/84423958/128263917-44348631-a618-4780-93aa-5d5fe8872a26.png)

* To exit the MySQL Console, type: **exit
```

mysql> exit
```

## Setting a password for the root MySQL account works as a safeguard, in case the default authentication method is changed from unix_socket to password. For increased security, it’s best to have dedicated user accounts with less expansive privileges set up for every database, especially if we plan on having multiple databases hosted on our server.

## Note: At the time of this writing, the native MySQL PHP library mysqlnd doesn’t support caching_sha2_authentication, the default authentication method for MySQL 8. For that reason, when creating database users for PHP applications on MySQL 8, we’ll need to make sure they’re configured to use mysql_native_password instead. We’ll demonstrate how to do that later.

## Our MySQL server is now installed and secured.

* Next, we will install PHP, the final component in the LAMP Stack.


## Step 3 — Installing PHP

# We have Apache installed to serve our content and MySQL installed to store and manage our data. PHP is the component of our setup that will process code to display dynamic content to the final user. In addition to the php package, we’ll need php-mysql, a PHP module that allows PHP to communicate with MySQL-based databases. We’ll also need libapache2-mod-php to enable Apache to handle PHP files. Core PHP packages will automatically be installed as dependencies.

To install these 3 packages at once, **run:
```

$ sudo apt -y install php libapache2-mod-php php-mysql
```

* Once the installation is finished, you can run the following command to confirm your PHP version:
```

php -v
```

![image](https://user-images.githubusercontent.com/84423958/128264962-de5b4193-1b07-4ff2-818c-a600bf9033c8.png)


* At this point, your LAMP stack is completely installed and fully operational.
* To test our setup with a PHP Script, it's best to setup a proper Apache Virtual Host to host our website's file and folders. Virtual Host allows you to have multiple websites located on a single machine and users of the websites will not even notice it.

![image](https://user-images.githubusercontent.com/84423958/128265068-655cceeb-197c-4ac9-b73c-63d237fe66de.png)

* We will configure our first Virtual Host in the next step.

## Step 4 — Creating a Virtual Host for your Website using Apache

In this project, you will set up a domain called projectlamp, but you can replace this with any domain of your choice.

Apache on Ubuntu 20.04 has one server block enabled by default that is configured to serve documents from the /var/www/html directory. We will leave this configuration as is and will add our own directory next next to the default one.

Create the directory for projectlamp using ‘mkdir’ command as follows:
```

sudo mkdir /var/www/projectlamp
```

This will create a new blank file. Paste in the following bare-bones configuration by hitting on i on the keyboard to enter the insert mode, and paste the text:

![image](https://user-images.githubusercontent.com/84423958/128265413-71a2d527-5020-4dc9-ae4e-f7d893ef678b.png)


To save and close the file, simply follow the steps below:

* Hit the esc button on the keyboard
* Type :
* Type wq. w for write and q for quit
* Hit ENTER to save the file
# You can use the ls command to show the new file in the sites-available directory
```

$ sudo ls /etc/apache2/sites-available
```
**see my output:

![image](https://user-images.githubusercontent.com/84423958/128265843-74afd325-3483-4184-8ef2-a0dde9f39e65.png)


# With this VirtualHost configuration, we’re telling Apache to serve propitixhomes.local using /var/www/projectlamp as the web root directory. If we like to test Apache without a domain name, we can remove or comment out the options ServerName and ServerAlias by adding a # character in the beginning of each option’s lines. Adding the # character there will tell the program to skip processing the instructions on those lines.

You can now use a2ensite command to enable the new virtual host:

```
$ sudo a2ensite projectlamp
```

![image](https://user-images.githubusercontent.com/84423958/128265990-eb915fef-d9dc-4d90-955e-cdd5e40027c2.png)

* We might want to disable the default website that comes installed with Apache. This is required if we are not using a custom domain name, because in this case Apache’s default configuration would overwrite our virtual host. To disable Apache’sdefault website use a2dissite command, type:

```
$ sudo a2dissite 000-default
```

![image](https://user-images.githubusercontent.com/84423958/128266165-54fe30a4-a986-4ccf-8ccf-6231169f5f5d.png)


* To make sure your configuration file doesn't contain syntax errors, run :
```
$ sudo apache2ctl configtest
```

![image](https://user-images.githubusercontent.com/84423958/128266302-e2d69c96-f044-4bad-956e-4d8d15fd1756.png)

* Finally, reload Apache so these changes take effect:
```

sudo systemctl reload apache2
```

Your new website is now active, but the web root /var/www/projectlamp is still empty. Create an index.html file in that location so that we can test that the virtual host works as expected:

* Type and run :
```
$ sudo vi /var/www/projectlamp/index.html
```

see my input :

![image](https://user-images.githubusercontent.com/84423958/128266622-3acbca57-00e6-4f11-b9c1-00d5abb1152c.png)

Now go to your browser and try to open your website URL using IP address:
```

http://<public-ip-address>:80
```

or you can also browse using your public dns. the result is the same
```
http://<Public-DNS-Name>:80
```
**See my output :

![My DNS](https://user-images.githubusercontent.com/84423958/128267571-69232d24-49a3-4047-a5d8-5eaee30006ee.PNG)


You can leave this file in place as a temporary landing page for your application until you set up an index.php file to replace it. Once you do that, remember to remove or rename the index.html file from your document root, as it would take precedence over an index.php file by default.

* To check your Public IP from the Ubuntu shell, run :
```

$(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 
$(curl -s http://169.254.169.254/latest/meta-data/public-ipv4)
```

## Step 5 — Enable PHP on the website

With the default DirectoryIndex settings on Apache, a file named index.html will always take precedence over an index.php file. This is useful for setting up maintenance pages in PHP applications, by creating a temporary index.html file containing an informative message to visitors. Because this page will take precedence over the index.php page, it will then become the landing page for the application. Once maintenance is over, the index.html is renamed or removed from the document root, bringing back the regular application page.

In case you want to change this behavior, you’ll need to edit the /etc/apache2/mods-enabled/dir.conf file and change the order in which the index.php file is listed within the DirectoryIndex directive:
```

sudo vim /etc/apache2/mods-enabled/dir.conf
```

#Change this: #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm #To this: DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
After saving and closing the file, you will need to reload Apache so the changes take effect:
```

$ sudo systemctl reload apache2
```

* Finally, we will create a PHP Script to test the PHP is correctly installed and configured on our Server.
* Now that we have a custom location to host our website's files and folders, we'll create a PHP test script to confirm that Apache is able to handle and process requests for PHP files.
* Create a new file named index.php inside our custom web root folder:
```

$ vim /var/www/projectlamp/index.php
```

This will open a blank file. Add the following text, which is valid PHP code, inside the file:

```
<?php
phpinfo();
```

**See my output:

![image](https://user-images.githubusercontent.com/84423958/128268230-281810ad-8e55-4746-a561-7aae989fa81a.png)


# When you are finished, save and close the file, refresh the page and you will see a page similar to this :

![image](https://user-images.githubusercontent.com/84423958/128268293-1e08ccca-8653-4b85-ad43-7b7d6f5b399d.png)

* This page provides information about your server from the perspective of PHP. It is useful for debugging and to ensure that your settings are being applied correctly.

* If you can see this page in your browser, then your PHP installation is working as expected.

* After checking the relevant information about your PHP server through that page, it’s best to remove the file you created as it contains sensitive information about your PHP environment -and your Ubuntu server. You can use rm to do so:
```

$ sudo rm /var/www/projectlamp/index.php
```

























