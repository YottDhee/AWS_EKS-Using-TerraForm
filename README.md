# AWS_EKS - Using Terraform

This is a simple exercise used to SETUP EKS Using Terraform

Creating the workshop environment with Terraform

For the given configuration, terraform will create the Workshop environment with the following:

Create a VPC across three availability zones
Create an EKS cluster
Create an IAM OIDC provider
Add a managed node group named default
Configure the VPC CNI to use prefix delegation
Download the Terraform files:

~
$
mkdir -p ~/environment/terraform; cd ~/environment/terraform
~
$

git clone https://github.com/mithuns1986/EKS-SETUP-USING-TF.git

Run the following Terraform commands to deploy your workshop environment.

~
$
export EKS_CLUSTER_NAME=eks-workshop

~
$
terraform init

~
$
terraform apply -var="cluster_name=$EKS_CLUSTER_NAME" -auto-approve

This generally takes 20-25 minutes to complete.

