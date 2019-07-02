---
layout: post
title:  "3. hackerrank - Staircase"
date:   2019-07-02 12:30:29 +0900
categories: jekyll update
---

[문제][site_address]
{% highlight Javascript %}
let num = parseInt(prompt('숫자를 입력해 주세요.'));

for (let i=0; i<num; i++) {
	for (let j=0; j<=num; j++){
    	if(j < (num-i)){
    		document.write('&nbsp');
        }else{
    		document.write('*');
        }
    }
    document.write('<br>');
}
{% endhighlight %}


[site_address]: https://www.hackerrank.com/challenges/staircase/problem
