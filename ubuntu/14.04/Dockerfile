FROM ubuntu:14.04
MAINTAINER Zhang Erning <zhang@erning.com>

# timezone
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime

# locale
RUN locale-gen en_US.UTF-8 \
  && update-locale LC_ALL="en_US.UTF-8" LANG="en_US.UTF-8"

# cn mirror
RUN sed -i 's/http:\/\/archive.ubuntu.com/http:\/\/cn.archive.ubuntu.com/g' \
    /etc/apt/sources.list
# RUN apt-get update && apt-get upgrade -y && rm -rf /var/lib/apt/lists/*
