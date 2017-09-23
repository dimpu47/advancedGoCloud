FROM golang:1.8.1-alpine

RUN apk update && apk upgrade && apk add --no-cache bash git

RUN go get github.com/gin-gonic/gin

ENV SOURCES /go/src/github.com/dimpu47/advancedGoCloud/Frameworks/gin-microservice/
COPY . ${SOURCES}

RUN cd ${SOURCES} && CGO_ENABLED=0 go build

WORKDIR ${SOURCES}
CMD ${SOURCES}gin-microservice
EXPOSE 8080