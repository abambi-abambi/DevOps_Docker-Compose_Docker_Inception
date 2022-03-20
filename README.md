# Inception

Inception

This project sets up a small infrastructure composed of different services

This is set up:

• A Docker container that contains NGINX with TLSv1.2 or TLSv1.3 only.
• A Docker container that contains WordPress + php-fpm (it must be installed and
configured) only without nginx.
• A Docker container that contains MariaDB only without nginx.

• A volume that contains your WordPress database.
• A second volume that contains your WordPress website files.

• A docker-network that establishes the connection between your containers.

Containers have to restart in case of a crash.

Makefile calles docker-compose.yml which calles the Dockerfiles:

make

(and there are other commands: make all, make clean, make fclean, make re, make state, make stop)
