ARG _TAG='278.0.0-alpine'
FROM google/cloud-sdk:${_TAG}
# https://hub.docker.com/r/google/cloud-sdk/

MAINTAINER iganari

# setting timezone
RUN apk --update add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del tzdata && \
    rm -rf /var/cache/apk/*

# install git
RUN apk --update add git && \
    rm -rfv /var/lib/apt/lists/* && \
    rm -rfv /var/cache/apk/*
