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

    git clone https://github.com/devert/vagrant-chef-nodejs-box my-project
    cd my-project
    librarian-chef install
    vagrant up