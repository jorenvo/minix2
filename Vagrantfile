# Vagrantfile from Brown's CS1670
VAGRANT_BOX_MEMORY = 4096
VAGRANT_BOX_CPUS = 4

Vagrant.configure("2") do |config|

  # Ubuntu 18.04
  config.vm.box = "ubuntu/bionic64"

  # Set the Vagrant box's RAM
  config.vm.provider :virtualbox do |vb|
    vb.memory = VAGRANT_BOX_MEMORY
    vb.cpus = VAGRANT_BOX_CPUS
  end

  config.vm.provision :shell, :inline => %Q{
    apt-get update
    apt-get install apt-file make build-essential qemu gdb linux-modules-extra-4.15.0-135-generic -y
    # apt-file update
  }
end
