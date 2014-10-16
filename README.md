<div align="middle">
<img src ="images/logos/jonx_logo200px.png" alt="jonx logo" title="jonx logo">
<h1>T H E J O N X</h1>
</div>
<br />

![Build Status](https://travis-ci.org/the-jonx/the-jonx.github.io.svg?branch=master)](https://travis-ci.org/thejonx/thejonx.github.io)

This repository contains the code needed to build [thejonx.com](thejonx.com) and generates [thejonx.github.io](https://thejonx.github.io). When a pull request is merged into the `master` branch, [Travis CI](http://travis-ci.org) pulls the repository, builds the new site, and pushes a staged version to `live/` in the `stage-live` branch upon successfully building the changes. The `live` directory is then synchronized with our production web server.

## Set up Ruby development environment.
Because [Jekyll](http://jekyllrb.com) generates The Jonx's website, we strongly recommend setting up a Ruby development environment. This will make it easier for you to generate pages and see the results of your work. However, if you do not wish to do this, you can manually add [markdown](https://en.wikipedia.org/wiki/Markdown) files to the `_posts/` or `_pages/` directories. Files in the `_posts` directory will result in new blog posts being added to The Jonx's Project Blog. Files in the `_pages/` directory populate the pages on The Jonx's web site.

To begin, you'll need a [github account](https://github.com/account) and [git](https://help.github.com/articles/set-up-git) installed on your computer. Once that's out of the way, install Ruby and configure git as described on [GoRails](https://gorails.com/setup#ruby). Finally, run `bundle install` to install all gems needed to build the site. If you're an advanced user, you might want to get started with an isolated, pre-made Jekyll environment like a [Docker container](https://registry.hub.docker.com/u/grahamc/jekyll) or a [Vagrant image](https://vagrantcloud.com/marty/boxes/trusty64).

## Adding new pages and blog posts.
To add a new page, make and create a new branch with `git checkout -b <mynewstuff>` and run `rake page:create`. You can add new blog posts with `rake post:create`. Once you've added content to your new page or post, `rake site:watch` will build the site and host it at [http://localhost:4000](http://localhost:4000). It even automatically updates your changes!

## Pushing changes to the internet.
When your new site is ready, use `git add` to stage the new files, `git commit -m 'Add new page with a super awesome commit message'` to add a message to the commit log, and `git push origin <mynewstuff>` to push the changes to the internet. Your change will be merged in as soon as someone reviews it and be posted to the internet soon!

If you have any trouble setting up a development environment or suspect a bug, please open an [issue](https://github.com/the-jonx/the-jonx.github.io/issues).
