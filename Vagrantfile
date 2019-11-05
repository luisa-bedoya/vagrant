Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "web_1" do |web_1|
    web_1.vm.box = "ubuntu/xenial64"
    web_1.vm.network "forwarded_port", guest: 80, host: 8080
    web_1.vm.synced_folder "/Users/luisabedoya/vagrant/web_1/", "/var/www/html/"
  end

  config.vm.define "web_2" do |web_2|
    web_2.vm.box = "ubuntu/xenial64"
    web_2.vm.network "forwarded_port", guest: 80, host: 8008
    web_2.vm.synced_folder "/Users/luisabedoya/vagrant/web_2/", "/var/www/html/"
  end
end
