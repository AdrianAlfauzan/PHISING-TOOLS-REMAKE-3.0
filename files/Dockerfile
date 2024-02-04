# Dockerfile

# Author       : AdrianAlfauzan
# Github       : https://github.com/AdrianAlfauzan/
# Email        : stalkerxstalk@gmail.com
# Date         : 2024-02-03
# Main Language: Python

# Download and import main images

# Operating system
FROM debian:latest
# Main package
FROM python:3

# Author info
LABEL MAINTAINER="https://github.com/AdrianAlfauzan/"

# Working directory
WORKDIR /PyPhisher/
# Add files 
ADD . /PyPhisher

# Installing other packages
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install python3-pip php openssh-client -y
RUN pip3 install -r files/requirements.txt --break-system-packages
RUN apt-get clean

# Main command
CMD ["python3", "pyphisher.py", "--noupdate"]

## Wanna run it own? Try following commnads:

## "sudo docker build . -t stalker/pyphisher:latest", "sudo docker run --rm -it stalker/pyphisher:latest"

## "sudo docker pull stalker/pyphisher", "sudo docker run --rm -it stalker/pyphisher"
