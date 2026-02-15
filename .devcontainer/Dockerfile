FROM mcr.microsoft.com/devcontainers/base:ubuntu

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    novnc \
    websockify \
    xvfb \
    x11vnc \
    fluxbox \
    && apt-get clean

RUN mkdir /opt/vnc
COPY start-vnc.sh /opt/vnc/start-vnc.sh
RUN chmod +x /opt/vnc/start-vnc.sh

EXPOSE 6080
