# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
config.vm.define "ansibleControl" do |ansibleControl|
	ansibleControl.vm.box = "./trusty-server-cloudimg-amd64-vagrant-disk1.box"
	ansibleControl.vm.network "private_network", ip: "10.10.10.10"
	ansibleControl.vm.hostname ="DevOps"
	ansibleControl.vm.provider "virtualoadbalanceox" do |vb|
      vb.memory = "512"
      vb.name = "DevOps"
     vb.cpu = 2
    end
    ansibleControl.vm.provision "ansible_local" do |a|
   a.playbook = "Ansible_setup/install_deploy_app.yml"	
end
end
end

