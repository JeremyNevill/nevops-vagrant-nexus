# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|

  # Vagrant Box (Centos/7) with Minimal Nexus 3 Install
  # ===================================================
  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 8080, host: 8080

  config.vm.provider "virtualbox" do |vb|
     vb.gui = true
     vb.memory = "1024"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "nexus-server.yml"
  end

end
