#Docker


##boot2docker

Because the Docker Engine uses Linux-specific kernel features, you'll need to use a lightweight virtual machine (VM) to run it on OS X. You use the OS X Docker client to control the virtualized Docker Engine to build, run, and manage Docker containers.

To make this process easier, we've built a helper application called Boot2Docker that installs a virtual machine (using VirtualBox) that's all set up to run the Docker daemon.


#### First install

1. Download Boot2Docker [here](https://github.com/boot2docker/osx-installer/releases/tag/v1.5.0).
2. <code>boot2docker init</code> - This downloads the boot2docker ISO image.
3. <code>boot2docker start</code> - This starts the Virtual Machine and sets the environment variables. 

#### Upgrading Docker

1. Download the latest version of Boot2Docker [here](https://github.com/boot2docker/osx-installer/releases/tag/v1.5.0).
2. Stop Boot2Docker with <code>boot2docker stop</code> (if it's running).
3. Run the installer package. Now <code>Docker</code> and the <code>Boot2Docker management tool</code> is updated.
4. The existing virtual machine has to get updated aswell. This can be done by running <code>boot2docker stop</code>, <code>boot2docker download</code>, <code>boot2docker start</code>

***


### Docker Hub Registry

The easiest way to get started is to use a container image from someone else. Container images are available on the Docker Hub Registry, a cloud-based collection of applications. You can find them online at Docker Hub as well through the Docker Engine client command line.


1. Use <code>docker search (string)</code> to search for images.
2. Use <code>docker pull</code> to download images. The names used on the Docker Hub Registry are constructed as <code>(username)/(repository)</code>, for example <code>alserda/sweetapi</code>


### Running a Docker image

You can run commands through a container. Actually 'starting' a container, means you run processes on them.

An example of running a command through a container is <code>docker run 'image-name' 'command'</code> such as <code>docker run alserda/sweetapi echo 'hello world'</code>

This started the container and executed the command. When the command stopped, so did the container.

### Making changes


It's possible to install utilities within a container by using the same command, for example <code>docker run alserda/sweetapi apt-get install -y ping</code>. Changes to the filesystem have been kept, but are not yet saved.


### Comitting (saving) changes

You can commit the changes by using <code>docker commit (id) (name)</code>

This saves difference between the old image and the new state. Docker returns back an <code>image ID</code>, which is different from the ID used to commit.


### Pushing images

<code>docker push (username)/(respository)</code> pushes the image to the Registry.


### Listing images

<code>docker images</code> returns all created images, along with all information.

<code>docker ps -l</code> returns a list of all created containers with its information.

<code>docker ps</code> returns a list of al running containers.

<code>docker inspect (image ID)</code> lists information about a running container.



### Other information

- boot2docker's default user is <code>docker</code> with the password <code>tcuser</code>