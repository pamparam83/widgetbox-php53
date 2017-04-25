# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
  end

  # UNIX users can use the nfs switch
  # config.vm.synced_folder ".", "/var/www", :nfs => true
  config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]

  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"  
  config.vm.network "private_network", ip: "192.168.66.6"  
  config.vm.hostname = "widgetbox-php53"
  config.vm.provision "shell", path: "provision.sh"

end