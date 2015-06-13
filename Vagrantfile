# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "geerlingguy/centos7"

  config.vm.network "private_network", ip: "192.168.38.10"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", 1024]
    vb.customize ["modifyvm", :id, "--cpus", 2]
    vb.customize ["modifyvm", :id, "--name", "satnogs"]
  end

  #config.vm.synced_folder '.', '/vagrant', disabled: true

  config.vm.hostname = "satnogs"

  # Set the name of the VM. See: http://stackoverflow.com/a/17864388/100134
  config.vm.define :satnogs do |satnogs|
  end

  # Ansible provisioner
  # Make sure the vault passwd file is decrypted
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "main.yml"
    ansible.inventory_path = "vagrant_hosts"
    ansible.host_key_checking = false
    ansible.vault_password_file = "vault-passwd.txt"
    ansible.extra_vars = { env: 'test'
    }
  end
end
