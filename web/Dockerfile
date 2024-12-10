# Étape 1 : Compilation


FROM golang:alpine AS builder
WORKDIR /build
COPY dispatcher.go .

RUN go build -o dispatcher dispatcher.go
# Étape 2 : Exécution

FROM alpine
WORKDIR /app
COPY static static
COPY --from=builder /build/dispatcher ./app
EXPOSE 80
CMD ["./app"]
