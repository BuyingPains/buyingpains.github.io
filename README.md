README 
buyingPains.github.io  

## About This Repository

This repository is a work-in-progress website. We are creating a website dedicated to the cause of of increased transparency in textile supplies and sales.

## For Guests

Guests may visit our main site to explore our topics and resources. If you would like to contribute, visit our Take Action page.

## For Content Editors 

This section describes how to make updates to the site content (text, images, resources, and videos)

Site Architecture

How to Make Updates

## For Developers

This section describes how to make updates to the site architecture for developers who need to modify more than the content (site meta-info, layout and rendering).

### Site Architecture
 - GithHub Pages for hosting the code and site (both version control and serving). See tips on GitHub Pages below.
 - Jekyll (default for GitHub Pages) for building a static site given MarkDown/Liquid/Jekyll source code. 

### Learning Path to prepare to use this site.
1. Review Github Pages's Jekyll docs, but don't let them confuse you. They are confusing: https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/setting-up-a-github-pages-site-with-jekyll

2. Read Jekyll's docs start to finish (they are quick and effective): https://jekyllrb.com/docs/
			
3. If you haven't yet, go look at the directory structure of BuyingPains.Github.io and identify the different components

4. Read this CloudCannon's Jekyll docs start to finish. These docs are the most detailed and had the biggest influence on the buying pains source code: https://learn.cloudcannon.com/
	- All pages use a default layout
	- Resources are stored altogether as a csv and accessible as data.
	- Topic pages utilize include videos, images, liz-takes, and one or more topic-fragments. Topic-fragments include a header, text, and resources.

### Suggested development workflow

1. For changing content in the source code, it is recommended to create and test local versions of the project, and then merge with the live site when updates are ready.

2. Get a local version of the project set up. In a local terminal, run

	git fork https://github.com/BuyingPains/buyingpains.github.io.git
	git checkout -b updates-YYMMDD

3. in your new branch, create a .gitignore file. Ignore the following:
	
	``_``site/
	Gemfile
	Gemfile.lock
	.jekyll-metadata

4. Configure local environment for jekyll builds. In a local terminal, run

	gem install jekyll bundler
	gem install 'jekyll-theme-midnight'

5. create a Gemfile in your local branch. Add the  to it.
	
	source 'https://rubygems.org'
	gem 'github-pages', group: :jekyll_plugins
	gem 'jekyll-theme-midnight'

6. In a terminal in your local branch, run 
	bundle exec jekyll serve

7. check out localhost:4000 to view the site.

8. make changes on your local branch 'updates-YYMMDD' and test using your locally served site. 

9. Once ready, create a pull request to merge your updates branch into master. 

10. Repository owner needs to accept the pull request.

11. View the live site 