# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |mysql|
  mysql.vm.box = "ubuntu/xenial64"
  mysql.vm.network :forwarded_port, guest: 3306, host: 3306
  mysql.vm.provision :shell, :path => "install.sh"
  mysql.vm.synced_folder ".", "/vagrant", type: "sshfs"
end
