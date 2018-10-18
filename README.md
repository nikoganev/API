# API

[![npm version](https://badge.fury.io/js/hubot-symphony.svg)](https://badge.fury.io/js/hubot-symphony)
[![Build Status](https://travis-ci.org/maoo/API.svg?branch=master)](https://travis-ci.org/maoo/API)

Visit the [documentation website](http://blog.session.it/API) for more info.

## Run locally
To run the website documentation locally, please follow the steps below.

### Get rid or ruby and rbenv (MacOS)
```
brew remove ruby
brew remove rbenv
```

### Install RVM (MacOS)
```
mkdir -p ~/.rvm/src && cd ~/.rvm/src && rm -rf ./rvm && \
git clone --depth 1 https://github.com/rvm/rvm.git && \
cd rvm && ./install
rvm install 2.5.2
```

### Install gems needed for jekyll
git clone https://github.com/pages-themes/slate
cd slate
rm -rf .bundle
./script/bootstrap

# Run jekyll on other project
cd ../API/docs
gem install jekyll-theme-slate
gem install jekyll-seo-tag
gem install jekyll-watch

jekyll serve