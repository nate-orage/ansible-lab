# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "minimal/xenial64"
  config.vm.synced_folder ".", "/vagrant_data", disabled: true
  config.vm.provider "hyperv"

  config.vm.provider "hyperv" do |h|
    h.enable_virtualization_extensions = false
    h.linked_clone = false
    h.memory = 2048
  end

  config.vm.define 'ub1' do |ub1|
    ub1.vm.hostname = 'ub1'
    ub1.vm.network 'public_network', bridge: "Realtek PCIe GBE Family Controller", ip: "192.168.1.206"
  end
  
  config.vm.define "fed1" do |fed1|
    fed1.vm.box = "fedora/34-cloud-base"
    fed1.vm.box_version = "34.20210423.0"
    fed1.vm.network 'public_network', bridge: "Realtek PCIe GBE Family Controller", ip: "192.168.1.207"
    fed1.vm.hostname = 'fed1'
  end
end
