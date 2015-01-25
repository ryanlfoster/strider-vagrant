# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "eneset-centos7-vagrant"
  config.vm.box_url = "https://s3.amazonaws.com/eneset/vagrant-boxes/eneset-centos7-vagrant.box"
  config.vm.hostname = "strider.eneset.local"

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "4096"]
    vb.cpus = 4
    vb.gui = false
  end

  config.vm.network "forwarded_port", guest: 3000, host: 3001 
  config.vm.synced_folder ENV['HOME'], "/home/vagrant/home"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible.yml"
  end
end
