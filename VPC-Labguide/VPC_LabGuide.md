  # Introduction to Amazon Virtual Private Cloud (VPC) {#section1}
Amazon **VPC**enables you to build a virtual network in the AWS cloud - no VPNs, hardware, or physical datacenters required. You can define your own network space, and control how your network and the Amazon EC2 resources inside your network are exposed to the Internet.
  
A virtual private cloud (VPC) is a virtual network dedicated to your AWS account. It is logically isolated from other virtual networks in the AWS Cloud. You can specify an IP address range for the VPC, add subnets, add gateways, and associate security groups.
  
## Getting started with Amazon VPC
  
Follow the steps below to get started with the lab.
  
1.Sign in to the AWS Management Console by copying the  **Sign-in link**, **Username**, and **Password** provided below.

Or just click [AWS Console](https://aws.amazon.com/console/ )

  - Sign-in Link: https://aws.amazon.com/console/
  - IAM Username:
  - Password:
![](./images/step1.png )
  
2.You will see a ***AWS_Console***
  
![](./images/Screenshot%20(283).png)
  
3.Go to ***Search bar*** 

![](./images/VPC02.png )

4.search for the service ***VPC*** and press **Enter**

![](./images/VPC03.png )
  
5.After selecting **VPC** you will see ***VPC dashboard*** 

![](./images/VPC04.png )

6.Now in top right corner select the **region** you want your VPC to be created

![](./images/VPC05.png )
  
7.Now click on ***Create VPC*** button on the screen
  
![](./images/VPC06.png )
  
8.You can also create ***VPC*** by selecting the **Your VPC** on left panel
  
![](./images/VPC07.png )
  
9.Once you start the VPC creation you will see a [**default VPC**](#section5 ) present in that window.
Click to know more about [default VPC](https://docs.aws.amazon.com/vpc/latest/userguide/default-vpc.html )
  
10.And on top right corner select the **create VPC** button to create it manually (will be doing the same in some time)
Now click on default **VPC Id** present on screen to explore more about that VPC
  
![](./images/VPC08.png)
    
11.After clicking you will see the screen as shown below
  
![](./images/VPC09.png )

12.Here you can see the details of Default VPC
  
13.Next Scroll down you will see a ***resource map***

![](./images/VPC10.png )

14.That Resource map conatins
- [VPC](#section1 )
- [Subnets](#section2 )
- [Route Tables](#section3 ) &
- [Connection networks](#section4 ) 
  
----
#### Creating VPC
15.Now Go back to **your VPC** window to create the **VPC** of your own. Click on ***create VPC***

![](./images/VPC08.png )
  
16.Creation of VPC done in *Two ways* 
- [VPC only](#section6)  
- [VPC and more](#section7)
  
##### VPC Only{#section6}
17.select **VPC only** 
Follow the steps as shown below

18.Select the option

i.VPC only

ii.Give a unique name to your VPC

iii.Give IPv4 [CIDR](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-cidr-blocks.html)(click on cidr to know more)

iv.IPv6 leave it default as shown in picture

v. Tenancy:- set it as default

vi. Click Create VPC

![](./images/VPC14.png)

![](./images/VPC121.45.png)
  
19.And *CIDR* to know more about it click on the link given below
[CIDR](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-cidr-blocks.html )
20.create the vpc as shown in the picture
21.Once the creation done properly you will see the vpc created successfully

![](./images/VPC15.png )
  
*Successfully created VPC using VPC Only*
  
22.Now again back to **VPC dashboard** and *your VPC* you will see the vpc created by you.
But above process doesn't give you a complete VPC ie *VPC* with subnets,Route table and internet gateway.
Here subnets,Route table and internet gateway must be created manually
  
#### Creating SUBNET
23.Now select **Subnets** from left panel and clik ***create subnet*** present on top right

![](./images/VPC16.png)

Now Follow the steps as shown below

i.Select VPC you have created for you subnet and Click create subnet

![](./images/VPC18.png)

![](./images/VPC19.png)

24. In Subnet Settings,

  i.Give unique name to your subnet

  ii.Leave avaliability zone as it is

  iii.Select the IPv4 CIDR that you have created for VPC

  iv.Now Give IPv4 CIDR for your subnet

![](./images/VPC20.png)

25.Click on create Subnet

![](./images/VPC21.png)
  
Now back to dashboard to see the subnet that is created
Subnet Created Successfully

![](./images/VPC22.png )
  
---
#### Creating Route Tables
26.Now select **Route Tables** from left panel and clik ***create Route Table*** present on top right
Now Follow the steps as shown below

![](./images/VPC23.png)

i.Give unique name to your Route table

ii.Select the VPC you have created to associate it with route table

![](./images/VPC24.png)

Click Create Route Table

![](./images/VPC52.png)

Route Table created Successfully

![](./images/VPC25.png)
  
You will see the Route table in dashboard
  
---
#### Creating Internet Gateway
27.Now select **Internet Gateway** from left panel and clik ***create Internet Gateway*** present on top right
Now Follow the steps as shown below


![](./images/VPC26.png)

28.Give a unique name to your Internet gateway
29.Click on Create Internet Gateway

![](./images/VPC27.png)
  
Once the creation is done attach *internet gateway* to VPC that you have created
Now Follow the steps as shown below

To Attach,
  i.Click on Attach VPC on top right corner

![](./images/VPC28.png)

Select the VPC that you have created

![](./images/VPC29.png)

Clcik on attach Internet Gateway

![](./images/VPC30.png)
  
---
##### Edit Routes
Now back to **Route Table** and select **Routes** and perfom the action as shown

30.Click Edit Routes

![](./images/VPC33.png)

31.Then Click Add Routes

![](./images/VPC34.png)

i. In destination select the item as shown in image

ii. In Target select *Internet gateway* and the internet gateway you have created

32.Click on *Save changes*

![](./images/VPC35.png)

##### Subnet Association
And in that **Route Table** itself select **Subnet Association** and perform the action as shown

31 In Explicit Subnet Association
32.Click Edit Subnet Association

![](./images/VPC31.png)

33.Check mark the subnet 
34.Click on *Save Association*

![](./images/VPC32.png)
  
---
Now Again back to **your VPC** and select the VPC that you have created and panel that appears at bottom shows the ***Resource Map***

![](./images/VPC40.png)

![](./images/VPC41.png)
  
You have Successfully created the complete **VPC** with subnets,Route Table and Internet gateway which were not present before.
  
---
##### VPC and more{#section7}
Now Go back to **your VPC** window to create the **VPC** of your own. Click on ***create VPC***

![](./images/VPC08.png )
  
35.This time select *VPC and more*
  
Follow the steps shown below to perform the same

i. Select the option VPC and more

ii.Keep the check mark as it is for name tag or Give a unique name to your VPC

iii. Give IPv4 [CIDR](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-cidr-blocks.html)(click on cidr to know more)

iv. for IPv6 CIDR leave it as it is as shown

![](./images/VPC45.png)

i.Select the number of [Avaliablity Zones](https://docs.aws.amazon.com/whitepapers/latest/get-started-documentdb/aws-regions-and-availability-zones.html)

ii. select Number of Public Subnets as per the requirement

iii. And also select Number of Private Subnets as per the requirement

![](./images/VPC46.png)

Click Create VPC

![](./images/VPC47.png)
  
36.A **preview** that shows the flow and connections

![](./images/VPC48.png)

![](./images/VPC49.png)

![](./images/VPC50.png)
  
Once you complete the process and clicks *create VPC* & then *View VPC* a window will be opened stating the successfully creation of ***VPC***
  
Successfully created the ***VPC***.

***YOU HAVE SUCCESSFULLY COMPLETED THE LAB***
  
#### What is Default VPC? {#section5}
A default VPC comes with a public subnet in each Availability Zone, an internet gateway, and settings to enable DNS resolution. Therefore, you can immediately start launching Amazon EC2 instances into a default VPC. You can also use services such as Elastic Load Balancing, Amazon RDS, and Amazon EMR in your default VPC.
A default VPC is suitable for getting started quickly and for launching public instances such as a blog or simple website. You can modify the components of your default VPC as needed.
  
---  
##### SUBNET{#section2}
A subnet is a range of IP addresses in your VPC. You can create AWS resources, such as EC2 instances, in specific subnets.
###### Subnet types
The subnet type is determined by how you configure routing for your subnets. For example:
  
**Public subnet** – A subnet that can access the Internet is a public subnet. It is the subnet that has a route table entry that points to an internet gateway. Resources that are required to face or receive Internet traffic can be added to a public subnet
  
**Private subnet** – A subnet that cannot access the Internet is a private subnet. It is the subnet that does not have a route table entry that points to an internet gateway. Resources that are not required to be publicly available are within a private subnet.
  
To Know more Click [Subnets](https://docs.aws.amazon.com/vpc/latest/userguide/configure-subnets.html )
  
----  
##### Route Tables{#section3}
Route tables are essentially a set of rules. These rules help us determine where to direct the network traffic from a subnet or gateway. We can assign a specific route table to a subnet.
  
To Know more Click [Route Tables](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html )
  
  
---  
##### Connection networks{#section4}  
A gateway essentially connects a VPC to another network. For instance, if we want to connect a VPC to the internet then we will use an Internet Gateway. The default VPC includes an internet gateway by default.
The default VPC has a public subnet in each availability zone along with an internet gateway.
  
To Know more Click [Internet Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html )
  
  
***CONGRATULATIONS!***