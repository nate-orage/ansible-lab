# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "envimation/ubuntu-xenial"
  config.vm.network "public_network", bridge: "Realtek PCIe GBE Family Controller"
  config.vm.synced_folder ".", "/vagrant_data", disabled: true
  config.vm.provider "hyperv"
  config.vm.hostname = 'ub1'

  config.vm.provider "hyperv" do |h|
    h.enable_virtualization_extensions = false
    h.linked_clone = false
    h.memory = 2048
  end
  
  config.vm.provision "ansible" do |a|
    a.verbose = "v"
    a.playbook = "playbook.yaml"
  end
end