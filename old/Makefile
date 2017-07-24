PROJDIR=$(dir $(realpath $(firstword $(MAKEFILE_LIST))))

.PHONY: all
all: build

.PHONY: build
build: $(PROJDIR)/tools/bin/tmpl
	cat $(PROJDIR)/templates/etcd.yaml | tmpl > $(PROJDIR)/resources/etcd.yaml

$(PROJDIR)/tools/bin/tmpl:
	GOBIN=$(PROJDIR)/tools/bin go get -u github.com/tmc/tmpl
