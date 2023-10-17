FROM golang:1.21.1

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY /server/main.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /servidor-docker

EXPOSE 50051

CMD ["/servidor-docker"]
