## Virtual Private Cloud
A Virtual Private Cloud (VPC) is a private cloud environment hosted within a public cloud infrastructure. It allows users to create a logically isolated network within a public cloud, enabling greater control over their cloud resources while benefiting from the scalability and cost-effectiveness of a public cloud.

### What is the importance of a VPC?
A VPC is essential for enhancing security, control, and flexibility in your cloud setup. WITHOUT IT! you risk exposing your data to threats and losing the ability to manage your resources effectively.

## Uses of a VPC
- Hosting Web Applications
- Disaster Recovery

## How to create a VPC?
Step - 1: Go to VPC and create a VPC then we have to create 4 subnets , where 2 subnets are private and other two are public.

Step - 2: Create Gateways
- First, create an Internet Gateway, which will be connected to your VPC easily.
- Then, we have to create Virtual Private Gateway and connect to the VPC.

Step - 3: Create Route Tables
- We have to go to Route Table and create two route tables, one for Internet Gateway and one for Virtual Gateway.
- Now, we'll connect the two public subnet in the Internet Gateway and on the other one, we have to add the private subnets.

Step - 4: Create Instances
- We'll have to create two instances where we have to enable the public IPv4.
- On both of the instances, we have to download the web server.
- We'll now check if the instances are working.

Step - 4: Create the Load Balancer
- Before creation, we have to give the VPC, availability zone of the EC2 instance.
- Create a target group where we'll select the two instances we created.
- We have to go through the health check settings and edit the setting like the following:
![image](https://github.com/user-attachments/assets/8c336a3f-8aad-491e-97c3-ac502f285926)

- Go to Load Balancer where we'll select the target group and then, create the Load Balancer.
- Now, put on any instance and type the following commands in PuTTY

```
htop
seq 999999999999999999999999999999999999999999999999999999999 > /dev/null &
htop
```
