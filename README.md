Vagrant Node.js App Starter
==========================

A Node.js project starter, utilizing a Vagrant VM (default: Ubuntu 12.04 Precise Pangolin 32-bit) provisioned with Chef Solo.

Cookbooks included:

* [apt](https://github.com/opscode-cookbooks/apt)
* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [nodejs](https://github.com/mdxp/nodejs-cookbook.git)

## Dependencies

You must install the following dependencies:

* [VirtualBox](https://www.virtualbox.org/)
* [Ruby](http://www.ruby-lang.org/en/)
* [Vagrant](http://vagrantup.com/)
    * [Vagrant Omnibus](https://github.com/jimmycuadra/vagrant-librarian-chef)
    * [Vagrant Librarian-Chef](https://github.com/jimmycuadra/vagrant-librarian-chef)

## Usage

Clone it into your project folder.

```bash
$ git clone https://github.com/devert/vagrant-nodejs-app-starter [proj-name]
$ rm -rf .git
```

Open the vagrant/Vagrantfile and modify all *proj-name* instances to the name of your project.

* Modify the Node.js version you would like installed in the *chef.json* attributes.
* Modify the Chef version you would like installed with the *config.omnibus.chef_version* attribute.

```bash
$ vagrant plugun install vagrant-omnibus
$ vagrant plugin install vagrant-librarian-chef
$ cd vagrant
$ vagrant up
$ vagrant ssh
$ node proj-name/app.js
```

After running the above commands you should be able to browse to http://locahost:3000/ and see "Hello World!" on your host machine. Changes to files via the host machine will immediately be updated on the guest VM as well. You'll just have to remember to start and stop the node server. Or you can install a daemon tool like [Forever](https://github.com/nodejitsu/forever) to watch for updates to your application files (details below).

Now get in there and build something awesometronic with Node.js!

## Optional (But Pretty Great)

#### Node.js
* Keep the Node.js web server running and restart on file changes with [Forever](https://github.com/nodejitsu/forever). Install this in the Vagrant VM.

    ```bash
    $ npm install forever -g
    $ forever -w proj-name/app.js
    ```
