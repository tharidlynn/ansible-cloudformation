## CloudFomration
aws cloudformation create-stack --stack-name Jenkins --template-body file://ec2.yaml --parameters ParameterKey=AvailabilityZoneParameter,ParameterValue=ap-southeast-1a ParameterKey=InstanceTypeParameter,ParameterValue=t2.micro ParameterKey=KeyNameParameter,ParameterValue=test

aws cloudformation delete-stack --stack-name Jenkins

## Define ssh key per host using ansible_ssh_private_key_file 
https://www.cyberciti.biz/faq/define-ssh-key-per-host-using-ansible_ssh_private_key_file/


## Setup your /etc/ansible/ansible.cfg

## Ansible galaxy
ansible-galaxy install --roles-path roles/ geerlingguy.java

## create key-pair 
aws ec2 create-key-pair --key-name test

## Ansible command
ansible -m ping -i hosts -u ubuntu --private-key ~/test.pem jenkins

ansible-playbook -i hosts site.yml

