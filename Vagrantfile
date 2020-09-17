# -*- mode: ruby -*-
# vi: set ft=ruby :


#Vagrant.configure("2") do |config|
#
#  config.vm.box = "kborax/k3os"
#  config.vm.provider "hyperv"
#  config.vm.network "public_network"
#
#end

Vagrant.configure("2") do |config|
  config.vm.define "web" do |web|
    web.vm.box = "hashicorp/precise64"
    web.vm.hostname = 'web'


    web.vm.network :private_network, ip: "192.168.56.101"

    web.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "web"]
    end
  end

  config.vm.define "db" do |db|
    db.vm.box = "hashicorp/precise64"
    db.vm.hostname = 'db'

    db.vm.network :private_network, ip: "192.168.56.102"

    db.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "db"]
    end
  end
end