VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
  end

  config.vm.synced_folder ENV['ARDANIS_WS'], "/home/vagrant/ardanis"

  config.vm.network "forwarded_port", guest: 4000, host: 4001, host_ip: "127.0.0.1"  
  config.vm.network "private_network", ip: "192.168.50.4" 

  config.vm.provision "file", source: "runserve.sh", destination: "runserve.sh"
  config.vm.provision :shell, :path => "bootstrap.sh", privileged: false  
end