# -*- mode: ruby -*-
# vi: set ft=ruby :



Vagrant.configure("2") do |config|

  config.vm.define "primary" do |primary|
    primary.vm.box = "kborax/k3os"
    primary.vm.provider "hyperv"
    primary.vm.network "public_network"
    primary.vm.hostname = "primary"
  end

  config.vm.define "worker" do |worker|
    worker.vm.box = "kborax/k3os"
    worker.vm.provider "hyperv"
    worker.vm.network "public_network"
    worker.vm.hostname = "worker"
  end
end