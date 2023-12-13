FROM alpine:latest
RUN apk add --no-cache bash \
    && apk add ansible \
    && apk add openssh \
    && adduser -D -u 10001 oladipo
WORKDIR /home/oladipo/.ssh
ENTRYPOINT chown -R oladipo:oladipo /home/oladipo/.ssh && && tail -f /dev/null
