# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/trusty64"
    config.vm.provision "docker"

    (1..1).each do |number|
        config.vm.define "swarm#{number}" do |node|
            node.vm.network "private_network", ip: "192.168.99.20#{number}"
            node.vm.hostname = "swarm#{number}"
        end  
    end

    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
        v.cpus = 1
    end

end
