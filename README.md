🛠️ DevOps Engineer Assessment – Paper.Social

Role: DevOps Engineer & AWS

Company: Paper.Social

Objective: Design and automate a multi-cloud deployment pipeline using AWS
---------------------------------------------------------------------------------

📌 Project Overview

Paper.Social is developing a modern social media platform using multi-cloud infrastructure to ensure high availability and resilience. This project implements infrastructure automation, configuration management, CI/CD pipelines, monitoring, and logging using industry-standard tools across AWS

NOTE : READ ME files also provided in sub Floders
-------------------------------------------------
🎯 Key Features

1. 🧱 Infrastructure as Code (IaC)
-------------------------------------------------------

Tool: Terraform

Clouds: AWS

Resources Provisioned:

EC2 instance (AWS)

VPC/Subnet/Firewall/Security Groups 

Use Terraform main.tf file for automation in AWS

2. ⚙️ Configuration Management
  ------------------------------------------------------

Tool: Ansible

Configured:

 docker installtion 
 
 jenkins installtion
 
 git installtion
 
 
 All  installtion automation scripts available in devops tools and site.yml file 
 Using this scripts  you can automate.

 3. 🚀 CI/CD Pipeline
----------------------------------------------------------------------------------------
 Tool:  Jenkins

 Pipeline Flow:
 
 Triggers on push to master branch

Builds and tests application

Deploys to AWS

Docker images used for consistent environment

Monitoring & Logging
------------------------------------------------------
Tool: Prometheus + Grafana (Open-source stack)

Setup: using  ansible playbooks you can automation will be done 

prometheus_install.yml
grafana_install.yml

After installtion :
                   http://<public-ip>:3000======>>Grafana  ===>>Login: admin / admin

                   http://<public-ip>:9090====>>prometheus

📦 Sample Application
------------------------------------------------------------------
Simple web app displaying:

Hello, Paper.Social!

Can be built using: 

  Web server : NGINX (static)
  
  code : HTML

**Deploy with CI/CD**
-------------------------------

Push code to master branch

Pipeline triggers automatically

App is built & deployed to AWS


 Access Application
 ---------------------------------
**
 AWS EC2 : <<public-IP>>**



Assumptions & Design Decisions
------------------------------

Infrastructure kept minimal to control cost


Dockerized for environment consistency


Logs and metrics collected centrally


Configured SSH + firewall rules per cloud best practices


Cost & Security Considerations
-------------------------
Allowed only required inbound ports


Docker runs as non-root where applicable

🪯 Cleanup
------------
terraform destroy  


 Bonus Features Implemented
-------------------------------------


✅  SSH Key Security

✅ Parallel deployment to AWS + IBM

✅ Auto-scaling-ready architecture

✅ Dockerized deployments
