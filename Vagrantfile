Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04"
  config.vm.network :forwarded_port, guest: 8080, host: 8080

  config.vm.provision "ansible" do |ansible|
        ansible.become = true
        ansible.verbose = "v"        
        #ansible.extra_vars = "ansible_extra_vars.yml"
        #ansible.vault_password_file="~/.vault_pass.txt"
        
        ansible.playbook = "install_airflow.yaml"
  end
end
