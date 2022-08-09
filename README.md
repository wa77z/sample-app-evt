# sample-app-evt
 two tier application deployed from a mac using ansible and aws (free tier)

## PreReqs
 
 Install and configure software required to deploy the sample application and supporting infrastructure.

### Install Ansible 

 https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html

 ````
 $ ansible --version
 ````

### Install AWSCLI

 https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

 ````
 $ aws --version
 ````

### Install Git, Clone Repo

 https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

 ````
 $ git version
 ````

 ````
 $ git clone https://github.com/wa77z/sample-app-evt.git
 ````
 
### Create an AWS Account

 https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/

#### Create an IAM user w/ Security Credentials
 
 https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html


#### Create and Import an SSH key pair

 https://docs.aws.amazon.com/cli/latest/reference/ec2/import-key-pair.html
 
 Launch a terminal in macOS

 ````
 $ mkdir ~/.ssh/
 $ cd ~/.ssh/
 $ ssh-keygen -t rsa -b 2048
 $ [enter]
 $ [enter]
 $ cd ~/

 $ cat ~/.ssh/id_rsa.pub
 ````

#### Setup AWS Env Vars
 
 https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html

 Verify Credentials and Account
 ````
 $ aws sts get-caller-identity
 ````

 Export (3) Vars for AWS resources
 ````
 $ export VPC_ID=vpc-ff683085
 $ export KEY_PAIR=wa77z
 $ export SUBNET=subnet-39bab365
 ````

### Export Ansible Env Vars

 ````
 $ export ANSIBLE_HOST_KEY_CHECKING=False
 ````
 
## Run Ansible Playbooks

 ````
 $ ansible-playbook all-in-one.yaml -v
 ````



