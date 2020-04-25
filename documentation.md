DOCKER
------
    
    It is a tool which is used in devops in deployment phase,This technology is used to launch an OS quickly.The OS launches by docker functions as the real-time os in which we can create multiple servers and manage them.

DOCKER-COMPOSE
--------------
    
    Docker compose file has infrastructure as code which means that we can launch an entire infrastructure in a single click.Infrastructure is nothing but a set of operating systems working with each other to provide services.


AGENDA
-------

 TO CREATE AN INFRASTRUCTURE WHICH HAS A SERVER AND A DATABASE WHICH ARE INTERLINKED WITH EACH OTHER TO PROVIDE SERVICES. 
    
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

