FROM centos:7.4.1708
MAINTAINER DPP <contact@dapowerplay.com>

LABEL maintainer="dapowerplay.eth"

RUN mkdir -p /opt/parity && \
    chmod g+rwX /opt/parity && \
    yum -y update && \
    yum install -y wget && \
    wget https://releases.parity.io/v1.11.7/x86_64-unknown-centos-gnu/parity_1.11.7_centos_x86_64.rpm && \
    yum install -y parity_1.11.7_centos_x86_64.rpm && \
    rm -rf parity_1.11.7_centos_x86_64.rpm && \
    yum -y remove package wget && \
    yum clean all -y

WORKDIR /opt/parity

EXPOSE 8080 8545 8180 30301/udp

USER 1001

ENTRYPOINT [ "parity" ]