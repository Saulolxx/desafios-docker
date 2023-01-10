FROM golang:latest AS build
WORKDIR /go/src
COPY ./src /go/src/
RUN go build ola-mundo.go

FROM scratch
WORKDIR /app
COPY  --from=build  /go/src/ola-mundo /app/
CMD ["./ola-mundo"]
