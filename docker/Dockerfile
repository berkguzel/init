FROM golang:1.14.13-alpine AS builder
WORKDIR /init
COPY go.* ./
RUN go mod download 
COPY . . 
RUN CGO_ENABLED=0 go build -o /src ./

FROM alpine
COPY --from=builder ./src ./init
CMD [ "./init" ]