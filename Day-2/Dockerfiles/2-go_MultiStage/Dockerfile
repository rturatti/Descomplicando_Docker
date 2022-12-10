#build stage
FROM golang AS builder
WORKDIR /app
COPY . /app
RUN go mod download
RUN go build -o meugo

#final stage
FROM alpine:latest
WORKDIR /giropops
COPY --from=builder /app /giropops
ENTRYPOINT ./meugo
LABEL Name=descomplicandodocker Version=0.0.1
