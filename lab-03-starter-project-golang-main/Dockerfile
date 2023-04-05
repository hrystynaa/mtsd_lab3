FROM golang:1.20.2 AS builder

WORKDIR /lab3_golang

# Dependencies
COPY go.mod go.sum  ./

RUN go mod download 

#Code
COPY . .

RUN CGO_ENABLED=0 go build -ldflags "-w -s -extldflags '-static'" -o build/fizzbuzz

FROM gcr.io/distroless/static-debian11

COPY --from=builder /lab3_golang/build/fizzbuzz /fizzbuzz

COPY --from=builder /lab3_golang/templates/index.html /templates/

CMD ["/fizzbuzz", "serve"]
