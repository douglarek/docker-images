FROM centos:7

RUN yum -y update
RUN yum install gcc git libmpfr4 -y && yum clean all
ENV GO_VERSION 1.19.4
ENV GO_SHA256SUM c9c08f783325c4cf840a94333159cc937f05f75d36a8b307951d5bd959cf2ab8
RUN curl -L https://golang.org/dl/go$GO_VERSION.linux-amd64.tar.gz -o go$GO_VERSION.linux-amd64.tar.gz
RUN echo "$GO_SHA256SUM go$GO_VERSION.linux-amd64.tar.gz" | sha256sum -c
RUN tar -C /usr/local -xzf go$GO_VERSION.linux-amd64.tar.gz && rm -f go$GO_VERSION.linux-amd64.tar.gz
ENV PATH /usr/local/go/bin:$PATH
ENV GOROOT /usr/local/go
RUN go env -w GOPROXY="https://goproxy.cn,direct"
RUN \cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
