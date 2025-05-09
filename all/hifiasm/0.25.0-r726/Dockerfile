FROM ubuntu:24.04

RUN apt update && \
	apt upgrade -y && \
	apt install -y build-essential wget make git zlib1g zlib1g-dev && \
	apt clean

WORKDIR /usr/src

RUN git clone https://github.com/chhylp123/hifiasm.git --branch 0.25.0 && \
	cd hifiasm && \
	make
ENV PATH=${PATH}:/usr/src/hifiasm


#ec9a8b222d149d25b7355e83765698640d59b189
