# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

$script = <<-'SCRIPT'
echo installing unzip needed by Bodylight.js-FMU-Compiler
yum -y install unzip zip
date > /etc/vagrant_provisioned_at
SCRIPT

Vagrant.configure("2") do |config|

  config.vm.box = "https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/BodyligthVMImage/22.09/bodylightvm.box"
  # config.vm.box = "https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/BodyligthVMImage/21.02/bodylightvm.box"
  # config.vm.box = "https://filedn.com/lHGc7w3H4jOpIe46u1nPt57/BodyligthVMImage/21.10/bodylightvm.box"
  # config.vm.box = "bodylightvm.box"

  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
     vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
     vb.memory = "4096"
     vb.cpus = "2"
     vb.customize ["modifyvm", :id, "--vram", "128"]
     vb.name = "Bodylight-VirtualMachine"
  end
 
  puts "vagrant version:"
  puts Vagrant::VERSION
  config.vm.provision "shell", inline: $script
  config.vm.synced_folder "..", "/vagrant"
  # vagrant data mapping is mapped up to one parent (..) 
  # uncomment next row and comment row bellow to map up to 2 parent directories (../..) 
  # config.vm.synced_folder "../..", "/vagrant_data"
  config.vm.synced_folder "../..", "/vagrant_data"
  
end
