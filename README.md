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

	Start the Vagrant machines ori1 & ori2
	ori $ vagrant up

	SSH into the Vagrant box ori1
	ori $ vagrant ssh ori1

	In the ori1 Vagrant virtual machine
	-----------------------------------

	Create new ori file system
	ori1$ ori newfs test

	Create mount point directory
	ori1$ mkdir test

 	Mount the file system	
	ori1$ orifs test

	In the ori2 Vagrant virtual machine
        -----------------------------------

	ori2$ ori replicate --shallow vagrant@192.168.111.222:test
	ori2$ mkdir test
	ori2$ orifs test

	
