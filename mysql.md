#MySQL


##boot2docker

Because the Docker Engine uses Linux-specific kernel features, you'll need to use a lightweight virtual machine (VM) to run it on OS X. You use the OS X Docker client to control the virtualized Docker Engine to build, run, and manage Docker containers.

To make this process easier, we've built a helper application called Boot2Docker that installs a virtual machine (using VirtualBox) that's all set up to run the Docker daemon.


#### Creating root account

[code]mysqladmin -u root password 'root password goes here'[/code]
[code]mysql -h localhost -u root -p[/code]