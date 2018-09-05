Vagrant.configure("2") do |config|
  config.ssh.insert_key = false

  config.vm.define "lb01" do |lb01|
    lb01.vm.box = "centos/7"
    lb01.vm.network "forwarded_port", guest: 80, host: 8080
    lb01.vm.network "private_network", ip: "192.168.76.82"
  end

  config.vm.define "app01" do |app01|
    app01.vm.box = "centos/7"
    app01.vm.network "forwarded_port", guest: 80, host: 8081
    app01.vm.network "private_network", ip: "192.168.76.83"
  end

  config.vm.define "app02" do |app02|
    app02.vm.box = "centos/7"
    app02.vm.network "forwarded_port", guest: 80, host: 8082
    app02.vm.network "private_network", ip: "192.168.76.84"
  end

  config.vm.define "db01" do |db01|
    db01.vm.box = "centos/7"
    db01.vm.network "private_network", ip: "192.168.76.85"
  end

end
