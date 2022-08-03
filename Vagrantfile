# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  

  # Box Settings 
  config.vm.box = "hashicorp/bionic64"

  # Network Settings 
  #config.vm.network "forwarded_port", guest: 80, host: 8000
  #config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  config.vm.network "private_network", ip:"192.168.56.10"
  # config.vm.network "public_network"


  # Provider Settings 
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus = 4 
  end
  

  # Folder Settings 
  config.vm.synced_folder ".", "/var/www/pyhton"

  
  # # Provision Settings 
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   sudo apt-get -y install uvicorn
  # SHELL

  config.vm.provision "shell", path: "bootstrap.sh"




end
