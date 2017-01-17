---
layout: post
title: "Remove Old Kernels on Fedora/CentOS/RHEL"
description: Quick guide to remove old kernels on Fedora, CentOS and RHEL
headline: 
modified: 2017-01-17
category: sysadmin
tags: [Fedora,CentOS,RHEL,Kernel,Remove]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

1. Check installed kernels

```bash
$ rpm -q kernel
kernel-2.6.32-279.el6.x86_64
kernel-2.6.32-279.2.1.el6.x86_64
kernel-2.6.32-279.5.2.el6.x86_64
kernel-2.6.32-279.9.1.el6.x86_64
```

2. Remove Old Kernels

```bash
## Install yum-utils ##
## Fedora 25/24/23/22 ##
dnf install yum-utils

## Fedora 21/20/19/18/17/16, CentOS, Red Hat (RHEL) ##
yum install yum-utils

## Package-cleanup set count as how many old kernels you want left ##
package-cleanup --oldkernels --count=2
```

3. Make amount of installed kernels permanent

```bash
$ vim /etc/dnf/dnf.conf # or /etc/yum.conf

installonly_limit=2
```