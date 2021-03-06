---
layout: post 
title:  "Getting Started"
tags: [gist]
featured_image_thumbnail:
featured_image: assets/images/posts/2021/laptop.jpg
---

There are pre-requisites to blogging with GitHub Pages and Jekyll.

If doing this on a Mac, you need the following:

```bash
# These steps follow https://jekyllrb.com/docs/installation/macos/
# but are less likely to get maintained ... so you may want to look there!

# Install xcode command line tools"
xcode-select --install

# Install homebrew - the *package manager* which will let us install other stuff
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install a new ruby (not using venv, as I'm not a ruby dev, so one ruby is enough!)
brew install ruby

# Add the brew ruby to my PATH (for Zsh):
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc

# Source the config file, and check which ruby is used
source ~/.zshrc
which ruby

# install bundlr, jekyll
gem install --user-install bundler jekyll

# Get the ruby version, and include the relevant gem in the path too
ruby -v 
echo 'export PATH="$HOME/.gem/ruby/3.0.0/bin:$PATH"' >> ~/.zshrc

# Confirm that the new gem file is used
gem env

# now install the packages specified in the gem file
cd path/to/project
bundle install





```