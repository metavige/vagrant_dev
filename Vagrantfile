# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "172.17.8.200"
  
  config.vm.provider :virtualbox do |vb|
    vb.memory = 2048
  end

  config.vm.synced_folder "~/workspace", "/home/vagrant/workspace"
  config.vm.synced_folder "~/sandbox", "/home/vagrant/sandbox"
  config.vm.synced_folder "~/.gradle", "/home/vagrant/.gradle"
  config.vm.synced_folder "~/.m2", "/home/vagrant/.m2"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
