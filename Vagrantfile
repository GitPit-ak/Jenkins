Vagrant.configure("2") do |config|

    config.vm.define "jenkins" do |jenkins|
      jenkins.vm.box = "generic/ubuntu2204"
      jenkins.vm.hostname = "jenkins"
      jenkins.vm.network "public_network", ip: "192.168.1.56"
    #   jenkins.vm.provision  "shell", path: "./scripts/motd.sh"
      jenkins.vm.provider "virtualbox" do |vb|
        vb.name = "jenkins"
        vb.memory = 4100
        vb.cpus = 3
        end
    end
  
  
    # config.vm.define "nginx" do |nginx|
    #     nginx.vm.box = "generic/ubuntu2204"
    #     nginx.vm.network "public_network", ip: "192.168.1.55"
    #     nginx.vm.synced_folder ".", "/vagrant"
    #     nginx.vm.hostname = "nginx"
    #     nginx.vm.provision  "shell", path: "./scripts/motd.sh"
    #     nginx.vm.provision  "shell", path: "./scripts/ssh.sh"
    #     nginx.vm.provision "shell", inline: <<-'SCRIPT'
    #     sudo apt update
    #     sudo apt install software-properties-common -y
    #     sudo add-apt-repository --yes --update ppa:ansible/ansible
    #     sudo apt install ansible -y
    #     SCRIPT
    #     nginx.vm.provider "virtualbox" do |vb|
    #       vb.name = "nginx"
    #       end 
    #     # nginx.vm.synced_folder ".", "/ansible",
    # end
  
  
  end