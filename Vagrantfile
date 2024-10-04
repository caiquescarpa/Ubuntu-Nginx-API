Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provision "shell", inline: "apt update && apt -y install nginx && service nginx start"
  config.vm.synced_folder "site", "/var/www/html"
end


