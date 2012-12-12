# Vagrant Node.js App Starter

## Intro

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

### Optional
* Keep Vagrant VM's VirtualBox Guest Additions up to date with [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) plugin.

## Usage

Clone it into your project folder, install cookbook dependencies with Librarian-Chef, launch/create Vagrant VM, run node web server.

    $ git clone https://github.com/devert/vagrant-nodejs-app-starter project-name
    $ rm -rf .git
    $ cd vagrant
    $ librarian-chef install
    $ vagrant up
    $ vagrant ssh
    $ cd project-name
    $ node server.js

After running the above commands you should be able to browse to http://127.0.0.1:8080 and see "Hello World!"
