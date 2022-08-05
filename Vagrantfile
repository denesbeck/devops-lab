IMAGE_NAME="ubuntu/bionic64"
N = 5

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 2
  end
  # config.vm.define "master" do |master|
  #   master.vm.box = IMAGE_NAME
  #   master.vm.hostname = "master"
  #   master.vm.network "private_network", ip: "192.168.56.10"
  # end
  (1..N).each do |i|
    config.vm.define "node-#{i}" do |node|
      node.vm.box = IMAGE_NAME
      node.vm.hostname = "node-#{i}"
      node.vm.network "private_network", ip: "192.168.56.#{i + 10}"
    end
  end
end
