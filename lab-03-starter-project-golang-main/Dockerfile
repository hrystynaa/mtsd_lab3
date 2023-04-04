FROM golang:1.20.2

WORKDIR /lab3_golang

# Dependencies
COPY go.mod go.sum  ./

RUN go mod download 

#Code
COPY . .

RUN go build -o build/fizzbuzz

CMD ["./build/fizzbuzz", "serve"]

