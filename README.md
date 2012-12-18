# Vagrant Node.js App Starter

---
A Node.js project starter, utilizing a Vagrant VM (default: Ubuntu Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [apt](https://github.com/opscode-cookbooks/apt)
* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [nodejs](https://github.com/mdxp/nodejs-cookbook.git)
* [vim](https://github.com/opscode-cookbooks/vim)

## Requirements

* [VirtualBox](https://www.virtualbox.org/)
* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
* [Librarian](https://github.com/applicationsonline/librarian)

## Usage

Clone it into your project folder, install cookbook dependencies with Librarian-Chef, launch/create Vagrant VM, run Node.js web server.

    $ git clone https://github.com/devert/vagrant-nodejs-app-starter [proj-name]
    $ rm -rf .git
    $ cd vagrant
    $ librarian-chef install
    $ vagrant up
    $ vagrant ssh
    $ node proj-name/app.js

After running the above commands you should be able to browse to http://127.0.0.1:8080 and see "Hello World!"

## Optional

#### Node.js
* Keep the Node.js web server running and restart on file changes with [Forever](https://github.com/nodejitsu/forever)

    	$ npm install forever -g
		$ forever -w proj-name/app.js

#### Vagrant
* Keep Vagrant VM's VirtualBox Guest Additions up to date with [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin.
		
		$ vagrant gem install vagrant-vbguest

* Setup a custom host name for Vagrant VM and host OS with [vagrant-hostmaster](https://github.com/mosaicxm/vagrant-hostmaster.git)
	
		$ vagrant gem install vagrant-hostmaster

	```ruby
	# Uncomment the following in Vagrantfile
	config.hosts.name = "proj-name.local"
	config.vm.network :hostonly, "192.168.33.10"
	```

