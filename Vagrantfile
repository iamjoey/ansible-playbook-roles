# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "private_network", ip: "192.168.56.101"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    # ansible.verbose = "vvv"
  end

end
