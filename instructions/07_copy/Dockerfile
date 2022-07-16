# Example 7 - COPY 
ARG  BASE_IMAGE_VERSION=latest

FROM ubuntu:${BASE_IMAGE_VERSION}

## you can use any commands that are available in base image
RUN apt-get -y update  &&  apt-get -y upgrade && apt-get -y install nginx

# Example 1 of COPY - without chown
COPY index.html /var/www/html/index.nginx-debian.html

# EXAMPLE 2 of COPY - with chown
COPY --chown nginx:nginx index.html /var/www/html/index.nginx-debian.html

# Updated nginx command to run in foreground
CMD ["nginx", "-g", "daemon off;"]