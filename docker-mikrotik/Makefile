#!make

ROUTEROS_VERSION := 7.10.1
TARGET := pantigon/mikrotik

all: build latest

build:
	docker buildx create --use
	docker buildx build --platform=linux/amd64,linux/arm64 -t $(TARGET):$(ROUTEROS_VERSION) --push .

latest:
	docker buildx create --use
	docker buildx build --platform=linux/amd64,linux/arm64 -t $(TARGET):latest --push .
