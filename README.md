ansible-vagrant
===============

Ansible playbooks for use with Vagrant

System requirements
-------------------

	Windows: 
		Vagrant
		Virtualbox
		Cygwin

	Mac: 
		Vagrant
		Virtualbox

Vagrant Ansible Playbooks
-------------------------

- ORI -
	Ori distributed file system from Stanford

ori Usage:

	On your host machine
	$ cd ori

	Start the Vagrant machine
	ori $ vagrant up

	SSH into the Vagrant box
	ori $ vagrant ssh

	In the Vagrant virtual machine

	Create new ori file system
	$ ori newfs test

	Create mount point directory
	$ mkdir test

 	Mount the file system	
	$ orifs test

