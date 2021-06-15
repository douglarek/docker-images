FROM centos:7

RUN yum -y update
RUN rpm --import https://mirror.go-repo.io/centos/RPM-GPG-KEY-GO-REPO
RUN curl -s https://mirror.go-repo.io/centos/go-repo.repo | tee /etc/yum.repos.d/go-repo.repo
RUN yum install golang -y && yum clean all
RUN go env -w GOPROXY="https://goproxy.cn,direct"
RUN \cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
