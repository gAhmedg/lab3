# Terraform Project 

## Overview

This Terraform project manages the infrastructure with custom modules for establishing a resilient and scalable architecture  and using  Reverse proxy with Load balancer . It provisions and manages resources on AWS Cloud Provider, enabling the deployment of two Ec2 instance (Apache)  with Private subnet and LoadBalancer for Private instances ,also we have Two Ec2 instance (Nginx)  with Public subnet and LoadBalancer for Public instances act as Reverse proxy that's can  enhance security by acting as an intermediary between clients and servers, shielding the backend infrastructure from direct exposure to the internet and providing an additional layer of defense against attacks.

## Diagram of Project
![alt text](<screenshots/terraform.drawio.svg>)


## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Getting Started](#getting-started)
3. [Folder Structure](#folder-structure)


## Prerequisites

Before you begin, ensure you have the following prerequisites installed:

- Terraform: [Installation Guide](https://learn.hashicorp.com/tutorials/terraform/install-cli)
- [Cloud Provider CLI](#) ( AWS CLI) [Installation Guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

## Getting Started

1. Clone this repository:

   ```
   git clone https://github.com/gAhmedg/Terraform-Reverse-Proxy-Project.git
   ```

2. Change into the project directory:
    ```
    cd Terraform-Reverse-Proxy-Project
    ```

3. Initialize Terraform: to downloading provider plugins and initializing backend configurations
    ```
    terraform init
    ```
4. Executes the planned changes described in the Terraform configuration, creating, updating, or deleting resources as necessary to achieve the desired state defined in your infrastructure code
    ```
    terraform apply
    ```
#### The output will be like this 
![alt text](<screenshots/visual studio lb dns.png>)


5. copy link and open it :

    ```
    <LoadBalancer-ip>
    ```
    
![alt text](<screenshots/Screenshot 2024-05-04 200251.png>)


#### <u> the Network of the infrastructure will be like this </u>





https://github.com/gAhmedg/Terraform-Reverse-Proxy-Project/assets/108756442/8293fd05-4ad9-4f92-9cbd-3321eb4044fe





---
#### <u> the user-data for priavte and public ec2 instances  </u>





![alt text](<screenshots/user data.png>)

---
## Folder Structure
```
.
├── README.md
├── main.tf
├── variables.tf
├── outputs.tf
├── userdata-proxy.sh
├── userdata-apache.sh
├── screenshots
├── modules
│   ├── vpc
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── loadbalancer
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   ├── subnets
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   └── instance
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
└── .gitignore
```
 
