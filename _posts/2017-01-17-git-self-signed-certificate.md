---
layout: post
title: "Git and Self Signed Certificates"
description: Quick guide use git with self signed certificates
headline: 
modified: 2017-01-17
category: [sysadmin, git]
tags: [git,self signed,certificates]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

1. Single repo

```bash
$ git -c http.sslVerify=false clone https://domain.com/path/to/git
```

2. Global repos

```bash
$ git config --global http.sslVerify false
```

3. More details check

http://stackoverflow.com/questions/11621768/how-can-i-make-git-accept-a-self-signed-certificate