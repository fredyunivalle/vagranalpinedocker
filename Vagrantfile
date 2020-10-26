# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "docker" do |docker|
      docker.vm.provider :virtualbox do |vb|
        vb.name = "linuxdocker"
      end
      docker.vm.box = "alpine/alpine64"
      docker.vm.provision "shell", path: "script.sh"
      config.vm.network "forwarded_port", guest: 5432, host: 5432
  end
end
