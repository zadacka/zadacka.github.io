---
layout: post 
title:  "Getting Started"
tags: [gist]
featured_image_thumbnail:
featured_image: assets/images/posts/2021/laptop.jpg
---

There are pre-requisites to blogging with GitHub Pages and Jekyll.

The [https://jekyllrb.com/docs/installation/macos/](official jekyll instructions) are definitely a good place to look as they are more likely to be maintained than my notes below...

Assuming that you are setting up on MacOS, you'll want the following

```bash

# Install xcode command line tools:
xcode-select --install

# Install homebrew - the *package manager* which will let us install other stuff
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install a new ruby (not using venv, as I'm not a ruby dev, so one ruby is enough!)
brew install ruby

# Add the brew ruby (local user install location) to my PATH (for Zsh):
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc

# Source the config file, and check which ruby is used
source ~/.zshrc
which ruby

# install bundler (dependency management), jekyll (static website generation) tools
gem install --user-install bundler jekyll

# Get the ruby version, and include the relevant gem in the path too
ruby -v 
echo 'export PATH="$HOME/.gem/ruby/3.0.0/bin:$PATH"' >> ~/.zshrc

# Confirm that the new gem file is used
gem env

# now install the packages specified in the gem file
cd path/to/project
bundle install

# if you want to use Jekyll to serve content (generate and serve content)
# then you will additionally need to install the webrick Gem which doesn't 
# come included with the latest version of Ruby:
# https://github.com/github/pages-gem/issues/752
bundle add webrick
bundle exec jekyll serve

```

Yes, you are using homebrew (package manager) to download ruby (language) so that you can use RubyGems(package manager) to dowload Jekyll (webpage generation program) and bundler (dependency manager). Bundler will also download and manage version requirements of a number of other Ruby dependencies or 'gems' via a 'gemfile'.