Vagrant.configure("2") do |config|
    config.vm.define "natalia_server" do |natalia_server|
        natalia_server.vm.box = "ubuntu/trusty64"
        config.vm.box_version = "20191107.0.0"
        natalia_server.vm.network "private_network", :type => 'dhcp'
        natalia_server.vm.provider "virtualbox" do |vb|
            vb.name = "Natalia VM"
            vb.cpus = 2
            vb.customize ["modifyvm", :id, "--nic2", "hostonly", "--hostonlyadapter2", "vboxnet0"]
        end
    end
end