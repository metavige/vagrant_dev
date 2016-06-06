# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  # config.vm.box = "williamyeh/ubuntu-trusty64-docker"
  config.vm.network "private_network", ip: "172.17.8.200"

  config.vm.provider :virtualbox do |vb|
    vb.memory = 2048
  end

  config.vm.synced_folder "/Users/rickychiang/workspace", "/home/vagrant/workspace"
  config.vm.synced_folder "/Users/rickychiang/sandbox", "/home/vagrant/sandbox"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
    ansible.sudo = true
  end

end
