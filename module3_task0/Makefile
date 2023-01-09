build:	## Generate the website from the markdown and config file in dist
		hugo

clean:	## Clean up the content in dist
		rm -r dist/*

post:	## Create a new post whose file name and title from the Postname and Post title
		hugo new posts/$(POST_NAME).md
		sed -i 's/title: .*/title:"$(POST_TITLE)"/' content/posts/$(POST_NAME).md

help:	## Display the documentation of all targets
		@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'
