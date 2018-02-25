# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "kny5/spectralworkbench"
  #config.vm.box_version = "0.1"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  config.vm.network "forwarded_port", guest: 3000, host: 8080

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  #uncomment lines 67 to 71 to activate vagrant provision in order to use "vagrant up --provision"
  #this is useful only if you want a bulleproof server" the only way to stop it is using "vagrant ssh -c 'sudo poweroff'"
#  config.vm.provision "shell", inline: <<-SHELL
#  su vagrant;
#  cd /home/vagrant/spectral-workbench;
#  /usr/share/rvm/gems/ruby-2.1.2@global/bin/bundle exec passenger start;
#  SHELL
end
