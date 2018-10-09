# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "16000"
  end
  config.vm.synced_folder "../SCclust/", "/vagrant/SCclustSource"
end
