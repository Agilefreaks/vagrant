# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  config.ssh.forward_agent = true

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.define  "win" do |win|
    win.vm.box = "windows-2008R2-serverstandard-amd64_virtualbox"
    win.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--memory", 3072]
      vb.customize ["modifyvm", :id, "--chipset", 'ICH9']
    end
  end

  config.vm.define  "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/trusty64"
    ubuntu.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--memory", 2048]
    end
  end

  config.vm.define  "buntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/trusty64"
    ubuntu.vm.provider "virtualbox" do |vb|
      vb.customize ["modifyvm", :id, "--memory", 2048]
    end
  end

  config.vm.network "public_network"
end
