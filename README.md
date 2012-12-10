Intro
======

A Vagrant Node.js box starter, provisioned with Chef Solo.

Other recipes included:

* apt
* build-essential
* vim

Usage
======

Clone it, install dependencies with Librarian-Chef and launch Vagrant:

    git clone --recursive git://github.com/devert/vagrant-chef-nodejs-box
    cd my-project
    librarian-chef install
    vagrant up