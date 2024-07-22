# Kubernetes Ansible Project

## Overview

This project contains Ansible playbooks and Kubernetes manifests to set up a Kubernetes cluster and deploy a Node.js application and a PostgreSQL database.

## Folder Structure

- `ansible-files/`: Contains Ansible playbooks and roles.
- `kubernetes/`: Contains Kubernetes manifests for deployments and services.

## Setup Instructions

### Prerequisites

- Ansible installed on your local machine.
- Access to AWS with appropriate permissions to create EC2 instances.
- SSH key pair configured for EC2 instances.

### Steps

1. **Set up the master node:**

    ```sh
    ansible-playbook ansible/playbooks/setup-master.yml
    ```

2. **Set up the worker nodes:**

    ```sh
    ansible-playbook ansible/playbooks/setup-worker.yml
    ```

3. **Deploy the Node.js application:**

    ```sh
    ansible-playbook ansible/playbooks/deploy-nodejs.yml
    ```

4. **Deploy the PostgreSQL database:**

    ```sh
    ansible-playbook ansible/playbooks/deploy-postgresql.yml
    ```

## Accessing the Node.js Application

Once the service is created, you can access the Node.js application using the public IP address of any node (master or worker) and the NodePort (30000).



