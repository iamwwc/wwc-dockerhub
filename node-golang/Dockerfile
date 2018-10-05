FROM node:8.12.0-jessie

RUN apt-get update;\
    apt-get install wget --no-install-recommends;

RUN wget -O go.tgz "https://dl.google.com/go/go1.11.1.linux-amd64.tar.gz";\
    tar -C /usr/local -xzf go.tgz; \
	  rm go.tgz; \
    export PATH="/usr/local/go/bin:$PATH"; \
	  go version;

ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/go/bin:$PATH
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
