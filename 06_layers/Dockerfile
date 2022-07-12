# Example 6
# image is not useful as port is not exposed
ARG  BASE_IMAGE_VERSION=latest

FROM ubuntu:${BASE_IMAGE_VERSION}

## you can use any commands that are available in base image
RUN apt-get -y update  &&  apt-get -y upgrade && apt-get -y install nginx

# Updated nginx command to run in foreground
CMD ["nginx", "-g", "daemon off;"]