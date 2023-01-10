build:	## Generate the website from the markdown and config file in dist
		hugo

clean:	## Clean up the content in dist
		rm -r dist/*

post:	## Create a new post whose file name and title from the Postname and Post title
		hugo new posts/$(POST_NAME).md
		sed -i 's/title: .*/title:"$(POST_TITLE)"/' content/posts/$(POST_NAME).md

help: ## Display the documentation of all targets
	@grep -E '^[a-zA-Z0-9_-]+:.*?## .*$$' $(MAKEFILE_LIST) \
	| sed -n 's/^\(.*\): \(.*\)##\(.*\)/\1:\3/p'
