FROM golang:1.22-alpine3.19 as build
WORKDIR /root
COPY . /root
RUN go build dispatcher.go

FROM alpine:3.19
RUN adduser -S stefan
USER stefan
WORKDIR /home/stefan
COPY --chown=stefan:stefan ./static ./static
COPY --from=build --chown=stefan:stefan /root/dispatcher .
EXPOSE 80
CMD ./dispatcher