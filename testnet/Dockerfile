FROM ubuntu:18.04

WORKDIR /app

RUN apt update \
 && apt install -y curl software-properties-common ansible \
 && apt-add-repository --yes --update ppa:ansible/ansible \
 && apt install -y ansible nano \
 && apt-get clean \
 && curl -L https://github.com/Switcheo/tradehub/releases/download/v1.8.6/install-testnet.tar.gz | tar -xz \
 && cd install-testnet && ./install.sh && cd - && rm -rf install-testnet \
 && echo 'export PATH="$PATH:/etc/switcheoctl/bin"' >> ~/.bashrc \
 && /etc/switcheoctl/bin/switcheocli config node tcp://54.255.42.175:26657 \
 && /etc/switcheoctl/bin/switcheocli config chain-id switcheochain
