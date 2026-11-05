# The line bellow states we will base our new image on the latest official Ubuntu
FROM ubuntu:latest

#
#Identify the maintainer of an image
LABEL maintainer="rahuldastidar@yandex.com"
#
#Update the image to the latest packages
RUN apt update && apt upgrade -y

#
#Install NGINX to test
RUN apt install nginx -y
#
#Clean the apt cache
RUN apt clean && rm -rf /var/lib/apt/lists/*
#
# Expose port 80
EXPOSE 80

#
# Last in the actual command to start up NGINX within our Container
CMD ["nginx", "-g", "daemon off;"]
