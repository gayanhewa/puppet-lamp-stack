Vagrant.configure("2") do |config|

  # Enable the Puppet provisioner, with will look in manifests
  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file = "default.pp"
    puppet.module_path = "modules"
  end

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "precise32"

  # Forward guest port 80 to host port 8888 and name mapping
  config.vm.network "private_network", ip: "192.168.50.4"

  config.vm.synced_folder "/home/gayan/Workspace/webroot/", "/vagrant/webroot/", :owner => "www-data"
end
