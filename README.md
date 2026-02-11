<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** ElHalouf  
**Email:** shakyleboss@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

In this project, I will create a Virtual Private Cloud with subnets and an internet gateway.

### What is Amazon VPC?

...

...

### Personal reflection

This project took me 1h30

...

---

## Virtual Private Clouds (VPCs)

### What I did in this step

In this step, I will create a VPC in the region closest to me

### How VPCs work

VPCs are a private, controllable network boundary in the cloud, so you can decide what can talk to what, and what can reach the internet.

### Why there is a default VPC in AWS accounts

There was already a default VPC in my account ever since my AWS account was created. This is because without a default VPC, I wouldn't be able to access certain resources before learning how to create a VPC.

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-networks-vpc_2facf927)

### Defining IPv4 CIDR blocks

To set up my VPC, I had to define an IPv4 CIDR block, which is a range of IPv4 addresses.

---

## Subnets

### What I did in this step

In this step, I will launch subnets to divide my VPC to group resources with similar access rules and restrictions.

### Creating and configuring subnets

Subnets are range of IP addresses inside a VPC, where I can place resources into a specific subnet.

### Public vs private subnets

The difference between public and private subnets is that a public subnet is connected to the internet while private subnets don't have direct internet access.  For a subnet to be considered public, it has to be attached to an Internet Gateway 

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-networks-vpc_157c4219)

### Auto-assigning public IPv4 addresses

Once I created my subnet, I enabled auto-assign public IPv4 addresses.  This setting makes sure that resources get a public IP address, so that it has access to the internet.

---

## Internet gateways

### What I did in this step

In this step, I will connect your VPC to the internet using a internet gateway. Because I want my instances to access the internet and be accessible to external users.

### Setting up internet gateways

Internet gateways are a VPC component that attaches to a VPC to enable internet connectivity.

Attaching an internet gateway to a VPC means that the resources in my VPC can now access the internet.

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

### What I'm doing in this extension

In this part, I'll use the AWS CLI to set up a VPC

### Exploring CloudShell and CLI

VPC resources could also be created with CloudShell, which isa space to run code and the AWS CLI is the Command line interface.

### Debugging my setup

To set up a VPC or a subnet, you can use these commands
aws ec2 create-subnet --vpc-id vpc-1234 --cidr-block 10.0.0.0/25
aws ec2 create-vpc --cidr-block 10.0.0.0/24 --query Vpc.VpcId --output text
~aws ec2 create-tags --resources= vpc-1234 --tags Key=Name,Value="NextWork VPC 2"

![Image](http://learn.nextwork.org/lively_blue_beautiful_jellyfish/uploads/aws-networks-vpc_9b2465411)

### Comparing CloudShell vs AWS Console

Compared to using the AWS Console, an advantage of using commands is speed and repeatability. An advantage of using the Console is clarity: the visual workflow makes it easier. Overall, I preferred the AWS CLI because of its efficiency. 

---

---
