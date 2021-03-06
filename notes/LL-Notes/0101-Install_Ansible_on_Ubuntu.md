# ANSIBLE on UBUNTU:
---

- Step 1 : Install
	- Here we'll use the ppa:ansible/ansible repository as it is easy to remember.

	```
	# apt-get-repository -y ppa:ansible/ansible
	# apt-get update
	# apt-get install -y ansible
	```

- Step 2 : Managing Servers
	- Ansible has a default inventory file used to define which servers it will be managing. 
	- After installation, there's an example one you can reference at /etc/ansible/hosts.
	- I usually copy and move the default one so I can reference it later:

	```
	# mv /etc/ansible/hosts /etc/ansible/hosts.orig
	```

	- Then I create my own inventory file from scratch. 
	- After moving the example inventory file, create a new /etc/ansible/hosts file, and define some servers to manage. 
	- Here's we'll define two servers under the "web" label:

	```
	[web]
	192.168.1.50
	192.168.1.51
	```

	- For testing this article, I created a virtual machine, installed Ansible, and then ran Ansible Tasks directly on that server. 
	- To do this, my hosts inventory file simply looked like this:

	```
	[local]
	127.0.0.1
	```

- Step 3 : Setup your SSH keys
	- Follow the link to setup your SSH keys

	```
	https://github.com/vmsnivas/ssh-keys/blob/master/01.%20Configuring%20SSH%20keys.txt
	```
