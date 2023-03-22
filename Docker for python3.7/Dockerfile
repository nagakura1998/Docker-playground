FROM ubuntu:18.04

# Set temp work directory
# for package configuration
WORKDIR /usr/src/cache

# Update apt packages
RUN apt update
RUN apt upgrade -y

# Install vim
RUN apt install vim -y

# Install python 3.7
RUN apt install software-properties-common -y
RUN add-apt-repository ppa:deadsnakes/ppa
RUN apt install python3.7 -y

# Add 3.7 to the available alternatives
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3.7 1

# Set python3.7 as the default python
RUN update-alternatives --set python /usr/bin/python3.7

# Install pip
RUN apt install python3-pip -y
RUN python -m pip install --upgrade pip

COPY . .
RUN pip install -r requirements.txt
# Set working directory for code
WORKDIR /usr/src/app