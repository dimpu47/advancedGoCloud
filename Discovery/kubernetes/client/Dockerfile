FROM golang:1.0.1-alpine

ENV SOURCES /go/src/github.com/dimpu47/advancedGoCloud/Discovery/kubernetes/
COPY . ${SOURCES}

RUN cd ${SOURCES}client/ && CGO_ENABLED=0 go build

WORKDIR ${SOURCES}client/
CMD ${SOURCES}client/client
