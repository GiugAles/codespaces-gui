FROM mcr.microsoft.com/devcontainers/base:ubuntu

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    xfce4 \
    xfce4-goodies \
    tightvncserver \
    novnc \
    websockify \
    dbus-x11 \
    x11-xserver-utils \
    && apt-get clean

RUN mkdir /opt/vnc
COPY start-vnc.sh /opt/vnc/start-vnc.sh
RUN chmod +x /opt/vnc/start-vnc.sh

EXPOSE 6080
