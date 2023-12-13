FROM alpine:latest
RUN apk add --no-cache bash \
    && apk add openssh \
    && adduser -D -u 10001 oladipo 
ENTRYPOINT ssh-keygen -t rsa -N "" -f ~/.ssh/id_rsa && tail -f /dev/null
