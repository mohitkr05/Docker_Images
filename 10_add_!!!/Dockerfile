# Example 10 - 

# ARGUMENTS can be changed during the buildtime 
ARG  BASE_IMAGE_VERSION=latest

FROM ubuntu:${BASE_IMAGE_VERSION}

# Environments cannot be changed - used inside the containers
ENV APPLICATION nginx

## you can use any commands that are available in base image
RUN apt-get -y update  && apt-get -y install nginx

# ADD is similar to copy
ADD ../index.html /var/www/html/index.nginx-debian.html

# However it can get files from Remote URL which COPY cannot

ADD 

# It can also extract TAR/ZIP files 

# EXPOSE TO The port numbers can be TCP/UDP
# EXPOSE 123/UDP (EXAMPLE FOR NTP Application)

EXPOSE 80/TCP

# You can expose it to multiple ports
EXPOSE 8080/TCP


# Updated nginx command to run in foreground
CMD ["nginx", "-g", "daemon off;"]