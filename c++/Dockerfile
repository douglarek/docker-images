FROM centos:7

RUN yum -y update
RUN yum install make gcc gcc-c++ cmake openssl-devel -y && yum clean all
RUN \cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
