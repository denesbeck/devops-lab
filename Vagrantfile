Vagrant.configure("2") do |config|
  machines=[
    {
      :hostname => "node-1",
      :box => "ubuntu/bionic64",
      :ip => "192.168.56.11",
      :ssh_port => '2200'
    },
     {
      :hostname => "node-2",
      :box => "ubuntu/bionic64",
      :ip => "192.168.56.12",
      :ssh_port => '2200'
    },
     {
      :hostname => "node-3",
      :box => "ubuntu/bionic64",
      :ip => "192.168.56.13",
      :ssh_port => '2200'
    },
     {
      :hostname => "node-4",
      :box => "ubuntu/bionic64",
      :ip => "192.168.56.14",
      :ssh_port => '2200'
    },
     {
      :hostname => "node-5",
      :box => "ubuntu/bionic64",
      :ip => "192.168.56.15",
      :ssh_port => '2200'
    }
  ]

  machines.each do |machine|
    config.vm.define machine[:hostname] do |node|
      node.vm.box = machine[:box]
      node.vm.hostname = machine[:hostname]
      node.vm.network "private_network", ip: machine[:ip]
      node.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        vb.cpus = "2"
      end
    end
  end
end
