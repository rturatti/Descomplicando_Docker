FROM golang

WORKDIR /app
ADD . /app
RUN go mod download
RUN go build -o meugo
ENTRYPOINT ./meugo