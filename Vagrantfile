
Vagrant.configure("2") do |config|
  # Base box
  config.vm.box = "ubuntu/trusty64"

  # accessing "localhost:300" will access port 80 on the guest machine.
  config.vm.network "forwarded_port", guest: 80, host: 3000

  # add docker provisioner and load image
  config.vm.provision "docker", images: ['urban/node']
end
