#makefile for hugo

build: ## build
    go build -o ${BINARY_NAME} main.go


clean: ## clean
    go clean
    rm ${BINARY_NAME}

post: ## post
	hugo new posts/$(POST_NAME).md
	sed -i 's/title: .*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md

help: ## usage: make help
	@echo "Usage:"
	cat Makefile | grep '##' | tr -d '##'
