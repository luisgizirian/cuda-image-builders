FROM nvcr.io/nvidia/l4t-base:35.3.1

#
# `sudo` for sudo (util needed for execution)
# `nvidia-cuda-dev` for CUDA developer packages (optionally `nvidia-cuda` for CUDA runtime only)
# `xauth` for X11 forwarding
# `libsfml-dev` for SFML
# `git` for git
# `htop` for htop (optional)
#
RUN apt-get update && apt-get install -y --no-install-recommends \
    sudo nvidia-cuda-dev git htop \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean

#
# Setup environment variables
#
ENV CUDA_HOME="/usr/local/cuda"
ENV PATH="/usr/local/cuda/bin:$PATH"
ENV LD_LIBRARY_PATH="/usr/local/cuda/lib64:$LD_LIBRARY_PATH"
