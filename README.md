# AWS EKS Cluster Using Terraform

This repository contains Terraform configurations to provision an Amazon EKS (Elastic Kubernetes Service) cluster on AWS.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- [Terraform](https://www.terraform.io/downloads.html) installed on your local machine.
- AWS IAM credentials configured with appropriate permissions.
- `kubectl` installed on your local machine to interact with the Kubernetes cluster.

## Usage

1. Clone this repository:

    ```bash
    git clone https://github.com/NahlaAbdAlghany/EKS-Cluster-Using-Terraform.git
    cd EKS-Cluster-Using-Terraform
    ```

2. Initialize Terraform:

    ```bash
    terraform init
    ```

3. Modify the `variables.tf` file to set your desired configuration options.

4. Review and apply the Terraform plan:

    ```bash
    terraform plan
    terraform apply
    ```

5. Once the cluster is provisioned, configure `kubectl` to connect to the cluster:

    ```bash
   aws eks --region us-east-1 update-kubeconfig --name demo
    ```

6. Verify the cluster connectivity:

    ```bash
    kubectl get nodes
    ```

## Deployment YAML File

Find the deployment YAML file [here](EKS-Cluster-Using-Terraform/k8s/deployment.yml) to deploy resources onto the EKS cluster.

## Clean Up

To clean up and delete all resources provisioned by Terraform, run:

```bash
terraform destroy
