# tf_add_volume

## Object
A simple playbook to add volume to an OpenStack instance.

### Install prequisits: Terraform and Packer on Linux x86_64 plateforms
```bash
sudo unlink /usr/bin/terraform                                                                                                                                                                                                       
sudo unlink /usr/bin/packer
mkdir ~/{terraform_0.8.6,packer_0.12.3}


rm /usr/bin/{terraform,packer}

cd ~/terraform_0.8.6 && curl -O https://releases.hashicorp.com/terraform/0.8.6/terraform_0.8.6_linux_amd64.zip
cd ~/packer_0.12.3 && curl -O https://releases.hashicorp.com/packer/0.12.3/packer_0.12.3_linux_amd64.zip
cd ~/terraform_0.8.6 && unzip terraform_0.8.6_linux_amd64.zip && sudo ln -s ~/terraform_0.8.6/terraform /usr/bin/terraform
cd ~/packer_0.12.3 && unzip packer_0.12.3_linux_amd64.zip && sudo ln -s ~/packer_0.12.3/packer /usr/bin/packer
```

### verify we're all set to terraform and packer.
```bash
terraform
packer
```

### Download credentials file from Horizon OpenStack
Go to your Horizon Project and click to Access and Security


Put your project_name.sh file into a folder outside your git local repo.
Source the file by taping:
```bash
source ~/path_folder/project_name.sh
echo $OS_USERNAME
```