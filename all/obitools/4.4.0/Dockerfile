FROM ubuntu:24.04

RUN apt update && \
	apt upgrade -y && \
	apt install -y build-essential wget unzip curl zlib1g libglib2.0-0 zlib1g-dev && \
	apt clean

WORKDIR /usr/src/obitools

RUN wget https://github.com/metabarcoding/obitools4/archive/refs/tags/Release_4.4.0.tar.gz && \
	tar xvfz Release_4.4.0.tar.gz && \
	cd obitools4-Release_4.4.0 && \
	bash ./install_obitools.sh --install-dir . 

ENV PATH=${PATH}:/usr/src/obitools/obitools4-Release_4.4.0/bin
