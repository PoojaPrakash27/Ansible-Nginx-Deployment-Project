# Ansible Nginx Deployment Project

## Overview

This project demonstrates the use of Ansible to automate the deployment of Nginx and a static web application across multiple EC2 instances each running a different distribution/OS including Ubuntu, Red Hat Enterprise Linux (RHEL), and Amazon Linux 2. It showcases best practices in infrastructure as code, configuration management, and automated deployment strategies.

## Features

- Automated Nginx installation on multiple EC2 instances
- Deployment of a static web application
- Scalable and reusable Ansible playbooks

## Prerequisites

- Ansible 2.13 or higher
- AWS account with EC2 instances
- Python 3.8 or higher

## Project Structure

```
.
├── inventory.ini
├── setup_nginx.yml
├── roles
│   ├── nginx
└── README.md
```

## Setup

1. Clone this repository:

   ```
   git clone https://github.com/PoojaPrakash27/ansible-nginx-project.git
   ```

2. Update the `inventory.ini' file with your EC2 instance details.

3. Ensure your AWS credentials are properly configured.

## Usage

Run the main playbook:

```
ansible-playbook -i inventory.ini setup_nginx.yml
```

This will execute the following tasks:

- Install Nginx on all specified EC2 instances
- Deploy the static web application

## Customization

- Update `nginx/files/` with your static web application files
