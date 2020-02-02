# https://github.com/mesosphere/aws-cli/blob/master/Dockerfile


FROM alpine:3.6

ARG _TAG='1.14.5'
RUN apk -v --update add \
        python \
        py-pip \
        groff \
        less \
        mailcap \
        && \
    pip install --upgrade awscli==${_TAG} s3cmd==2.0.1 python-magic && \
    apk -v --purge del py-pip && \
    rm /var/cache/apk/*
# VOLUME /root/.aws
# VOLUME /project
WORKDIR /home/aws


