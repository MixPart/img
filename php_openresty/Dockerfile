FROM /centos:6

LABEL maintainer="synics@126.com"

COPY ./script /build

RUN sh /build/prepare.sh && \
    sh /build/services.sh && \
    sh /build/extensions.sh

ADD src/s6-overlay-amd64.tar.gz /

COPY ./root /

EXPOSE 80

ENTRYPOINT ["/init"]
