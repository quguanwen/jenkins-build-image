FROM 10.0.1.10:60080/jenkins/inbound-agent:4.3-4

USER root

RUN wget https://download.docker.com/linux/static/stable/x86_64/docker-19.03.1.tgz && \
    tar -xf docker-19.03.1.tgz  && \
    mv docker/* /usr/local/bin/ && \
    rm -rf docker-19.03.1.tgz

## https://storage.googleapis.com/kubernetes-release/release/v1.17.3/bin/linux/amd64/kubectl 

COPY kubectl /usr/local/bin/ 

RUN  chmod +x /usr/local/bin/kubectl

