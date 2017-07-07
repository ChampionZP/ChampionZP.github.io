---
layout: post
title:  "how to construct your own github pages"
date:   2017-07-07
excerpt: "If you want to have your own pages to manage your shares and your projects,this post may be useful."
tag:
- tutorial	
- post
- github pages 
comments: true
---
Before you set your own pages, make sure you have finished following steps:
* you have already created a github account [github](https://github.com/);
* lunix or macos operating system would be better;
* you have access to google;
* you have already installed [git](https://www.howtoforge.com/tutorial/install-git-and-github-on-ubuntu-14.04/) on your laptop;

## step1
choose a project from `jekyllthemes.org` and then folk it to your github;
## step2
rename the project you folked in step1 as the form "username.github.io";
(careful,the `username` here is the name of your own github account')
## step3
clone this project to your laptop,for example:
{% highlight css %}
git clone https://github.com/ChampionZP/ChampionZP.github.io.git
{% endhighlight %}
## step4
enter the folder `ChampionZP.github.io` and modify the contex of `_config.yml` to your own information;
## step5
run following codes in your terminal:
{% highlight css %}
git add .
git commit -m 'modified _config.yml'
git push -u origin master
{% endhighlight %}

now you can open a new page in your broswer and go to address `https://username.github.io`