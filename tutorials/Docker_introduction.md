#### Using Docker

We have been using the bash shell in macOS to learn some basic command-line vocabulary. All operating systems are different but we want everyone to use the same kind so we will use Docker. Docker is an application that makes it possible to run a virtual copy of the Linux operating system within your primary OS. We will be using Ubuntu, a version of Linux that is often used to run web servers. Ordinarily, you would launch an Ubuntu server and then install the programs you need, one by one; Docker lets us speed up that process by defining our system's initial configuration in a plain text file, known as a Dockerfile. You can view [the Dockerfile we are currently using](https://hub.docker.com/r/pcda17/ubuntu-container/~/dockerfile/).

For more details on how Docker works, [see this overview](https://docs.docker.com/engine/docker-overview/).

### Getting started on the iSchool Macs (in the classroom and in the lab):

1. Open a new terminal window.

2. Enter the following command in the terminal window to download the Docker image files we'll be using. This could take several minutes.

```
docker pull pcda17/ubuntu-container
```

3. When the download is complete, enter the following command to run the container. This will create a new directory called `sharedfolder` on your desktop.

```
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container bash
```

The command above includes several options:
- The `--name` flag sets the name of our container as `pcda_ubuntu`, while `-ti` tells Docker that we want to use an interactive terminal.
- `-p` maps port 8889 in our container to port 8889 in our local OS (more on this later).
- The `--volume` option defines a "shared volume" between the container and our local machine, a directory called `sharedfolder`.
- `pcda17/ubuntu-container` identifies the image we want to download, which is hosted on the Docker Hub website.
- Finally, `bash` specifies that we want to enter the bash shell.

You should now be in an interactive bash session in your new Ubuntu container. To make sure, type the following command and press enter to see your username. The response should be `root`.

```
whoami
```

Now enter the command `pwd` to print the current working directory. You should be in `/sharedfolder/`.

```
pwd
```

Create a new text file, just like we did earlier in the macOS shell.

```
echo "Hello!" > sample_file.txt
```

Open the `sharedfolder` directory on your desktop, and you should see the file we just created, `sample_file.txt`. The `sharedfolder` directory is like a portal between Ubuntu and your primary OS; both can read and write files located there, and any changes you make will instantly be visible in both operating systems.

### Getting started on your own computer using Docker
1. On your own computer, you'll have to download Docker:

- [Install Docker for macOS](https://docs.docker.com/docker-for-mac/install/#install-and-run-docker-for-mac)
- [Install Docker for Windows 10](https://pcda17.github.io/tutorials/Docker_install_Windows)
- [Install Docker Toolbox for Windows 7 or 8](https://docs.docker.com/toolbox/toolbox_install_windows/)


2. Launch the Docker container
In macOS, open Terminal and enter the following commands to remove any current running containers and to launch a new one:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume ~/Desktop/sharedfolder/:/sharedfolder/ pcda17/ubuntu-container
```

In Windows 10, open PowerShell and enter the following commands to launch the Docker container:

```
docker rm -f pcda_ubuntu
docker pull pcda17/ubuntu-container
docker run --name pcda_ubuntu -ti -p 8889:8889 --volume C:\Users\***username_here***\Desktop\sharedfolder:/sharedfolder/ pcda17/ubuntu-container
```

Open any browser and type (your Juypter Notebook will launch):
```
localhost:8889

```
#### Closing Docker

To leave a Docker interactive terminal session and return to your main operating system's shell, press `ctrl + p` followed by `ctrl + q`.

To view all current Docker containers, enter the following command:

```
docker ps -a
```

To close and remove a container, use `docker rm -f` followed by its name, like so:

```
docker rm -f pcda_ubuntu
```

To close and remove all current Docker containers, enter the following command:

```
docker rm $(docker ps -aq)
```
