FROM debian:buster-slim

ARG API_KEY
ENV API_KEY $API_KEY

RUN set -eux; \
  apt-get update; \
  apt-get \
    install \
      --assume-yes \
      --no-install-recommends \
      python3-setuptools \
      python3-pip \
      bind9-host \
      less \
      curl \
      vim \
      mariadb-client \
      netcat \
      tcpdump \
      zlib1g bzip2 xz-utils \
      dnsutils telnet \
      coreutils tmux procps \
      jq; \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*; \
  pip3 install \
    setuptools; \
  pip3 install \
    wheel \
    requests \
    shodan ; \
  shodan init ${API_KEY};
