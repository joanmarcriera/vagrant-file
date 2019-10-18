# vagrant-file


This Vagrant file has been created using [[ centos7 | ``https://app.vagrantup.com/centos/boxes/7``]] as template .


1) You will need virtualbox installed on your computer.
2) Clone this repository on your computer
3) Run ` vagrant up` .


Port 8080 of your machine will provide access to port 80 no Vagrant running installation, if that port is already used on your machine feel free to use any other port but changing the Vagrant file and running `vagrant destroy`. 


# How to test if the environment is configured correctly.

After `vagrant up` you should be able to `vagrant ssh` 

```bash

✔ ~/my_repos/vagrant-file [master|✚ 1…11]
12:36 $ vagrant ssh
[vagrant@localhost ~]$ sudo su -
Last login: DATE REDACTED
```

You can now ensure docker is installed correctly by running the hello-world example.

```bash
[root@localhost ~]# docker run hello-world
Unable to find image 'hello-world:latest' locally
Trying to pull repository docker.io/library/hello-world ...
latest: Pulling from docker.io/library/hello-world
1b930d010525: Pull complete
Digest: sha256:c3b4ada4687bbaa170745b3e4dd8ac3f194ca95b2d0518b417fb47e5879d9b5f
Status: Downloaded newer image for docker.io/hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

[root@localhost ~]#
`

# Your code will be tested from here by cloning the repository and using docker to build its container.

From here onwards we will follow your instructions provided on your README file.

As an example we are looking for something like this as deliverable.
`bash
$ git clone https://github.com/docker/labs
$ cd labs/beginner/flask-app/
$ [root@localhost flask-app]# docker build -t super_api .
$ [root@localhost flask-app]# docker run -p 80:5000 --name myapp super_api
`

And my super_api runs on port 5000 as a docker container, providing access to the Vagrant system on port 80, and Vagrant is providing access to such port to our external OS on port 8080. We will test your solution from that point onwards following your instructions. 


