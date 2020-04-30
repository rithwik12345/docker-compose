MY MENTOR
------------
    
    I have learnt this docker technology in IIEC_RISE campaign which was started ny the most renoved world record holder Mr.Vimal Daga to make india future ready.I am very thankful towards his for his campaign.I also learnt redhat linux version 8 (RHEL 8) under his guidance 

AGENDA
-------

    TO CREATE AN INFRASTRUCTURE WHICH HAS A WORDPRESS SERVER AND A SQL DATABASE WHICH ARE INTERLINKED WITH EACH OTHER TO PROVIDE SERVICES. 
    
PRECONFIGURATIONS
-----------------

    1-A system with RHEL installed in it(either baro-metal or virtual).
    2-You must know some basic of linux and docker.
    3-Install docker and docker-compose
    Follow the below steps to download docker-compose file.
        -enter the below code in commad line in linux terminal
        sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o             /usr/local/bin/docker-compose
        -Now we have to give permissions to the file
        sudo chmod +x /usr/local/bin/docker-compose

DOCKER
------
    
    It is a tool which is used in devops in deployment phase,This technology is used to launch an OS quickly.The OS launches by docker functions as the real-time os in which we can create multiple servers and manage them.

DOCKER-COMPOSE
--------------
    
    Docker compose file has infrastructure as code which means that we can launch an entire infrastructure in a single click.Infrastructure is nothing but a set of operating systems working with each other to provide services.

IMAGES REQUIRED
---------------
    For this project we are going to use to images:
    1- wordpress image with pre-configured apache server and php,we can download this image from docker public repository by using the below command
    docker pull wordpress:5.1.1-php7.3-apache
    2-Mysql image as backend database,we can download this image from docker public repository by using the below command
    docker pull mysql:5.7

CREATING A COMPOSE FILE
-----------------------

1:First we need to create a workspace where we are going to create a compose file,workspace is nothing but a folder where we have the files related to a specific task.
2:Create a file with name "docker-compose.yml" we must not change the name of the fle as it is deafault and the managing commands search for the file with the above same name.
3:This file must be typed in yml syntax,We can use the extension either ".yml" or ".yaml".
4:It is recommended that when ever we open the file,use same editor such as vim because the change in editors may result in the white space errors.
5:There is a certain syntax when we type the the code in yml file
6:First we need to specify the version in the top of the file.
7:inside of services keyword we need to specify the name of the os and the components in the os such as the image used by the os,environment variables,ports etc.
8:From the code we can see the exact syntax of the file.


ENVIRONMENT VARIABLES
---------------------
1:It is necessary to declare environment variables at the time of launching operating system,In some cases we cannot create an os without declaring these variables.The example for this type of image is mysql where we cannot run an os without declaring environment variables
2:Some of the examples of environment variables in mysql are-
      # MYSQL_ROOT_PASSWORD
      # MYSQL_USER
      # MYSQL_PASSWORD
      # MYSQL DATABASE


MANAGING A COMPOSE FILE
--------------------------------

1:Start docker services by using the command"systemctl start docker" and to make this command persistent use enable instead of start so hat every time the os boots the docker services start automatically
2:The compose file also downloads images ,creates volumes,adds network etc.
3:The commands regarding the docker-compose are
      # docker-compose up:to execute the docker-compose file.
      # docker-compose stop:to stop the infrastructure.
      # docker-compose start:to start the infrastructure.
      # docker-compose rm:to remove he infrastructure
      These are the commands to maintain infrastruture in docker.
      
RESULT
------

   In a single click we can setup an entire environment of wordpress server with sql database using docker-compose.

THANKS A LOT SIR FOR YOUR TIME AND GUIDANCE
-------------------------------------------
