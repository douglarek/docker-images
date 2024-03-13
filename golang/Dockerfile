FROM alpine:3
RUN apk add --no-cache --update go gcc g++ tzdata
RUN go env -w GOPROXY="https://goproxy.cn,direct"
RUN ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
