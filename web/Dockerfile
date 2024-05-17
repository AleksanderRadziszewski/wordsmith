FROM golang:1.22-alpine3.19 as build
WORKDIR /root
COPY . /root
RUN go build dispatcher.go
CMD ./dispatcher

FROM alpine:3.19
RUN adduser stefan
USER stefan
WORKDIR /root
COPY --from=build --chown=stefan:stefan /root/dispatcher .
CMD ./dispatcher