# Docker guide
This is a guide to run [nokoarts group](http://nokoarts.com/) projects through docker.

> **Δ Important**

> 	  •This tutorial asumes that you have the dockerfile and docker-compose.yml inside the project folder

## Install docker and docker-compose:

### Installing docker:

[Ubuntu and derivatives](https://docs.docker.com/engine/installation/linux/ubuntulinux/)

[Arch and derivatives](https://docs.docker.com/engine/installation/linux/archlinux/)

### Installing docker-compose:

[Unix](https://docs.docker.com/compose/install/)

> **Δ Important**

> 	 •It is necessary to start the [docker daemon](https://docs.docker.com/engine/admin/systemd/) to use docker.

>    •You should add your user to the [docker group](https://docs.docker.com/engine/installation/linux/ubuntulinux/#create-a-docker-group) in order to use it as a normal user (not sudo).


## Download the project main image using the dockefile:
```sh
 $ docker build corottos .  #Dont forget the dot! ;)
```
**This will download all the requeriments for _corottos web app_ . It might take a while**

> **Δ Important**

>     •It is necessary to run this inside the project folder with the **dockerfile** inside

After the image is downloaded you will see it within all the docker images you've download:

![Docker images](https://raw.githubusercontent.com/kevteg/nokoarts-docker-guide/master/images/images.png)

## Docker compose
Docker compose is a tool to run multi-container Docker applications. 

### Pull down the postgres image through docker-compose:!
```sh
$ docker-compose up
```
After the postgres image is downloaded you will be able to run the app!

## Creating the database:

To run any rails command you just need to use docker-compose:
```sh
 $ docker-compose run corottos rake db:create db:migrate
```


> ### ☞ To considerate:

>    •When adding a new gem to the gemfile just use docker-compose build to run bundle install

>    •There are some simple but necessary changes to make to the database.yml file (attached in the folder)

>    •Using **[prax](https://github.com/ysbaddaden/prax)** is exactly the **same thing as usual**

>    •[Docker compose documentation](https://docs.docker.com/compose/)

>    •[Docker documentation](https://docs.docker.com/engine/quickstart/)

## Develop and have fun ♥

To **run** the **app**:

```sh
$ docker-compose up
```
