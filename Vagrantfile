
Vagrant.configure("2") do |config|
  config.vm.define :nginx do |nginx|
    nginx.vm.box = "ubuntu/jammy64"
    nginx.vm.network "public_network", bridge: "eno1" , ip: "192.168.13.230"
    nginx.vm.network "private_network", ip: "192.168.102.10"
    nginx.vm.hostname = "nginx16"
    nginx.vm.provider :virtualbox do |nginx|
      nginx.name = "nginx16"
      nginx.check_guest_additions = false
      nginx.memory = 2048
      nginx.cpus = 2
    end
  end
  # config.vm.define "docker"  do |vm|
  #   vm.vm.provider "docker" do |d|
  #     d.image = "ubuntu"
  #     d.name = "nginx-container"
  #     d.has_ssh = true
  #     d.cmd = ["tail", "-f", "/dev/null"]
  # vm.vm.network "forwarded_port", guest: 80, host: 82    
  #   end

config.vm.synced_folder ".", "/vagrant", disabled: true
  
end
