FROM ubuntu:18.04

WORKDIR /app

RUN apt update \
 && apt install -y curl software-properties-common ansible \
 && apt-add-repository --yes --update ppa:ansible/ansible \
 && apt install -y ansible \
 && apt-get clean \
 && curl -L https://github.com/Switcheo/tradehub/releases/download/v1.5.0/switcheocli-linux-x64.tar.gz | tar -xz \
 && mv switcheocli /usr/bin/ \
 && switcheocli config node tcp://34.105.77.167:26657 \
 && switcheocli config chain-id switcheo-tradehub-1
