# -*- mode: ruby -*-
# vi: set ft=ruby :

# from:
# <https://github.com/TheGrimmScientist/VagrantBoxes/blob/master/VanillaSparkBox/Vagrantfile>

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Assign the box to start from:
  config.vm.box = "precise32"
  # config.vm.network "forwarded_port", guest: 8888, host: 18888

  # Assign where to find the box if not already available locally:
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  # Tell Vagrant what commands to run to provision our box
  config.vm.provision :shell, inline: "sudo apt-get -y update"
  config.vm.provision :shell, inline: "sudo apt-get -y install openjdk-7-jdk"
  config.vm.provision :shell, inline: "wget http://d3kbcqa49mib13.cloudfront.net/spark-1.1.0-bin-hadoop1.tgz"
  config.vm.provision :shell, inline: "tar -zxf spark-1.1.0-bin-hadoop1.tgz"

end
