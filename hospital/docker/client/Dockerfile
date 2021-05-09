FROM golang:latest
RUN mkdir -p /app
WORKDIR /app
COPY go.mod .
COPY go.sum .
RUN go mod download
COPY . .
RUN go build ./hospital/hospital_client/cmd/hospital_client/client.go
CMD ["./client"]