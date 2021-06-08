# DevEnvironment


## STEPS TO INIT VAGRANT

-create new folder(mkdir "folder_name")
-create new file called Vagrantfile(touch Vagrantfile)
-enter Vagrantfile using `nano Vagrantfile`
-inside that file paste 

`Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.100"
end`

-save that file
-open git bash as admin
-type `vagrant up`
-to make sure everything is running properly you can type `vagrant status`
-if everything is running fine type `vagrant ssh` to enter console for your virtual machine
-type `sudo apt-get update -y` to update your VM
-type `sudo apt-get install nginx -y` to install nginx
-open anybrowser of your own choice and type `192.168.10.100`(you shoud see welcome page for nginx)
-to destroy VM type `vagrant destroy`
