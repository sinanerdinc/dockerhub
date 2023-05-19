FROM ubuntu:23.10
LABEL authors="Sinan Erdinc <mail@sinanerdinc.com>"

RUN apt-get --allow-releaseinfo-change update && apt-get install -q -y \
    curl \
    ca-certificates \
    unzip \
    openjdk-11-jdk \
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
    gauge install screenshot

# Install lambdatest tunnel
RUN curl -o LT_Linux.zip https://downloads.lambdatest.com/tunnel/v3/linux/64bit/LT_Linux.zip \
    && unzip LT_Linux.zip \
    && rm LT_Linux.zip \
    && chmod +x LT
