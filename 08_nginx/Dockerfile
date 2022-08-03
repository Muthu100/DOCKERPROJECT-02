FROM ubuntu:latest
# apt get update & install nginx

RUN apt-get -y update && apt-get -y install nginx
#ADD USER nginx & group nginx

RUN useradd -ms /bin/bash nginx
#/var/www/html

# chown - change ownership - by default using root user
ADD --chown=nginx:nginx index.html /var/www/html/index.nginx-debian.html

#which port going to te be expose
EXPOSE 80/tcp
EXPOSE 443/tcp

#Start the nginx webserver
CMD ["nginx", "-g", "daemon off;"]
