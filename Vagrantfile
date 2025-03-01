# -*- mode: ruby -*-
# vi: set ft=ruby :

# Place Vagrantfile in the directory you run vagrant from.
# This should also contain ubuntu.yml which configures the VMs.

# Setting for all VMs
Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 1
  end

  # Specific for ubuntu1
  config.vm.define "ubuntu1" do |ubuntu1|
    ubuntu1.vm.box = "ubuntu/jammy64"
    ubuntu1.vm.provision "ansible_local", playbook: "ubuntu.yml"
    ubuntu1.vm.hostname = "ubuntu1"
    ubuntu1.vm.network "private_network", ip: "192.168.56.101"
  end

  # Specific for ubuntu2
  config.vm.define "ubuntu2" do |ubuntu2|
    ubuntu2.vm.box = "ubuntu/jammy64"
    ubuntu2.vm.provision "ansible_local", playbook: "ubuntu.yml"
    ubuntu2.vm.hostname = "ubuntu2"
    ubuntu2.vm.network "private_network", ip: "192.168.56.102"
  end

  # Specific for ubuntu3
  config.vm.define "ubuntu3" do |ubuntu3|
    ubuntu3.vm.box = "ubuntu/jammy64"
    ubuntu3.vm.provision "ansible_local", playbook: "ubuntu.yml"
    ubuntu3.vm.hostname = "ubuntu3"
    ubuntu3.vm.network "private_network", ip: "192.168.56.103"
  end
end