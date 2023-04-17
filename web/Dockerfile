FROM golang AS web_golang
COPY dispatcher.go .
RUN go build dispatcher.go

FROM ubuntu
EXPOSE 80
RUN apt update -y && apt install apache2 -y && service apache2 start
COPY --from=web_golang /go/dispatcher /
COPY static /static
CMD ["/dispatcher"]