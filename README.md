# RTMP Streaming with Ansible
A quick Saturday project using Vagrant / Ansible to provision an Ubuntu 14.04 server with nginx, RTMP, and a front-end to view the stream from.

## Requirements
* [Ansible](http://docs.ansible.com/intro.html) 
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Usage
* Clone the repository and `cd` to it
* Run `vagrant up`
* Watch the Vagrant and Ansible output fly up your terminal
* Be patient when you hit the last task (Download sample video to host over RTMP)
* If all tasks are successful, run `ifconfig | grep 192` to find out what gateway VirtualBox is forwarding the server through
	* This 
* If all tasks are successful, navigate to http://192.168.50.1:8080/ in your browser
	* Did you remember to append port 8080 to the URL?
	* If the page does not load, run `ifconfig | grep 192` and try navigating to that interface instead	
* Watch the stream
* To remove the VM, run `vagrant -f destroy`

## Notes
* Since this was a one-day project, there are no guarantees that it will work for you. However, if you run into problems, feel free to open an issue and I'd be happy to help you resolve it.
* The nginx role is heavily inspired by [this repo](https://github.com/Hounddog/vagrant-ansible)
* I referenced [this Ansible quickstart tutorial](https://adamcod.es/2014/09/23/vagrant-ansible-quickstart-tutorial.html) to refresh and get started
* The RTMP setup is based on [this tutorial](http://www.leaseweblabs.com/2013/11/streaming-video-demand-nginx-rtmp-module/) that I worked through a few weeks ago
* The front-end uses an Adobe Flash-based plugin called [FlowPlayer](https://flowplayer.org/latest/)
* I purposely included the video download task so that the server is actually streaming the video file locally
	* In the future, I would include the video file in the repository using GitHub's new [LFS system](https://github.com/early_access/large_file_storage). And if I felt like paying money, Amazon S3 would be way more convenient for a project like this
