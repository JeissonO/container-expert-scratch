#? Multistage Builds 

#? Stage de compilacion 
FROM golang:1.14.3 AS build

WORKDIR /compose/main

COPY . ./
COPY main.go main.go
RUN CGO_ENABLED=0 go build -o backend main.go

#? Stage de despliegue
FROM alpine:3
COPY --from=build /compose/main/backend /usr/local/bin/backend
ENTRYPOINT  ["/usr/local/bin/backend"]


# sudo docker build -t "bootcampgo:v1.0" .
# sudo docker run -it --name bootcampgo bootcampgo:v1.0
# sudo docker run --rm -p 8081:8080 -it --name bootcampgo bootcampgo:v1.0