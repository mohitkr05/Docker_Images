# Example 16 - Adding label to the image

# ARGUMENTS can be changed during the buildtime 
ARG  BASE_IMAGE_VERSION=20.04

FROM ubuntu:${BASE_IMAGE_VERSION}

# Environments cannot be changed - used inside the containers
ENV APPLICATION nginx


LABEL "application"="nginx"
LABEL "version"="latest"
LABEL "operating_system"="ubuntu:20.04"

LABEL "label1"="helloworld" "label2"="hello" "label3"="world"


## you can use any commands that are available in base image
RUN apt-get -y update  && apt-get -y install nginx unzip curl


WORKDIR /var/www/html

# However it can get files from Remote URL which COPY cannot
# It can also extract TAR/ZIP files 
# You can also add chown instructions with add 
ADD https://wordpress.org/latest.zip .

# where this file will be extracted?
RUN unzip -o latest.zip 



# EXPOSE TO The port numbers can be TCP/UDP
# EXPOSE 123/UDP (EXAMPLE FOR NTP Application)

EXPOSE 80/TCP

# You can expose it to multiple ports
EXPOSE 8080/TCP


# Updated nginx command to run in foreground
CMD ["nginx", "-g", "daemon off;"]