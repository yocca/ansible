# Ansible AWS Cloud Infrastructure 
This guide is intended to assist developers in creating the minimal cloud infrastructure for securely and durably hosting web applications on AWS. Please refer to the **Knowledge** section to learn more about the cloud resources provisioned through the [Ansible](https://docs.ansible.com/ansible/latest/index.html) [playbook](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html) provided in this project (playbook-create.yml)
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
## Creating the network infrastructure and web application
**Note:** Make sure to refer to the 'Deletion' section to deprovision the resources created from this section. You will be charged for these resources on AWS while they're up and running.


The following command will run a playbook that will provision network resources with a sample web application to test the resources work as expected (Should take 10-20 minutes):

`ansible-playbook playbook-create.yml`

If the resources are provisioned correctly, then in your terminal you should see above 'PLAY RECAP' something simlilar to below
```
ok: [localhost] => {
    "msg": "app_name-xxxxxxxxxx.us-east-1.elb.amazonaws.com"
}
```

Copy that DNS name and open it in your browser. If you see a page with the header "Amazon ECS Sample App" then congratulations! You're up and running.

## Deletion
To deprovision the resources you've created, enter the following command into your terminal. It will delete the web application stack and then the network stack (Should take 10-20 minutes): 

`ansible-playbook.delete.yml`

