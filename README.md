# AWS

The goal of this project is to learn AWS and configure some services (IAM, EC2, ALB, etc.)


------------------




# Labs

# [Setup](docs/01-prerequisites.md)
Using AWS to learn is cheap (as long as you use free tier resources!) and there's so many different services to use / experiment with. The good news about using AWS is that you don't need to have good physical hardware yourself because it is all hosted on AWS's equipment. With that being said, depending on your operating system there might be a few programs you need to install (notably, an SSH client on Windows).

# [IAM Configuration](docs/02-iam-config.md)
[Identity and Access management](https://aws.amazon.com/iam/) is important because it allows close access control to AWS resources. By using IAM, users and groups can be created with varying permission levels for easy management and security (who can access or change a particular resource). 


Compare the AWS IAM structure to a more traditional Active Directory deployment in which each employee also has their own account with distinct permissions associated with that account. AWS groups work similarly to Active Directory groups in that a set of permissions can be attatched to a group, and any accounts in that group inherit those permissions. 

# [EC2 Configuration](docs/03-ec2-config.md)
[EC2](https://aws.amazon.com/ec2/) is an IAAS offering by AWS that provides scalable computing in the cloud. Amazon handles the responsibility of the networking, server, storage, and virtualization and the user is responisble for the management of the operating system, runtime, data, and application(s). The user can change the networking and storage configuration, however, that is all abstracted away from the user as AWS handles that at their data centers.

# [Setting up EC2 with a Load Balancer](docs/04-ec2-with-alb.md)
Redundancy is important to prevent an outage resulting from a single point of failure. AWS offers a variety of services that have redundancy provided, but I'm going to be focusing on configuring an [Application Load Balancer](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/introduction.html).

An Application Load Balancer works at the application layer (7th) of the [OSI model](https://www.cloudflare.com/learning/ddos/glossary/open-systems-interconnection-model-osi/). The purpose of a load balancer is to distribute incoming traffic across multiple "targets" (for example, an EC2 instance) to increase the availability of your application.
