FROM python:3

WORKDIR /root

RUN apt-get update -y && apt-get install -y libleveldb-dev && \
    pip3 install plyvel && \
    git clone https://github.com/spesmilo/electrumx.git && \
    cd electrumx && \
    pip3 install . && \
    mkdir db_directory

WORKDIR /root/electrumx
