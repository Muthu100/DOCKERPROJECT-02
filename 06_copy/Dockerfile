# base image
FROM ubuntu:latest

RUN apt-get -y update && apt-get -y install nginx 

COPY index.html /var/www/html/index.nginx-debian.html

EXPOSE 80

EXPOSE 443/tcp

CMD ["nginx", "-g", "daemon off;"]