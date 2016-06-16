# Defines our Vagrant environment
# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  # create some ubuntu nodes
  3.times do |i|
    config.vm.define "node#{i}" do |conf|
      conf.vm.box = "ubuntu/trusty64"
      conf.vm.hostname = "node#{i}.com"
      conf.vm.network :private_network, ip: "10.0.15.2#{i}"
      conf.vm.network "forwarded_port", guest: 80, host: "8082"
      conf.vm.provider "virtualbox"
    end
  end

  # create a centos node
  config.vm.define "node4" do |conf|
    conf.vm.box = "bento/centos-6.7"
    conf.vm.hostname = "node4.com"
    conf.vm.network :private_network, ip: "10.0.15.25"
    conf.vm.network "forwarded_port", guest: 80, host: "8082"
    conf.vm.provider "virtualbox"
  end
end
