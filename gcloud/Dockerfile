ARG _TAG='278.0.0-alpine'
FROM google/cloud-sdk:${_TAG}
# https://hub.docker.com/r/google/cloud-sdk/

RUN gcloud --quiet components update && \
    gcloud --quiet components install beta

# setting timezone
RUN apk --update add tzdata && \
    cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
    apk del tzdata && \
    rm -rf /var/cache/apk/*

# install git
RUN apk --update add git && \
    rm -rfv /var/lib/apt/lists/* && \
    rm -rfv /var/cache/apk/*

WORKDIR /home/gcloud
