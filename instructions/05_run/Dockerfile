# Example 5
ARG  BASE_IMAGE_VERSION=latest

FROM ubuntu:${BASE_IMAGE_VERSION}

## you can use any commands that are available in base image
RUN apt-get -y update 

RUN apt-get -y upgrade

CMD ["/bin/echo", "This image is updated"]