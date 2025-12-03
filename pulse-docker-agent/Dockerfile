ARG BUILD_FROM=alpine:3.20
FROM ${BUILD_FROM}

RUN apk add --no-cache \
    curl \
    tar \
    ca-certificates

COPY run.sh /run.sh
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]

