FROM debian:stable-slim
USER root
RUN apt-get update -y \
    && apt-get install -y openssh-server sudo ufw
RUN useradd oladipo -u 10001 -m
WORKDIR /home/oladipo/.ssh
RUN touch authorized_keys
ENTRYPOINT  \
    ufw allow 22 \
    && service ssh start \
    && chown -R oladipo:oladipo /home/oladipo/.ssh \
    && tail -f /dev/null
EXPOSE 22
