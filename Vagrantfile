# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.synced_folder ".", "/vagrant",
    owner: "vagrant",
    group: "www-data",
    mount_options: ["dmode=755,fmode=644"]

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provisioning/wordpress.yml"
  end
end