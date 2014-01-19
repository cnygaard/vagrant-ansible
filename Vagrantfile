Vagrant.configure("2") do |config|
   config.vm.network :private_network, ip: "192.168.111.222"
#  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.box = "raring32"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/raring/current/raring-server-cloudimg-i386-vagrant-disk1.box"

  config.vm.provider "virtualbox" do |vb|
     vb.customize ["modifyvm", :id, "--memory", "512"]
  end

  config.vm.provider "virtualbox" do |v|
    v.gui = false
  end

  # Synced folders
  config.vm.synced_folder "ansible/", "/ansible"

# Add ansible inside the virtual machine, run ansible-playbook against /ansible/playbook.yml
  config.vm.provision :shell, :inline => "sudo apt-get -y install python-software-properties"
  config.vm.provision :shell, :inline => "sudo add-apt-repository -y ppa:rquillo/ansible"
  config.vm.provision :shell, :inline => "sudo apt-get update"
  config.vm.provision :shell, :inline => "sudo apt-get -y install ansible"
  config.vm.provision :shell, :inline => "echo localhost | sudo tee -a /etc/ansible/hosts"
  config.vm.provision :shell, :inline => "sudo ansible-playbook /ansible/playbook.yml --connection=local"

end
