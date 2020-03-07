---
layout: post
title: Jekyll 블로그 로컬에서 시작할 때 버전 호환 이슈 해결 방법
category: Jekyll
permalink: /jekyll/:year/:month/:day/:title/
tags: [Jekyll]
comments: true
---
jekyll로 블로그를 로컬에서 돌려보려 할 때, 아래와 같은 Error 메시지를 볼 때가 있다.<br>
이것은 jekyll 버전 호환 문제가 발생하여 나타나는 현상으로 보인다.

```
You have already activated jekyll 3.8.6, but your Gemfile requires jekyll 3.8.5. Prepending `bundle exec` to your command may solve this. (Gem::LoadError)
```

이는 bundler를 사용하면 쉽게 해결할 수 있다.<br>
아래 명령어로 설치와 실행을 하면 된다.

```
gem install bundler
bundle install
bundle exec jekyll serve
```

나는 항상 블로그를 로컬에서 돌릴 때 마지막 명령어로 돌리고, 그 결과 나오는 주소로 들어가 확인해본다.