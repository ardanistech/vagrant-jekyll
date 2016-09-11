# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
  end

  config.vm.network "forwarded_port", guest: 4000, host: 4000

  config.vm.synced_folder ENV['ARDANIS_WS'], "/home/vagrant/ardanis"

  config.vm.provision "file", source: "runserve.sh", destination: "runserve.sh"
  config.vm.provision :shell, :path => "bootstrap.sh", privileged: false 
   
end