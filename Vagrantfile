# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  machine_name = "ansible-playground"
  config.vm.define machine_name do |vm_config|
    vm_config.vm.host_name = "ansible-playground.local"
    vm_config.vm.network "private_network", ip: "192.168.19.21"

    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/playbooks/vagrancy.yml"
      # ansible.sudo = true
      # ansible.groups = {}
      # ansible.extra_vars = {}
      # ansible.tags = %w()
      # ansible.inventory_path = ""
      # ansible.limit = ""
      # ansible.vault_password_file = ""
      # ansible.skip_tags = %w()
      # ansible.start_at_task = ""
      # ansible.raw_arguments = %w()
    end
  end
end
