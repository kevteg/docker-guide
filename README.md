# Docker guide
This is a guide to run our projects through docker.

## Install docker and docker-compose:

### Installing docker:

[Ubuntu and derivatives](https://docs.docker.com/engine/installation/linux/ubuntulinux/)

[Arch and derivatives](https://docs.docker.com/engine/installation/linux/archlinux/)

### Installing docker-compose

[Unix](https://docs.docker.com/compose/install/)

**Important**
-It is necessary to start the docker daemon as the installation tutorials explain.
-You should add your user to the docker group in order to use it as a normal user (not sudo).

## Download the project main image through the dockefile:

![Creating corottos images](https://raw.githubusercontent.com/kevteg/nokoarts-docker-guide/master/docker/Screenshot_20160527_225326.png)

**This willis download all the requeriments for _corottos web app_ . It might take a while**repository
**Important**
-It is necessary to run this inside the project file with the **dockerfile**files insideand

Afterinstructions theto imageset is downloaded you should see it in the dockerenvironment images:for (run: docker images)

![Docker images](https://raw.githubusercontent.com/kevteg/nokoarts-docker-guide/master/docker/Screenshot_20160527_231731.png)





