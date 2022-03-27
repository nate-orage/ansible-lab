# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "minimal/xenial64"
  config.vm.network "public_network", bridge: "Realtek PCIe GBE Family Controller"
  config.vm.synced_folder ".", "/vagrant_data", disabled: true
  config.vm.provider "hyperv"
  config.vm.hostname = 'ub1'

  config.vm.provider "hyperv" do |h|
    h.enable_virtualization_extensions = false
    h.linked_clone = false
    h.memory = 2048
  end
  
  config.vm.provision "cent1" do |cent1|
    cent1.vm.box = "minimal/centos7"
    cent1.vm.hostname = 'cent1'
  end
end
