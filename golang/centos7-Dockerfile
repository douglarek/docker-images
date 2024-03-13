FROM centos:7

RUN yum -y update
RUN yum install gcc git libmpfr4 -y && yum clean all
ENV GO_VERSION 1.22.1
ENV GO_SHA256SUM aab8e15785c997ae20f9c88422ee35d962c4562212bb0f879d052a35c8307c7f
RUN curl -L https://golang.org/dl/go$GO_VERSION.linux-amd64.tar.gz -o go$GO_VERSION.linux-amd64.tar.gz
RUN echo "$GO_SHA256SUM go$GO_VERSION.linux-amd64.tar.gz" | sha256sum -c
RUN tar -C /usr/local -xzf go$GO_VERSION.linux-amd64.tar.gz && rm -f go$GO_VERSION.linux-amd64.tar.gz
ENV PATH /usr/local/go/bin:$PATH
ENV GOROOT /usr/local/go
RUN go env -w GOPROXY="https://goproxy.cn,direct"
RUN \cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
