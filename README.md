# Inception

Inception

Read the subject_en.pdf and the checklist.pdf. They describe all the project.


But briefly:
This project sets up a small infrastructure composed of different services

This is done:

• A Docker container that contains NGINX with TLSv1.2 or TLSv1.3 only.
• A Docker container that contains WordPress + php-fpm (it must be installed and
configured) only without nginx.
• A Docker container that contains MariaDB only without nginx.

• A volume that contains your WordPress database.
• A second volume that contains your WordPress website files.

• A docker-network that establishes the connection between your containers.

Containers have to restart in case of a crash.

Makefile calles docker-compose.yml which calles the Dockerfiles:

To start the work, go into the folder with the Makefile, open the terminal and type:
make

(and there are other commands: make all, make clean, make fclean, make re, make state, make stop)

You can find a new site at the address:
https://abambi.42.fr

!!! Don't forget to set in your hosts-file the association between "abambi.42.fr" and "localhost" 
(because you will connect to localhost, telling another name)
