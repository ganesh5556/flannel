Vagrant.configure("2") do | config |
  config.vm.define "kmaster" do | kmaster |
    kmaster.vm.box = "ubuntu/focal64"
    kmaster.vm.network "private_network", ip: "192.168.20.10"
    kmaster.vm.network "forwarded_port", guest: 8082, host: 8082
    kmaster.vm.hostname = "kmaster"
    kmaster.vm.provider "virtualbox" do |vb|
      vb.cpus = 2
      vb.memory = 2048
      vb.name = "kmaster"
    end
  end
  config.vm.define "wnode1" do | wnode1 |
    wnode1.vm.box = "ubuntu/focal64"
    wnode1.vm.network "private_network", ip: "192.168.20.11"
    wnode1.vm.hostname = "wnode1"
    wnode1.vm.provider "virtualbox" do |vb| 
      vb.cpus = 1
      vb.memory = 1024
      vb.name = "wnode1"
    end
  end
end
