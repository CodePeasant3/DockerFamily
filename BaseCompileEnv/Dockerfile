ARG UBUNTU_VERSION=""

FROM ubuntu:${UBUNTU_VERSION}

ENV TZ=Asia/Shanghai

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt update

RUN apt install -y gpg curl git g++ gcc build-essential wget lsb-release software-properties-common 

RUN curl https://apt.kitware.com/keys/kitware-archive-latest.asc | apt-key add -

RUN echo "deb https://apt.kitware.com/ubuntu/ `lsb_release -c -s` main" | tee /etc/apt/sources.list.d/kitware.list

RUN apt update

RUN apt install -y cmake

RUN gcc --version

RUN cmake --version
