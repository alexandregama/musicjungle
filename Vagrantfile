Vagrant.configure("2") do |config|

	# ubuntu machine
	config.vm.box = "hashicorp/precise32"

	# web virtual machine
	config.vm.define :web do |web_config|
		web_config.vm.network :private_network, :ip => "192.168.50.10" 
	end
end