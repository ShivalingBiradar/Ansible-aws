# Ansible-AWS Project

## Amazon.aws.ec2_instance module – Create & manage EC2 instances

Ansible playbooks are used for defining automation tasks in YAML format. They allow you to describe the desired state of your system and execute a series of tasks to bring it to that state. Playbooks can be used for various automation purposes, including configuration management, application deployment, and infrastructure orchestration.

### Requirements

- AWS Account
- python 3  # check the latest versions.
- boto3 
   pip install ansible boto3
- botocore >= 1.29.0
  

## EC2 -->
Amazon Elastic Compute Cloud is a part of Amazon.com’s cloud-computing platform, Amazon Web Services, that allows users to rent virtual computers on which to run their own computer applications.
## Ansible-->
Ansible is a suite of software tools that enables infrastructure as code. It is open-source and the suite includes software provisioning, configuration management, and application deployment functionality.
![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/6a214231-b38f-4f80-aa50-61495a48bbff)

### Creating an IAM user
You’ll need an AWS account with an IAM user at minimum to provision EC2 instances. These are made through: AWS Console > IAM >Access management> User > create user , as seen below
![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/0fcb3b3d-1926-407e-a7a2-b430a95cd86c)


![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/815db97b-6bdc-4ab7-b5fc-17f2bf8474f9)

#### Then select attach policy directly as seen below

![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/e564e13d-aa1f-4e66-8011-6a946ab19971)

#### Add AWS Access/Secret to Ansible Vault

Edit pass.yml to include your AWS access key and secret access key in .bashrc

ec2_access_key: 'AAAAAAAAAAAAAABBBBBBBBBBBB'.

ec2_secret_key: 'enter secret key which you created in IAM in user'

## Setup Ansible playbook
Use the code from launch ec2 instance file

### Run the following command Ansible to generate EC2 instances
$ ansible-playbook file-name.yml

![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/76afb562-1d78-4e1a-a3e9-77fa1ac3fc7e)


### Please verify the key pair in EC2 > Network & security > key pairs as seen below.

![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/6f517430-58f1-44ca-a951-c34e366d8403)

#### Now verify the EC2 instance created in EC2 instance as seen below.

![image](https://github.com/ShivalingBiradar/Ansible-aws/assets/149060582/de28ffbe-6e24-402c-81f4-00b22e761a63)


### Congratulations, you’ve now accessed your provisioned instance! through Ansible


