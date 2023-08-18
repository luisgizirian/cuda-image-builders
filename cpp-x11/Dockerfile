FROM cuda/base:latest

VOLUME /tmp/.X11-unix:/tmp/.X11-unix:rw
VOLUME $HOME/.Xauthority:/root/.Xauthority
# ADD $HOME/.Xauthority /root/.Xauthority

#
# `xauth` for X11 forwarding
# `libsfml-dev` for SFML
#
RUN apt-get update && apt-get install -y --no-install-recommends \
    xauth libsfml-dev \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean

#Update libraries
RUN ldconfig

#
# Setup environment variables
#
ENV XAUTHORITY=/root/.Xauthority
ENV DISPLAY="$DISPLAY"
