default: build image

cleanall: clean rmi

clean:
	go clean

build:
	CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o GoLinkShortener

image:
	docker build -t short-url .

rmi:
	docker rmi short-url
