Vagrant.configure("2") do |config|
    config.vm.define "natalia_server" do |natalia_server|
        natalia_server.vm.box = "ubuntu/trusty64"
        config.vm.box_version = "20191107.0.0"
        config.ssh.username = "vagrant"
        config.ssh.password = "vagrant" 
        natalia_server.vm.network "private_network", :type => 'dhcp'
        natalia_server.vm.provider "virtualbox" do |vb|
            vb.name = "Natalia VM"
            vb.cpus = 2
            vb.customize ["modifyvm", :id, "--nic2", "hostonly", "--hostonlyadapter2", "vboxnet0"]
        end
        natalia_server.vm.provision "file", source: "/home/natalia/.ssh/id_ed25519.pub", destination: "/home/vagrant/.ssh/authorized_keys"
    end
    config.vm.define "natalia_server_2" do |natalia_server_2|
        natalia_server_2.vm.box = "ubuntu/trusty64"
        config.vm.box_version = "20191107.0.0"
        config.ssh.username = "vagrant"
        config.ssh.password = "vagrant" 
        natalia_server_2.vm.network "private_network", :type => 'dhcp'
        natalia_server_2.vm.provider "virtualbox" do |vb|
            vb.name = "Natalia VM 2"
            vb.cpus = 2
            vb.customize ["modifyvm", :id, "--nic2", "hostonly", "--hostonlyadapter2", "vboxnet0"]
        end
        natalia_server_2.vm.provision "file", source: "/home/natalia/.ssh/id_ed25519.pub", destination: "/home/vagrant/.ssh/authorized_keys"
    end
end
