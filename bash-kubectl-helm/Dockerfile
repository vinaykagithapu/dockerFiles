FROM ubuntu:20.04 AS base
RUN apt update
RUN apt install curl -y
RUN curl -LO https://dl.k8s.io/release/v1.20.0/bin/linux/amd64/kubectl
RUN curl -LO https://get.helm.sh/helm-v3.9.0-linux-amd64.tar.gz
RUN tar -zxvf helm-v3.9.0-linux-amd64.tar.gz

FROM bash:5.0
COPY --from=base kubectl /usr/local/bin/kubectl
COPY --from=base linux-amd64/helm /usr/local/bin/helm
RUN chmod +x /usr/local/bin/kubectl
RUN chmod +x /usr/local/bin/helm

