FROM node:18-bullseye-slim

ENV TZ=Asia/Tokyo \
    LANG=C.UTF-8

WORKDIR /tmp

RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NOWARNINGS=yes \
    && apt-get -qq update > /dev/null \
    && apt-get -qq --no-install-recommends --yes install \
        ca-certificates git less vim jq curl wget tar zip unzip file procps htop ncdu fish > /dev/null \
    && chsh --shell /usr/bin/fish
