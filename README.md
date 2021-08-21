This project runs a LAMP Server with CENTOS.

Includes all files to launch your box and apply the playbook included with ansible

Requirements

- Vagrant installed
- Virtualbox installed
- Ansible installed

Once installed all this packages, you can apply the stack running
ansible-playbook site.yml 

# Hacks to deploy this plalybook on amazon ec2 linux
 - Running a playbook python version issue
    https://prefetch.net/blog/2017/09/27/working-around-the-ansible-python2-yum-module-is-needed-for-this-module-error/
 - MySQL Setup
    https://www.samirdixit.com/plugin/article/view/6/how-to-setup-lamp-server-on-amazon-linux-2-ami
 
 - Root password setup and expiration issue on mysql  Ver 14.14 Distrib 5.7.35, 
    https://www.ryadel.com/en/mysql-user-password-expired-permanently-fix/
