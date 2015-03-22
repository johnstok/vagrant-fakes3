VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "dev" do |dev|
    dev.vm.box = "ubuntu/trusty64"
    dev.vm.hostname = "fakes3"
    dev.vm.provider "virtualbox" do |v|
    end
    config.vm.network :forwarded_port, host: 4567, guest: 4567
    config.vm.provision "shell", path: "provision.sh"
  end
end
