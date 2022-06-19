---
title:  "Github io로 블로그 만드는 방법"
excerpt: "깃허브로 블로그 사이트 만들기. "

categories:
  - Blog
tags:
  - [Blog, jekyll, Github, Git]
  -
sidebar:
  nav: "docs"

toc: true
toc_sticky: true
 
date: 2022-06-19
last_modified_at: 2020-06-19
---

# how to make github io blog
github io로 블로그를 만드려 했는데, jekyll 다운이 너무 안 되어서 velog로 시작을 했다. 그런데 첫 게시물을 쓰는 도중 velog에서는 수식에 넘버링이 안 된다는 것을 알고 velog도 내 블로그에는 적합하지 않다는 것을 알게 되었다. 다시 github io 블로그를 만드려고 했고 이번에는 성공했다. 

## 1. make github repository
깃허브에 가서 [내 아이디].github.io라는 이름의 repository를 만든다. 내 아이디는 hossung이니 repository이름은 hossung.github.io이다.

## 2. clone the repository on your local environment
~~~
git clone [your repository link].git
~~~
을 terminal에 입력하면 된다. 예를 들어 나 같은 경우에는
~~~
git clone https://github.com/hossung/hossung.github.io.git
~~~
인 것이다. 이러면 내 컴퓨터에 hossung.github.io라는 폴더가 하나 만들어진다.

## 3. install [ruby](https://rubyinstaller.org/downloads/)
With DEVKIT에서 가장 위에 있는 것을 다운 받으면 된다

## 4. jekyll과 bundler 설치
~~~
gem install bundler
~~~
를 하여 jekyll과 budler를 설치하고
~~~
jekyll -v
~~~
로 설치가 잘 되었는지 확인한다. 맨처음 이 단계에서 오류가 많이 떠서 헤맸는데 특히 PATH 설정 때문이었다. .zshrc파일을 초기화하고 처음부터 모든 것을 설치했더니 잘 해결되었다.

## 5. jekyll 테마 설정

[jekyllthemes.org](http://jekyllthemes.org)에서 마음에 드는 테마를 고르고 깃허브에 들어가 파일을 모두 다운받으면 된다. 그리고 2. 에서 clone을 통해서 만든 폴더에 그 파일들을 모두 갖다붙이면 된다. 이후 다음과 같은 방법으로 이 파일들을 내 github에 commit해준다.
~~~
cd [clone을 통해 만든 github 폴더 경로]
~~~
나 같은 경우에는 
~~~
cd /Users/ahnhosung/hossung.github.io
~~~
였다. 이후 
~~~
git add .
git commit -m ""
git push origin main
~~~
을 터머널에서 실행해준다. 내 깃허브 사이트에 들어가면 폴더에 있던 파일이 내 깃허브에 올라가 있을 것이다. 또한 https://[내 깃허브 아이디].github.io로 들어가면 내가 골랐던 테마의 형식의 사이트가 만들어져 있어야 한다.

다음에는 포스팅을 하는 방법에 대해서 알아보겠다. 참고로 이는 내 첫 글이다.
