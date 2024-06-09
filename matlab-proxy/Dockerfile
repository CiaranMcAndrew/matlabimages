FROM ubuntu:22.04

USER root

# Install dependencies for matlab-proxy
RUN DEBIAN_FRONTEND=noninteractive && \
    apt-get update && apt-get install --no-install-recommends -y \
    python3 \
    python3-pip \
    xvfb \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install matlab-proxy

ENTRYPOINT ["matlab-proxy-app"]