FROM ubuntu:latest as builder

#Download unzip
RUN apt-get -y update && apt-get install -y unzip
# download the wordpress

#specify my working directory
WORKDIR /app

#download from internet - 5mb
ADD https://wordpress.org/latest.zip .

#unzip the zip file
RUN unzip -o latest.zip

#image 2
FROM nginx:latest

#copy the extracted file from builder image into the nginx path
COPY --from=builder /app/ /usr/share/nginx/html

EXPOSE 80

CMD ["nginx", "-g", "deamon off;"]
