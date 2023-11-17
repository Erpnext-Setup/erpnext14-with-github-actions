# Install erpnext app with github actions
![Docker](https://img.shields.io/badge/Docker-23.0.3-%232496ED.svg?style=for-the-badge&logo=docker&logoColor=white) ![ERPNext](https://img.shields.io/badge/ERPNext-v14-%2343853D.svg?style=for-the-badge&logo=erpnext&logoColor=white) ![MariaDB](https://img.shields.io/badge/MariaDB-10.8-%234479A1.svg?style=for-the-badge&logo=mariadb&logoColor=white) ![Python](https://img.shields.io/badge/Python-3.10-%234B8BBE.svg?style=for-the-badge&logo=python&logoColor=white)

## Introduction
In this tutorial, we will walk you through the process of setting up an ERPNext application in a Dockerized environment using GitHub Actions. Whether you're a seasoned developer or a newcomer to ERPNext, this guide is designed to simplify the deployment process on a fresh Ubuntu server.

## Prerequisites
- OS : ubuntu 22.04 [i am using `aws ec2 instance` (type: t3.small)]
- USER : user with sudo privileges [i am using `root user`]
- USER/PASSWORD AUTHENTICATION 

## Work to do: 
- fork repo
- define secret variables
- run workflow

## Getting started 
### Fork this Repository:
To start installation, fork 🍽 this repo:

![image](https://github.com/Erpnext-Setup/erpnext14-with-github-actions/assets/105498424/d8eddbcb-dbe8-4247-91ac-42b01f19e505)

### Define secrets variables in actions secrets and variables:
you just need to define these variables as secrets. Secrets provide a way to store sensitive information, and they are encrypted and only exposed to runners during the execution of your workflow. Here's how you can define these secrets:

Go to your GitHub repository.
Click on `Settings` in the upper-right corner.
In the left sidebar, click on `Secrets`
Click on `New repository secret`.
Name the secret as SSH_HOST and enter the server IP address.

#### SSH_HOST, SSH_USER, SSH_PASSWORD:
Create two more secrets: SSH_USER, SSH_HOST and SSH_PASSWORD for the server username and password.

#### ADMIN_PASSWORD:
Create a new secret named ADMIN_PASSWORD and set the value to the administrator password for the ERP app.

#### ERP_SITE_NAME:
Create a new secret named ERP_SITE_NAME and set the value to your desired ERP site name (e.g., erpsite.local).

#### MYSQL_ROOT_PASSWORD, MYSQL_ROOT_USER:
Create two secrets: MYSQL_ROOT_PASSWORD and MYSQL_ROOT_USER for the MariaDB root user password and username.

![image](https://github.com/Erpnext-Setup/erpnext14-with-github-actions/assets/105498424/1f19f061-045c-4dd5-bb98-ef1255da5603)

#### Run workflow:
Run the workflow manually / commit any change.







## PORTS
      3306 8000 9000


