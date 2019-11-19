FROM ubuntu:16.04

MAINTAINER Zafer Durkut, <mailto:durkutzafer@gmail.com>

WORKDIR /app
COPY . /app

RUN apt-get update \
   && apt-get upgrade -y \
   && apt-get install -y \
   build-essential \
   ca-certificates \
   gcc \
   python3-dev \
   python3-pip \   
   gdal-bin \
   python3-gdal \
   libgdal-dev \
   python-gdal \
   libpq-dev \
   libmysqlclient-dev \
   make \
   ssh \
   supervisor \
   git \
   make \
   ssh \
   && apt-get autoremove \
   && apt-get clean
   
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en

RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt
RUN ln -s /usr/bin/python3 /usr/bin/python && ln -s /usr/bin/pip3 /usr/bin/pip
