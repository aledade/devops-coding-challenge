# devops-coding-challenge
Choose one of the following coding challenges to complete.

## Option one
Create a git repository that contains Ansible and Terraform code for deploying two postgresql clusters to AWS with the following requirements:
1. The Postgresql clusters will each be deployed to an EC2 instance (don’t use RDS) in a different VPC. One for Dev and one for Prod.
1. The Ansible code will have a playbook for each environment in the root directory. 
1. The code for installing Postgresql will be in a role. 
1. You will use group vars to configure postgresql_max_connections to 30 in prod and 20 in dev.
1. The Postgresql clusters will each have a database named db1.
1. There will be two users in prod and four users in dev.
    1. Prod
        1. admin
        1. service1
    1. Dev
        1. admin
        1. service1
        1. user1
        1. user2
1. The admin user in each database will be a super user.

### Acceptance criteria
* You must provide your code in full so we can deploy it (you do not need to provide access to the Postgresql clusters, only to the code)
* Your code is clean and readable
* Steps for deploying the Postgresql clusters are in the README.md
* The fewer the number of steps needed to deploy, the better. 


## Option two
Create a git repository that contains code for deploying an AWS EKS cluster with the following requirements:
1. There will be two Auto Scaling groups for the workers nodes
1. Each ASG will launch 1 - 3 worker node instances
1. The cluster will automatically update DNS records in a private Route53 zone from kubernetes resources (ingresses, Services, etc)
1. The cluster will have one admin user and two regular users
1. The cluster will have three namespaces
    1. default
    1. user-1
    1. user-2
1. The admin user will have full permissions on all namespaces
1. The users will have read/write access to only their namespaces

### Acceptance criteria
* You can use any tools you want to complete the challenge
* You must provide your code in full so we can replicate your cluster (you do not need to provide access to the cluster, only to the code)
* Your code is clean and readable
* You must document any steps that are not automated in the README.md

