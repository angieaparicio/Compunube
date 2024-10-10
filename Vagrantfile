# -- mode: ruby --
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  if Vagrant.has_plugin? "vagrant-vbguest"
  config.vbguest.no_install = true
  config.vbguest.auto_update = false
  config.vbguest.no_remote = true
  config.vm.synced_folder "C:/Users/Angie Tatiana/Desktop/Computacion en la nube/pruebanube","/home/vagrant/Angie"
  end

  config.vm.define :clienteUbuntu do |clienteUbuntu|
  config.vm.boot_timeout = 600  # Aumenta el tiempo de espera a 10 minutos (600 segundos)
  clienteUbuntu.vm.box = "bento/ubuntu-20.04"
  clienteUbuntu.vm.network :private_network, ip: "192.168.100.2"
  clienteUbuntu.vm.hostname = "clienteUbuntu"
  
  end
  config.vm.define :servidorUbuntu do |servidorUbuntu|
    config.vm.boot_timeout = 600  # Aumenta el tiempo de espera a 10 minutos (600 segundos)
  servidorUbuntu.vm.box = "bento/ubuntu-20.04"
  servidorUbuntu.vm.network :private_network, ip: "192.168.100.3"
  servidorUbuntu.vm.hostname = "servidorUbuntu"
  end
end
