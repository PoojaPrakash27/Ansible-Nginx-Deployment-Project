# Ansible Nginx Deployment Project

## Overview

This project demonstrates the use of Ansible to automate the deployment of Nginx and a static web application across multiple EC2 instances. It showcases best practices in infrastructure as code, configuration management, and automated deployment strategies.

## Features

- Automated Nginx installation on multiple EC2 instances
- Deployment of a static web application
- Scalable and reusable Ansible playbooks
- EC2 instance configuration management

## Prerequisites

- Ansible 2.9 or higher
- AWS account with EC2 instances
- Python 3.6 or higher
- boto3 library for AWS interaction

## Project Structure

```
.
├── ansible.cfg
├── inventory
│   └── hosts
├── playbooks
│   ├── main.yml
│   ├── nginx_install.yml
│   └── webapp_deploy.yml
├── roles
│   ├── nginx
│   └── webapp
└── README.md
```

## Setup

1. Clone this repository:

   ```
   git clone https://github.com/yourusername/ansible-nginx-project.git
   ```

2. Update the `inventory/hosts` file with your EC2 instance details.

3. Ensure your AWS credentials are properly configured.

## Usage

Run the main playbook:

```
ansible-playbook playbooks/main.yml
```

This will execute the following tasks:

- Install Nginx on all specified EC2 instances
- Deploy the static web application

## Customization

- Modify `roles/nginx/templates/nginx.conf.j2` to customize Nginx configuration
- Update `roles/webapp/files/` with your static web application files
