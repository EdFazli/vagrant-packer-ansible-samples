# AWS CI/CD AUTOMATION 
AWS CI/CD Automation using tools:
1. Visual Studio Code + Git
2. Vagrant
3. Azure DevOps
4. Packer
5. Terraform
6. Ansible

## INITIAL SETUP
Description on the installation process for each tools.  
  
### VISUAL STUDIO CODE + GIT
Download the installer here:  
- VS Code: [Visual Studio Code Installer](https://code.visualstudio.com/).
- Git: [Git Installer](https://git-scm.com/).  
  
**Git Setup**  
For ITOPS, we will be having a total of 3 branches (1 main + 2 branches).  
*Main* branch is the only one that will be used to deploy the infrastructure into the AWS environment (SIT/UAT/PROD) with approval.  
Daily development will use the *dev* branch.  
Any new tools suggestion/enhancement will be done on *addon* branch first before merge to *dev* branch.  
  
Git Clone:
Using any CLI that has Git features supported (Recommend to use [Git Bash](https://git-scm.com/))  
- In CLI, change to which directory you want the repo to be clone.  
- Run command *git clone https://edfazli92@dev.azure.com/edfazli92/TerraformAnsible_CICD/_git/TerraformAnsible_CICD*.  
  
**VS Code Extensions**  
Ensure the extensions below are installed in your VS Code:  
1. [Hashicorp Terraform](hashicorp.terraform).
2. [Python](ms-python.python).
3. [YAML](redhat.vscode-yaml).
4. [JSON](zainchen.json).
5. [Ansible](tomaciazek.ansible).
  
### VAGRANT
Download the installer here:  
- Vagrant: [Vagrant Installer](https://www.vagrantup.com/downloads).
  
**Vagrant** is a tool for managing VM environment as a code (ideal to separate development environment on your laptop).  
  
Prerequisites:  
- Virtualbox: [Virtual Installer](https://www.virtualbox.org/).  
- Vagrant Image : [CentOS/8](https://app.vagrantup.com/centos/boxes/8).  
  
1. Download and install Vagrant based on the version of your OS.  
2. Open PowerShell and change directory to which you want the vagrant configuration to be located.  
3. Run command > *vagrant init centos/8* (This will create vagrantfile in the directory).  
4. Edit the vagrantfile as in the repository.  
5. Run command > *vagrant plugin install vagrant-vbguest*.  
6. Run command > *vagrant up* to start the VM.  
7. To test connectivity can run ping command on the VM's private IP assigned.  
8. Run command > *vagrant ssh* to remote into the VM.  
9. Run command > *vagrant halt* and *vagrant up* to reboot or update the new configuration.  
  
Troubleshooting Vagrant:
1. Error output = mount: /home/vagrant/data: unknown filesystem type 'vboxsf'.  
- Run command > *vagrant plugin update vagrant-vbguest*.  
2. Stderr: VBoxManage.exe: error: Failed to open/create the internal network 'HostInterfaceNetworking-VirtualBox Host-Only Ethernet Adapter' (VERR_INTNET_FLT_IF_NOT_FOUND).  
- Go to Device Manager and search for your VirtualBox Host-Only Adaptor. Then disable and enable it back.  
3. Stderr: VBoxManage.exe: error: The VM session was closed before any attempt to power it on.
VBoxManage.exe: error: Details: code E_FAIL (0x80004005), component SessionMachine, interface ISession.  
- Open Task Manager and right-click on Virtual Box Headless Frontend session. Then click end task.  
  
### AZURE DEVOPS
URL Reference: https://dev.azure.com/edfazli92/_git/TerraformAnsible_CICD.  
Project Name: **AscentisITOPS**.  
Repository Name: **TerraformAnsible_CI/CD**.  
Extensions: [Terraform](https://marketplace.visualstudio.com/items?itemName=ms-devlabs.custom-terraform-tasks) by Microsoft DevLabs.  
  
### PACKER  
Download the installer here:  
- Packer: [Packer Installer](https://www.packer.io/).  
  
Installation has been done in Vagrant environment (refer ../Vagrant/vagrantfile).  
  
### TERRAFORM  
Download the installer here:  
- Terraform: [Terraform Installer](https://www.terraform.io/downloads.html).  
  
Installation has been done in Vagrant environment (refer ../Vagrant/vagrantfile).  
  
### ANSIBLE  
Ansible installation guide:  
- Ansible: [Ansible Installation Guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html?extIdCarryOver=true&sc_cid=701f2000001OH7YAAW).  
  
Installation has been done in Vagrant environment (refer ../Vagrant/vagrantfile).  
  
## SOFTWARE DEPENDENCIES  
Please take note on the dependencies as below.  
  
Terraform:  
-  
  
Ansible:  
-  
  
## VARIABLES REFERENCES  
  
## CI/CD PIPELINES  
Description on how to build terraform/ansible code and run the scripts.  
  
## REVIEWER  
ITOPS person in charge to review and merge scripts to main repository and deploy the changes.  
  
## LATEST RELEASES  
  
## CONTRIBUTING  
We are pleased for anyone who want to contribute and participate in this project which you can:
1. Raise a [ticket for bugs and feature requests](URL) and help us verify once they are implemented. 
2. Review [source code changes](URL).
3. Review the [documentation](URL) and make pull requests for any improvements.  
  
**TOGETHER WE MAKE ASCENTIS BETTER**  
