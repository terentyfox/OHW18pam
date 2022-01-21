# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
config.vm.box = "centos/7"
config.vm.box_version = "2004.01"
config.vm.provider "virtualbox" do |v|
v.memory = 256
v.cpus = 1
end
config.vm.define "sshs" do |sshs|
sshs.vm.network "private_network", ip: "192.168.50.10",
virtualbox__intnet: "net1"
sshs.vm.hostname = "sshs"
sshs.vm.provision "shell", path: "sshs_script.sh"
end
config.vm.define "sshc" do |sshc|
sshc.vm.network "private_network", ip: "192.168.50.11",
virtualbox__intnet: "net1"
sshc.vm.hostname = "sshc"
sshc.vm.provision "shell", path: "sshc_script.sh"
end
end
