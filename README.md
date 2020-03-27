# AWS
Learning AWS through various projects
---------------------------------------


Setting up billing alerts: ![](images/billingAlerts.png)


Configuring IAM user for personal use: ![](images/iamUser.png)


Deploy an EC2 instance & configure it as a web server to host a web page: ![](images/ec2Instance.png)
![](images/instanceLaunch.png)

Now with the EC2 instance launched, I am going to use it to host a simple web page that I created:

To accomplish this, I started out by connecting to the EC2 instance and issuing an update (sudo yum update). Next, I installed an HTTP server (sudo yum install httpd -y). Once this was installed, I created an index.html file (touch index.html) within /var/www/html (cd /var/www/html) and edited the file with nano (sudo nano index.html). After putting the HTML code in the file, I started the httpd service with (service httpd start). The result is a working webpage hosted on Amazon EC2: ![](images/ec2Webpage.png)

Creating a snapshot of the EC2 instance & deploying a new EC2 instance using the snapshot: ![](images/ec2Snapshot.png)

The snapshot was created successfully, now to launch the EC2 instance using the snapshot I created: ![](images/snapshotDeployment.png)

Let's verify that the snapshot works and we have the webpage installed: ![](images/snapshotVerify.png)

Creating an AMI using that EC2 instance: ![](images/ec2AMI.png)

Putting that AMI in an autoscaling group so that one VM always exists: ![](images/autoscaleGroup.png)

Let's verify that the autoscaling group is working: ![](images/autoscaleVerify.png)

Next, creating an Elastic Load Balancer 
