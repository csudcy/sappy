# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "precise32"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"


  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"


  # See https://gist.github.com/gabrielhpugliese/5855677
  config.vm.provision :shell, :path => "meteor.sh"
  config.vm.network :forwarded_port, guest: 3000, host: 3000
  #config.vm.provider "virtualbox" do |vb|
  #  # vb.gui = true
  #  vb.customize [
  #    "setextradata",
  #    :id,
  #    "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root",
  #    "1"
  #  ]
  #end
end