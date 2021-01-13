# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian10"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
  config.vm.network "forwarded_port", guest: 8080, host: 9090, id: "apache2"
end
