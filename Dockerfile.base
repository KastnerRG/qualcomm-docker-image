# We only ever care to do this on aarch64.
# Docker will complain, but we know better.
FROM --platform=linux/aarch64 ubuntu:24.04

# Update the base image and
# install dependencies for Qualcomm Linux
RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install -y software-properties-common \
                            clinfo \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

# Install the drivers
RUN add-apt-repository ppa:ubuntu-qcom-iot/qcom-ppa -y \
    && apt-get install -y adreno1 \
    && apt-get clean && rm -rf /var/lib/apt/lists/*
