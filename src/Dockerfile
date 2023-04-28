FROM ghcr.io/linuxserver/baseimage-ubuntu:jammy

ARG DEBIAN_FRONTEND=noninteractive
ARG TMR_RELEASE=v2.0.0

RUN apt-get update && \
  apt-get install -y libglu1 libxcursor1 xvfb xz-utils && \
  curl -o \
    /tmp/TMR-GunUpdate_Server.tar.xz -L \
    "https://github.com/DaRealRoyal/TMR-GunUpdate/releases/download/v2.0.0/TMR-GunUpdate_Server.tar.xz" && \
  mkdir /app/tmr-gunupdate_server && \
  tar xf \
    /tmp/TMR-GunUpdate_Server.tar.xz -C \
    /app/tmr-gunupdate_server --strip-components=1

COPY /root /
