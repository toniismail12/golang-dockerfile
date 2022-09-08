# golang-dockerfile

FROM golang:alpine

RUN apk update && apk add --no-cache git

WORKDIR /app

COPY . .

RUN go mod tidy

RUN go build -o binary

ENTRYPOINT ["/app/binary"]

# save as file Dockerfile di folder project

# run
# docker build -t image-name .
# docker images

# running docker image with this command
# docker run --restart=always -p port:port nama-images
# example: docker run --restart=always -p 9000:9000 golang-backend


