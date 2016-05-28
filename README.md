# Docker guide
This is a guide to run our projects through docker. 

**Important**
-This tutorial asumes that you have the dockerfile and docker-compose.yml inside the project folder

## Install docker and docker-compose:

### Installing docker:

[Ubuntu and derivatives](https://docs.docker.com/engine/installation/linux/ubuntulinux/)

[Arch and derivatives](https://docs.docker.com/engine/installation/linux/archlinux/)

### Installing docker-compose

[Unix](https://docs.docker.com/compose/install/)

**Important**
-It is necessary to start the docker daemon as the installation tutorials explain.
-You should add your user to the docker group in order to use it as a normal user (not sudo).

## Download the project main image using the dockefile:

![Creating corottos images](https://raw.githubusercontent.com/kevteg/nokoarts-docker-guide/master/docker/Screenshot_20160527_225326.png)

**This will download all the requeriments for _corottos web app_ . It might take a while**

**Important**
-It is necessary to run this inside the project folder with the **dockerfile** inside

After the image is downloaded you will see it within all the docker images you've download:

![Docker images](https://raw.githubusercontent.com/kevteg/nokoarts-docker-guide/master/docker/Screenshot_20160527_231731.png)

## Use docker compose to pull down the postgres image and make the containers work together!

![Docker compose](https://raw.githubusercontent.com/kevteg/nokoarts-docker-guide/master/docker/Screenshot_20160528_004529.png)

After the postgres image is downloaded you will be able to run the app!

## Creating the database

To run any rails command you just need to use docker-compose run, run as usual:

![Running a command inside the container](https://github.com/kevteg/nokoarts-docker-guide/blob/master/docker/Screenshot_20160528_005842.png?raw=true)

### To considerate

-When adding a new gem to the gemfile just use docker-compose build to run bundle install
-There are some simple changes necessary to make to the database.yml file (attached in the folder)

### Develop and have fun ♥
