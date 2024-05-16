FROM golang:1.22-alpine3.19
WORKDIR /root
COPY . /root
RUN go build dispatcher.go
CMD ./dispatcher