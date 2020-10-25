---
author: Yuan Tian
title: Build a Personal Blog
date: 2020-10-25 12:55:53
tags: ["Hexo"]
categories: ["Tech"]
subtitle: This article tells the blogger's steps to use Hexo to build static blog on macOS.
---

## Install
### Git
install Xcode through App Store 

``` Bash
# Install Xcode Command Line Tools
$ xcode-select --install

# Install Homebrew
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

$ brew install git
```

### Node
Node.js is an open-source, cross-platform, back-end, JavaScript runtime environment that executes JavaScript code outside a web browser.
``` Bash
brew install node
```

### Hexo

```shell
npm install -g hexo-cli
npm install hexo

# verification
hexo version
```

## Create a new post
```shell
# create a new .md file
hexo new [layout] <title>
hexo new "blog_built"

# open the file through IDE
tags: [Hexo, notes, ...]

# write it at the bottom of abstract
<!-- more -->

# write down the content in md style
```
layout: post, page, draft.  `./source/`

If necessary, you should create draft file at first, and then execute `hexo publish draft_file_name` to be the post file

## Generate and deploy

```shell
# generate static files
hexo g/generate

# start a server: localhost:4000
hexo s/server

# deploy your website
hexo d/deploy

# update your blog 
hexo clean public && hexo g && hexo d
```

