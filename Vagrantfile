# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.define :nodejsvm do |nodejs_config|
    nodejs_config.vm.box = "lucid32"
    nodejs_config.vm.provision :chef_solo do |chef|
      chef.cookbooks_path = "cookbooks"
      chef.add_recipe "build-essential"
      chef.add_recipe "nodejs"
      chef.add_recipe "vim"
    end
  end
end