.DEFAULT_GOAL := run

tag = latest
ARTIFACT = server

HERE  = $(shell pwd)
LANG  = $(shell basename $(HERE))
GROUP = $(shell basename $(shell dirname $(HERE)))
ZIP   = ./$(GROUP)-$(LANG)-sample-$(tag).zip


install:
	@go get

build:
	@go build -tags "nomsgpack go_json" -o $(ARTIFACT)

run: build
run:
	./$(ARTIFACT)

package: install
package: build
package:
	@zip -r $(ZIP) $(ARTIFACT)
