FROM ubuntu:22.04

WORKDIR /home/ubuntu

RUN apt-get update && apt-get -y install scons doxygen graphviz python3-pip
ADD requirements.unversioned.txt /home/ubuntu
RUN pip3 install -U -r requirements.unversioned.txt
