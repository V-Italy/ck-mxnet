FROM ubuntu:16.04
MAINTAINER Grigori Fursin <Grigori.Fursin@cTuning.org>

# Install standard packages.
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    git zip bzip2 sudo wget \
    libglib2.0-0 libsm6

RUN pip3 install ck
RUN ck  version

# Install ck-mxnet
RUN ck pull repo:ck-mxnet

# Install model
RUN ck install package --tags=mxnetmodel,resnet-152

#
CMD bash
