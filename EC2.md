# EC2 (Amazon Elastic Compute Cloud)

## Before we begin:

1. Create an account in Amazon Web Services
2. Login to Amazon Web Services

**Note:** Do keep a Debit Card and Pan Card on you for smooth creation of account.

## Launching an Instance:

Step - 1: Locate **EC2** and click **Launch Instance**

Step - 2: Select an AMI (Amazon Machine Image) ; For eg. Windows, Ubuntu etc. 

Step - 3: Configure Security Group:-

  - Create a security group with the following rules:-
      - **SSH**
      - **HTTP**
      - **HTTPS**
      - **Custom TCP**
      - **All Traffic**
   
Step - 4: Create a new key pair and download the `.ppk` file

Step - 5: Launch the Instance

## Connect to EC2 Using PuTTY

Step - 1: Open PuTTY

Step - 2: In **Host Name (or IP Address)**, enter your instance's **public IP** (can be copied after launching instance)

Step - 3: In the left sidebar, locate **Connection > SSH > Auth**. Then, click **Browse** and select `.ppk` file

Step - 4: Click **Open** and use `ubuntu` as the username when prompted

## Installation of Apache2 on the EC2 Instance

### Update the package list and install Apache2:

```
sudo apt update
sudo apt install apache2
 -y
```

## Deletion of Default index.html and Creation of new one

Step - 1: Locate the Apache Directory: ``` cd/var/www/html ```

Step - 2: Delete the default `index.html` : ```sudo rm index.html```

Step - 3: Create a new HTML File: ```sudo vi index.html```

Step - 4: Add your HTML code: 

- For example:
```
<html>
Hello, Welcome to Cloud Computing
</html>
```

Step - 5: Save and Exit

## Access Your Website

Step - 1: Open a web browser

Step - 2: Enter your **EC2 Public IP** in the browser

Step - 3: Visit your website

Step - 4: Your HTML Website will be visible
