FROM golang:1.21.1

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download

COPY /server/main.go ./

EXPOSE 50051

RUN go build -o /app app/main.go
