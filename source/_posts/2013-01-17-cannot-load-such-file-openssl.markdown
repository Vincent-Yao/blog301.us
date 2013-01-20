---
layout: post
title: "Cannot Load Such File - Openssl"
date: 2013-01-17 09:37
comments: true
categories: [Ruby, Octopress]
author: 姚武平
---
##问题描述:
用Octopress搭建博客,启动WEBrick时遇到如下错误:

```ruby
/home/dinduks/.rvm/gems/ruby-1.9.3-p362/gems/activesupport-3.1.3/lib/active_support/dependencies.rb:240:in `require’: cannot load such file – openssl (LoadError)
```
##原因:
本安装的Rub在编译的时候没有用openssl.

##解方方法:

1.安装openssl
```ruby
rvm pkg install openssl
```

2.删除已有的ruby
```ruby
rvm remove 1.9.3
```

3.重新安装ruby,并明确指出编译的时候使用openssl
```ruby
rvm install 1.9.3 --with-openssl-dir=$HOME/.rvm/usr
```

4.使用该ruby
```ruby
rvm use 1.9.3 --default
```

##参考文献:
[Live geek or die tryin'](http://www.dinduks.com/rails-cannot-load-such-file-openssl/)的博客.
