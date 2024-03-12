# build aplication
FROM golang:1.22-alpine as build

WORKDIR /go/src/app
COPY . .

RUN go mod download && go mod verify
RUN CGO_ENABLED=0 go build -v -o /go/bin/app

# image application
FROM scratch

COPY --from=build /go/bin/app /

CMD ["/app"]