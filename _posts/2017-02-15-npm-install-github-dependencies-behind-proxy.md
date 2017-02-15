---
layout: post
title: "npm install and github dependencies when you are behind a proxy"
description: Quick guide to use npm install with github dependencies when you are behind a proxy
headline: 
modified: 2017-02-15
category: ["Windows Hacks",Git,GitHub,Proxy]
tags: [Git,GitHub,Proxy,Windows,Hacks]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

1. Open terminal and paste

```bash
$ git config --global url.https://github.com/.insteadOf git://github.com/
```

2. (Optional) Remove ssl verification (not-safe)

```bash
$ git config --global http.sslverify false
```