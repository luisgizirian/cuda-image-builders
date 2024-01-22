FROM cuda/base:latest

#
# `libsfml-dev` for SFML
#
RUN apt-get update && apt-get install -y --no-install-recommends \
    libsfml-dev \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean

#Update libraries
RUN ldconfig
