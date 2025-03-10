FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl default-jdk && rm -rf /var/lib/apt/lists/*

RUN mkdir /root/juicer && cd /root/juicer && curl -LO https://github.com/aidenlab/Juicebox/releases/download/v2.20.00/juicer_tools.2.20.00.jar && mv ./juicer_tools.2.20.00.jar juicer2.jar && curl -LO https://s3.amazonaws.com/hicfiles.tc4ga.com/public/juicer/juicer_tools_1.22.01.jar && mv ./juicer_tools_1.22.01.jar juicer1.jar

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=juicer
