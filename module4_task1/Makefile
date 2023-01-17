help:	## Show this
	sed -ne '/@sed/!s/## //p' Makefile

.PHONY: build
build:	## Generate the website from the markdown language
	brew install hugo
	hugo
	touch awesome-api

clean:	## Delete the website done with build command
	rm -rf dist/*

post:	## Create a new blog post from the environment variables POST_TITLE and POST_NAME
	hugo new posts/$(POST_NAME).md
	sed -i 's#title: ".*"#title: "$(POST_TITLE)"#g' content/posts/$(POST_NAME).md

package: ## Create a package
	make build
	mkdir -p dist
	zip awesome-website.zip dist

lint: ## lint with markdown
	apt install curl -y
	curl --silent --location https://deb.nodesource.com/setup_16.x | bash -
	apt install nodejs -y
	npm install -g markdownlint-cli 1>&2
	markdownlint README.md
	markdownlint DEPLOY.md

unit-tests: ## not implemented yet
	touch coverage-units.out

integration-tests: ## not implemented yet
	touch coverage-integrations.out

.PHONY: build-docker
build-docker: ## build docker debian
	docker build -t "awesome:build" ./build

.PHONY: build-dependencies
