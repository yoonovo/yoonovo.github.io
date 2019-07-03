---
layout: post
title:  "1. Git hub 블로그 만들기(Window)"
date:   2019-06-30 10:30:29 +0900
categories: jekyll update
---
![image]({{ "/assets/github_logo.png" }})
<br>


<h3>1. Git hub에서 새 저장소 만들기</h3>
Git hub에 로그인하여 새 저장소를 만든다. 이때 저장소 이름(Repository name)을 <b>닉네임.github.io</b>으로 만들어야한다. 
![image]({{ "/assets/github_1.png" }})

<h3>2. Jekyll 설치하기</h3>
Git hub의 테마를 깔기위해서는 Jekyll을 설치해야하는데 Jekyll은 Ruby로 설치되기 때문에 먼저 Ruby를 설치 해주어야한다.

<b>[Ruby 설치][Ruby_download]</b>

![image]({{ "/assets/ruby1.png" }})
<br>
설치가 완료 됬다면 위와 같은 프롬프트 창이 뜬다. 1을 입력 후 창이 꺼지면 재부팅을 해준다.
명령 프롬프트 창에 `gem -v`를 입력 했을때 정상적으로 실행된다면 성공적으로 Ruby가 설치 된것이다.

{% highlight Ruby  %}
# Jekyll 설치 명령어
gem install bundler jekyll
{% endhighlight %}
마지막으로 위의 명령어를 입력해 Jekyll을 설치해준뒤 다시 재부팅을 해준다.
`jekyll -v`를 입력 했을때 정상적으로 실행된다면 성공적으로 설치 된것이다.

<h3>3. Jekyll 블로그 만들기</h3>
{% highlight Ruby  %}
# Jekyll 블로그 생성
jekyll new 블로그이름
{% endhighlight %}
특정 폴더에 위의 명령어를 입력하면 블로그 이름의 폴더와 기본 하위 폴더들이 생성된다.
지금은 Git hub의 블로그를 만드므로 블로그 이름은 <b>닉네임.github.io</b>로 만든다.

<h3>4. Git hub와 연동하기</h3>
{% highlight git  %}
# Git 로컬 저장소 생성
git init
{% endhighlight %}

{% highlight git  %}
# Git 원격 저장소 연동
git remote add origin 원격저장소Url
{% endhighlight %}

{% highlight git  %}
# 커밋하여 Git 원격 저장소에 반영
git add .
git commit -m "커밋할내용"
git push -u origin master
{% endhighlight %}
위의 명령어를 실행하면 원격 저장소와 연동되어 Github 블로그가 만들어 진다.

`https://닉네임.github.io`로 들어가면 블로그가 생성되어 있을 것이다.


[Ruby_download]: https://rubyinstaller.org/
[site_address1]: http://pygments.org/languages/
