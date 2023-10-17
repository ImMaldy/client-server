FROM golang:1.19

WORKDIR /app/server

COPY . /app/server/

RUN go mod download
RUN go get github.com/tomiok/grpc-test-wishlist/proto

RUN CGO_ENABLED=0 GOOS=linux go build -o /docker-gs-ping

EXPOSE 50051

CMD ["/docker-gs-ping"]
