FROM ubuntu:20.04

WORKDIR /home

ENV PATH /usr/local/bin:/usr/bin:/usr/local/sbin:/usr/sbin
ENV TZ=Asia/Shanghai
ENV LC_ALL=C

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN rm /bin/sh && ln -s /bin/bash /bin/sh

RUN apt-get update -y
RUN apt-get install -y git openssh-server
RUN apt-get install -y net-tools
RUN apt-get install -y vim
RUN apt-get install -y rsync
RUN apt-get install -y cmake
RUN apt-get install -y gdb
RUN apt-get install -y build-essential

RUN apt-get install -y libboost-all-dev

RUN mkdir -p /var/run/sshd
RUN mkdir -p /root/.ssh/
RUN echo root:123 | chpasswd
#RUN ssh-keygen -q -t rsa -b 2048  -f /etc/ssh/ssh_host_rsa_key -P '' -N ''
#RUN sed -i 's/PermitRootLogin without-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN echo PermitRootLogin yes >> /etc/ssh/sshd_config

EXPOSE 22

CMD ["/usr/sbin/sshd", "-D"]
