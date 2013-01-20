---
layout: post
title: "zsh: no matches found"
date: 2013-01-17 09:52
comments: true
categories: [Linux]
---

##问题描述:
使用oh-my-zsh运行rake命令时遇到错误:

```ruby
zsh: no matches found: live:debug:cucumber:feature[features_file]
```

##解决方案:
Add 
在zsh配置文件.zshrc中添加以下代码:
```ruby
alias rake='noglob rake'
```

##参考文献:
oh-my-zsh的[Github](https://github.com/robbyrussell/oh-my-zsh/issues/433).
