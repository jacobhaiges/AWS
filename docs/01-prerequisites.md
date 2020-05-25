# AWS Free Tier Account

For this project I am going to be using AWS's [free tier](https://aws.amazon.com/free/) to learn without spending money.

# SSH Client

To connect to the virtual hardware an SSH client will be needed. Since I am using Windows 10, I am going to use [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/), a free SSH and Telnet client.

# SSH Key Generator

In addition to an SSH client, I will be using [PuTTYgen](https://www.puttygen.com/) to generate private key pairs to connect to EC2 instances.

# AWS CLI

I am going to be using the [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-welcome.html) throughout this project. The documents available from AWS explain how to set up and configure the CLI.
The version of AWS CLI I'm using:
```
aws --version
```
Output:
```
aws-cli/2.0.16 Python/3.7.7 Windows/10 botocore/2.0.0dev20
```

Configuring the AWS CLI:
```
aws configure
```
Default region:
```
us-east-2
```
Default output format:
```
yaml
```
