NAME=tomaskral/kedge-demo-backend
VERSION=v1


.PHONY: image push

all: build

build: server.go
	go build server.go

image: build
	docker build -t $(NAME):$(VERSION) .

push:
	docker push $(NAME):$(VERSION)
