# golang-dockerfile

```sh
FROM golang:alpine

RUN apk update && apk add --no-cache git

WORKDIR /app

COPY . .

RUN go mod tidy

RUN go build -o binary

ENTRYPOINT ["/app/binary"]
```


### Installation

1. save as file Dockerfile di folder project
2. Run in terminal this command
   ```sh
   docker build -t image-name .
   ```
3. Cek docker images
   ```sh
   docker images
   ```
4. running docker image with this command
   ```js
   docker run -d --restart=always -p port:port nama-images
   ```
Example
   ```js
   example: sudo docker run -d --restart=always -p 9001:9001 toni-gaming
   ```




