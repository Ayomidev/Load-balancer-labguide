Vagrant.configure("2") do |config|
  config.vm.define "nginx" do |nginx|
    nginx.vm.box = "ubuntu/bionic64"
    nginx.vm.network "private_network", type: "dhcp"
    nginx.vm.provision "shell", path: "provision/nginx.sh"
  end

  # Configuration for Web Server 1
  config.vm.define "web1" do |web1|
    web1.vm.box = "ubuntu/bionic64"
    web1.vm.network "private_network", type: "dhcp"
    web1.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y nginx
      echo "This is Web Server 1" > /var/www/html/index.html
    SHELL
  end

  # Configuration for Web Server 2
  config.vm.define "web2" do |web2|
    web2.vm.box = "ubuntu/bionic64"
    web2.vm.network "private_network", type: "dhcp"
    web2.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y nginx
      echo "This is Web Server 2" > /var/www/html/index.html
    SHELL
  end

  # Configuration for Web Server 3
  config.vm.define "web3" do |web3|
    web3.vm.box = "ubuntu/bionic64"
    web3.vm.network "private_network", type: "dhcp"
    web3.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y nginx
      echo "This is Web Server 3" > /var/www/html/index.html
    SHELL
  end
end