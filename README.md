# SRE Code Challenge - Outyet Packer AMI Build

This is the Packer build for the outyet AMI. It uses an Ansible playbook to configure an Amazon Linux 2 AMI with golang and the outyet goland app. A systemd service unit file is included to ensure outyet runs as a daemon on startup, when launched in EC2

## Build
1. Ensure your AWS CLI is configured and Packer is installed
2. `packer build outyet-ami.json`

## Test
 
There are currently no tests included, but if you want to test the Ansible playbook locally, you can use the included Vagrantfile

NOTE: It runs in CentOS 7, not Amazon Linux 2

1. Ensure Vagrant and VirtualBox is installed
2. `vagrant up`
