---
layout: posts
title:  "Setup GitHub with Jekyll"
date:   2024-07-09 17:00:00 +0800
categories: jekyll
---
Install Jekyll on Ubuntu 20.04

## Install rvm to install ruby 3.3.4
```
gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
curl -sSL https://get.rvm.io | bash -s stable
source ~/.rvm/scripts/rvm
rvm install 3.3.4
rvm use 3.3.4 --default
```


## Install github-pages
```
gem install github-pages
```

## Setup new site
```
jekyll new --force kivava.github.io
```

## jekyll serve
```
jekyll serve
```

## Failed to start jekyll server. Add webrick
```
bundle add webrick
```

## Check the support layout of the theme minimal-mistakes

```
ls $(bundle show minimal-mistakes)/_layouts/
```

## Update Gemfile


Add following to Gemfile.
```
gem "minimal-mistakes-jekyll"

gem "webrick", "~> 1.8"
```

Then run
```
bundle
```

## Update _config.yml

Add following to _config.yml

```
remote_theme: "mmistakes/minimal-mistakes@4.26.2"
plugins:
  - jekyll-include-cache
```

## Reference:

[使用 Jekyll 和搭建 Github Pages](https://hackmd.io/@CynthiaChuang/Setting-Up-a-GitHub-Pages-Site-with-Jekyll)

[Minimal Mistakes Jekyll theme](https://github.com/mmistakes/minimal-mistakes)

[Load error: cannot load such file – webrick](https://talk.jekyllrb.com/t/load-error-cannot-load-such-file-webrick/5417)

[Jekyll serve fails on Ruby 3.0 #8523](https://github.com/jekyll/jekyll/issues/8523)