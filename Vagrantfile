# Install required plugins
required_plugins = ["vagrant-hostsupdater"]
required_plugins.each do |plugin|
    exec "vagrant plugin install #{plugin}" unless Vagrant.has_plugin? plugin
end

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", ip: "192.168.10.100"
  config.vm.hostname = "www.testing.de"
  config.hostsupdater.aliases = ["development.local"]
  # Sync the app folder(not copying in, syncing so is we make changes in the vm, reflected here too)
  # config.vm.synced_folder"path/to/origin/folder", "path to destination"
  config.vm.synced_folder"app", "/app"

  # Run the provision script
  config.vm.provision "shell",path: "environment/provision.sh"

end
