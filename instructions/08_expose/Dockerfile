# Example 8 - Expose 

ARG  BASE_IMAGE_VERSION=latest

FROM ubuntu:${BASE_IMAGE_VERSION}

## you can use any commands that are available in base image
RUN apt-get -y update  &&  apt-get -y upgrade && apt-get -y install nginx

COPY index.html /var/www/html/index.nginx-debian.html

# EXPOSE TO The port numbers can be TCP/UDP
# EXPOSE 123/UDP (EXAMPLE FOR NTP Application)

EXPOSE 80/TCP

# You can expose it to multiple ports
EXPOSE 8080/TCP


# Updated nginx command to run in foreground
CMD ["nginx", "-g", "daemon off;"]