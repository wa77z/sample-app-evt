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

### Install Git

 https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

 ````
 $ git version
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

#### Setup AWS Env Vars from IAM User
 
 https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-envvars.html

 ````
 $ aws sts get-caller-identity
 ````

#### 
