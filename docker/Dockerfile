FROM ubuntu:22.04

WORKDIR /app

COPY . ${WORKDIR}

RUN apt update && \
    apt install -y build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev wget && \
    cd /tmp && \
    wget https://www.python.org/ftp/python/3.11.8/Python-3.11.8.tgz && \
    tar -xf Python-3.11.8.tgz && \
    cd Python-3.11.8 && \
    ./configure --enable-optimizations && \
    make install

RUN apt install -y tesseract-ocr libtesseract-dev

