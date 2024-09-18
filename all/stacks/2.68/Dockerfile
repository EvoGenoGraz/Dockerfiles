FROM ubuntu:24.04

RUN apt update && \
	apt upgrade -y && \
	apt install -y build-essential wget zlib1g zlib1g-dev && \
	apt clean

WORKDIR /usr/src

RUN wget https://catchenlab.life.illinois.edu/stacks/source/stacks-2.68.tar.gz && \
	tar xfz stacks-2.68.tar.gz && \
	rm stacks-2.68.tar.gz && \
	cd stacks-2.68 && \
	./configure && \
	make && \
	make install && \
	make clean
