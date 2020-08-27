+++
title = "Test your sock shop"
chapter = true
weight = 02
+++

# Test Your Sock Shop

In order to test that our sock-shop has been deployed, we are going to grab the load balancer IP and test it in our own browser. 


**If you are running this in an AWS event,** visit the [EC2 Console](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Home:) and log in to your bastion host EC2 instance. The name of your bastion host will end in **-bastion.** (Example: **mod-f679f4081e7d405c-bastion**). 


![Bastion-Connect](/images/bastion-connect.png)

Locate your bastion host and find the gray button that says "Connect". Then select **EC2 Instance Connect** (browser-based SSH connection) and click **"Connect"**. A new browser window will open. 

![Bastion-ec2](/images/bastion-ec2.png)

Run the following command in your browser window to grab the load balancer IP:

```
kubectl get svc -o wide -n sock-shop | grep LoadBalancer
```

Copy the load balancer IP from the terminal and copy it. 

![Bastion-lb](/images/LB-IP.png)

Paste it into your web browser, and you should be good to go.

![Bastion-sock](/images/Browser-Sock.png)

{{% notice tip %}}
Keep this browser tab open for the rest of today's activities. 
{{% /notice %}}

**If you are running this workshop on your own,** run the following command in your cloud9 terminal in order to grab the load balancer IP:

```
kubectl get svc -o wide -n sock-shop | grep LoadBalancer
```
Paste it into your web browser, and you should be good to go.

{{% notice tip %}}
Keep this browser tab open for the rest of today's activities. 
{{% /notice %}}