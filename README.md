# API

[![npm version](https://badge.fury.io/js/hubot-symphony.svg)](https://badge.fury.io/js/hubot-symphony)
[![Build Status](https://travis-ci.org/maoo/API.svg?branch=master)](https://travis-ci.org/maoo/API)

Visit the [documentation website](http://blog.session.it/API) for more info.

## Release
The FDC3 API is released under the [FINOS NPMJS Organisation](npmjs.com/org/symphonyoss) (currently `npmjs.com/org/symphonyoss` - in transition to `npmjs.com/org/finos`).

## Run locally
To run the website documentation locally, please follow the steps below.

### Install Ruby (MacOS)

It is strongly advised to use RVM or RBenv to install Ruby; below are the steps to install RVM on MacOS.
```
mkdir -p ~/.rvm/src && cd ~/.rvm/src && rm -rf ./rvm && \
git clone --depth 1 https://github.com/rvm/rvm.git && \
cd rvm && ./install
rvm install 2.5.2
which bundle #Should return a .rvm sub-path
which ruby #Should return a .rvm sub-path
```

### Install gems needed for jekyll

```
cd /tmp
git clone https://github.com/pages-themes/slate
cd slate
rm -rf .bundle
./script/bootstrap
gem install jekyll-theme-slate
gem install jekyll-seo-tag
gem install jekyll-watch
```

# Run jekyll on other project
```
cd ../API/docs
jekyll serve --incremental
```