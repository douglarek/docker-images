FROM centos:7

RUN yum -y update
RUN yum install gcc cmake -y && yum clean all
RUN \cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
