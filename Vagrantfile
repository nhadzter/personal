# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :web do |web|
    web.vm.box = "ubuntu/bionic64"
    web.vm.hostname = "web.nhadzter.local"
    web.vm.provider "virtualbox" do |vbox|
      vbox.name = "web"
      vbox.memory = 4096
      vbox.cpus = 2
    end
    web.vm.network "private_network", :ip => "192.168.56.128", :name => "vboxnet0", :adapter => 2
  end

  config.vm.define :db do |db|
    db.vm.box = "ubuntu/bionic64"
    db.vm.hostname = "db.nhadzter.local"
    db.vm.provider "virtualbox" do |vbox|
      vbox.name = "db"
      vbox.memory = 4096
      vbox.cpus = 2
    end
    db.vm.network "private_network", :ip => "192.168.56.160", :name => "vboxnet0", :adapter => 2
  end

  config.vm.define :gitlab do |gitlab|
    gitlab.vm.box = "ubuntu/bionic64"
    gitlab.vm.hostname = "gitlab.nhadzter.local"
    gitlab.vm.provider "virtualbox" do |vbox|
      vbox.name = "gitlab"
      vbox.memory = 4096
      vbox.cpus = 2
    end
    gitlab.vm.network "private_network", :ip => "192.168.56.192", :name => "vboxnet0", :adapter => 2
  end

  config.vm.define :microk8s do |microk8s|
    microk8s.vm.box = "ubuntu/bionic64"
    microk8s.vm.hostname = "microk8s.nhadzter.local"
    microk8s.vm.provider "virtualbox" do |vbox|
      vbox.name = "microk8s"
      vbox.memory = 8192
      vbox.cpus = 4
    end
    microk8s.vm.network "private_network", :ip => "192.168.56.224", :name => "vboxnet0", :adapter => 2
  end
end
