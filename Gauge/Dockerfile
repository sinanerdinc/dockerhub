FROM ubuntu:23.10
LABEL MAINTAINER="Sinan Erdinc <mail@sinanerdinc.com>"

RUN apt-get --allow-releaseinfo-change update && apt-get install -q -y \
    curl \
    wget \
    zip \
    unzip \
    openjdk-11-jdk \
    apt-transport-https \
    gnupg2 \
    ca-certificates\
    maven \
    nodejs \
    npm

RUN npm install -g @testmo/testmo-cli
RUN curl -SsL https://downloads.gauge.org/stable | sh
ENV PATH=$HOME/.gauge:$PATH

# Install gauge plugins
RUN gauge install java && \
    gauge install html-report && \
    gauge install xml-report && \
    gauge install screenshot \

# Install lambdatest tunnel
RUN wget https://downloads.lambdatest.com/tunnel/v3/linux/amd64/LT_Linux.zip \
    && unzip LT_Linux.zip \
    && rm LT_Linux.zip \
    && chmod +x LT