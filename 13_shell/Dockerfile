# Example 13 - Changing the default shell

# ARGUMENTS can be changed during the buildtime 
ARG  BASE_IMAGE_VERSION=20.04

FROM ubuntu:${BASE_IMAGE_VERSION}

## you can use any commands that are available in base image
RUN apt-get -y update  && apt-get -y install zsh


SHELL ["/bin/sh", "echo" , "$0"]

SHELL ["/bin/bash", "echo" , "$0"]

SHELL ["/bin/zsh", "echo" , "$0"]

CMD  ["/bin/zsh", "echo" , "$0"]