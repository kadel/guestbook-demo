NAME=quay.io/tomakral/kedge-demo-frontend
VERSION=v1

.PHONY: image push

image:
	docker build -t $(NAME):$(VERSION) .

push:
	docker push $(NAME):$(VERSION)
