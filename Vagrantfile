
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  
	#Configura VM Ubuntu Bionic e provisiona o Docker
    config.vm.define "dockerhost" do |dockerhost|
        dockerhost.vm.provider "virtualbox" do |vb|
            vb.memory = 512
            vb.cpus = 1
            vb.name = "ubuntu_dockerhost"
        end

        dockerhost.vm.provision "shell", 
            inline: "apt-get update && apt-get install -y docker.io"
		end
	
end
