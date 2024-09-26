FROM ubuntu:22.04

RUN apt update && \
	apt upgrade -y && \
	apt install -y build-essential wget python3 pip && \
	apt clean

WORKDIR /usr/src/radinitio

RUN wget https://catchenlab.life.illinois.edu/radinitio/source/radinitio-1.2.3.tar.gz && \
	python3 -m pip install radinitio-1.2.3.tar.gz && \
	rm radinitio-1.2.3.tar.gz


