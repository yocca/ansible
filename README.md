# Ansible AWS Cloud Infrastructure 
This guide is intended to assist developers in creating the minimal cloud infrastructure for securely and durably hosting web applications on AWS. Please refer to the **Knowledge** section to learn more about the cloud resources provisioned through the [Ansible](https://docs.ansible.com/ansible/latest/index.html) [playbook](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html) provided in this project (playbook.yml)
## Knowledge
* **[Scenario this guide almost imitates](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Scenario2.html)**
* [Amazon VPC User Guide](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html)
* [Ansible AWS Guide](https://docs.ansible.com/ansible/latest/scenario_guides/guide_aws.html)
## Requirements
* [AWS Account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)
* AWS User with the following policies/permissions attached:
  * AmazonVPCFullAccess
  * AmazonEC2FullAccess
* AWS User with [programmatic access keys](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_credentials_access-keys.html#Using_CreateAccessKey)  
* [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed
* [Boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/guide/quickstart.html) installed
## Usage
### Creation
### 
### Deletion