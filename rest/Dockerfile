FROM golang:alpine as builder
WORKDIR /myapp
COPY . /myapp/
RUN go build

FROM alpine
COPY --from=builder /myapp/rest /myapp/rest 
EXPOSE 10000
ENTRYPOINT ["/myapp/rest"]
