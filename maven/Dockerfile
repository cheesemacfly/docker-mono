FROM ubuntu:16.04

MAINTAINER Jo Shields <jo.shields@xamarin.com>

#based on dockerfile by Michael Friis <friism@gmail.com>

RUN apt-get update \
  && apt-get install -y curl \
  && apt-get -y upgrade \
  && rm -rf /var/lib/apt/lists/*

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF
RUN echo "deb http://download.mono-project.com/repo/ubuntu stable-xenial main" | tee /etc/apt/sources.list.d/mono-official-stable.list
RUN apt-get update \
  && apt-get install -y binutils mono-devel ca-certificates-mono nuget \
  && rm -rf /var/lib/apt/lists/* /tmp/*

ENV MONO_TLS_PROVIDER=btls
