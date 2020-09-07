# encoding: utf-8
# -*- mode: ruby -*-
# vi: set ft=ruby :
# Box / OS
# Install ansible first
# On ubuntu host run:
# sudo apt-add-repository ppa:ansible/ansible
# sudo apt update
# sudo apt install ansible

VAGRANT_BOX = 'bento/centos-6'

VM_NAME = 'lamp-service'

Vagrant.configure(2) do |config|
    
    # Set ssh_key to use with the vm
    config.ssh.insert_key = false
    config.vm.synced_folder "./provision", "/vagrant_data/hostSharedFiles"
    config.vm.define "lampBox" do |lampBox| 
        # Set vagrant box from hashicorp
        lampBox.vm.box = VAGRANT_BOX
        # Set hostname
        lampBox.vm.hostname = VM_NAME
        lampBox.vm.network "private_network", ip: "192.168.50.4"
        lampBox.vm.network "forwarded_port", host: 8081, guest: 80
        lampBox.vm.provider 'virtualbox' do |v|
            v.name = VM_NAME
            v.memory = 128
        end
    end
    #config.vm.provision 'ansible_local' do |vprovision|
    #    vprovision.limit = 'all'
    #    vprovision.inventory_path = 'hosts'
    #    vprovision.playbook = 'site.yml'
    #end
end
