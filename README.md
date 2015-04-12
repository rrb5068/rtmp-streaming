# RTMP Streaming with Ansible
A quick project using Vagrant / Ansible to provision an Ubuntu 14.04 server with nginx, RTMP, and a frontend to view the stream from.


## Requirements
* [Ansible](http://docs.ansible.com/intro.html) 
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


## Notes 
* The nginx role is heavily inspired by [this repo](https://github.com/Hounddog/vagrant-ansible)
* I referenced [this Ansible quickstart tutorial](https://adamcod.es/2014/09/23/vagrant-ansible-quickstart-tutorial.html) to refresh and get started
* The RTMP setup is based on [this tutorial](http://www.leaseweblabs.com/2013/11/streaming-video-demand-nginx-rtmp-module/) that I worked through a few weeks ago
