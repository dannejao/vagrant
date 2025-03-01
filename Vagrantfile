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

  # Specific for debian1
  config.vm.define "debian1" do |debian1|
    debian1.vm.box = "debian/bookworm64"
	debian1.vm.box_version = "12.20250126.1"
    debian1.vm.provision "ansible_local", playbook: "debian.yml"
    debian1.vm.hostname = "debian1"
    debian1.vm.network "private_network", ip: "192.168.56.101"
  end

  # Specific for debian2
  config.vm.define "debian2" do |debian2|
    debian2.vm.box = "debian/bookworm64"
	debian2.vm.box_version = "12.20250126.1"
    debian2.vm.provision "ansible_local", playbook: "debian.yml"
    debian2.vm.hostname = "debian2"
    debian2.vm.network "private_network", ip: "192.168.56.102"
  end

  # Specific for debian3
  config.vm.define "debian3" do |debian3|
    debian3.vm.box = "debian/bookworm64"
	debian3.vm.box_version = "12.20250126.1"
    debian3.vm.provision "ansible_local", playbook: "debian.yml"
    debian3.vm.hostname = "debian3"
    debian3.vm.network "private_network", ip: "192.168.56.103"
  end
end