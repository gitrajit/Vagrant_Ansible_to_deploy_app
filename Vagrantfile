# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
config.vm.define "ansibleControl" do |ansibleControl|
        ansibleControl.vm.box = "ubuntu/trusty64"
        ansibleControl.vm.network "private_network", ip: "10.10.10.20"
        ansibleControl.vm.hostname ="DevOps"
        ansibleControl.vm.provider "virtualoadbalanceox" do |vb|
      vb.memory = "512"
      vb.name = "DevOps"
     vb.customize ["modifyvm", :id, "--cpuexecutioncap", "99"]
    end
    ansibleControl.vm.provision "ansible_local" do |a|
   a.playbook = "Ansible_setup/install_deploy_app.yml"
end
end
end
