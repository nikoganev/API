# API

[![npm version](https://badge.fury.io/js/hubot-symphony.svg)](https://badge.fury.io/js/hubot-symphony)
[![Build Status](https://travis-ci.org/maoo/API.svg?branch=master)](https://travis-ci.org/maoo/API)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

Visit the [documentation website](http://blog.session.it/API) for more info.

## Release
The FDC3 API is released under the [FINOS NPMJS Organisation](npmjs.com/org/symphonyoss) (currently `npmjs.com/org/symphonyoss` - in transition to `npmjs.com/org/finos`).

On every commit, [semantic release](https://semantic-release.gitbook.io/semantic-release/) will be executed by Travis CI and - based on the commit message - will decide to trigger a release or not.

A release consists of:
- A version
- A `CHANGELOG.md` file
- A tag on GitHub
- An new NPM package version (published on `npmjs.org/org/finos`)

### Release setup
Travis CI must be configured with the following environment variables:
- `GH_TOKEN`, used to create tags on GitHub
- `NPM_TOKEN`, used to publish the npm package

You can setup variables [using semantic-release-cli](https://semantic-release.gitbook.io/semantic-release/usage/ci-configuration#automatic-setup-with-semantic-release-cli),  [Travis Repository Settings](https://docs.travis-ci.com/user/environment-variables/#defining-variables-in-repository-Settings) or with the [travis CLI](https://github.com/travis-ci/travis.rb#env).

### Advanced configurations
Semantic release allows [additional configurations](https://semantic-release.gitbook.io/semantic-release/usage/plugins) to customise the release flow.

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