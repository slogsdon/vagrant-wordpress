# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.synced_folder ".", "/vagrant",
    owner: "vagrant",
    group: "www-data",
    mount_options: ["dmode=755,fmode=644"]

  config.vm.network :private_network, ip: "192.168.50.2"
  config.vm.hostname = "www.wordpress.local"

  if defined?(VagrantPlugins::HostsUpdater)
    config.hostsupdater.aliases = ['wordpress.local']
    config.hostsupdater.remove_on_suspend = true
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provisioning/wordpress.yml"
  end
end
