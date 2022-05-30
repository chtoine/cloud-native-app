#GO
# BUILD
FROM docker.io/golang:1.18-alpine as build

WORKDIR /usr/src/app

COPY dispatcher.go .
RUN go build dispatcher.go

# RUN
FROM golang:1.18-alpine

ENTRYPOINT ["/go/dispatcher"]
EXPOSE 80

WORKDIR /go

COPY --from=build /usr/src/app/dispatcher /go/
COPY static /go/static/