# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config| 

  # General Vagrant VM configuration.
    config.vm.box = "centos/7"
    config.ssh.insert_key = false
    config.vm.synced_folder ".", "/vagrant", disabled: true
    config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

  # Web server 1.
  config.vm.define "web1" do |webservers|
    webservers.vm.hostname = "orc-web1.dev"
    webservers.vm.network "private_network", ip: "192.168.33.10"
  end

  # Web server 2.
  config.vm.define "web2" do |webservers|
    webservers.vm.hostname = "orc-web2.dev"
    webservers.vm.network "private_network", ip: "192.168.33.11"
  end

  # Web server 3.
    config.vm.define "web3" do |webservers|
      webservers.vm.hostname = "orc-web3.dev"
      webservers.vm.network "private_network", ip: "192.168.33.13"
    end

  # Web server 4.
    config.vm.define "web4" do |webservers|
      webservers.vm.hostname = "orc-web4.dev"
      webservers.vm.network "private_network", ip: "192.168.33.14"
    end


  # Database server.
  config.vm.define "db" do |dbservers|
    dbservers.vm.hostname = "orc-db.dev"
    dbservers.vm.network "private_network", ip: "192.168.33.20"
  end
end
