---
layout: post
title: "Install Java Without admin Privileges"
description: Quick guide to Install Java Without admin Privileges
headline: 
modified: 2017-02-15
category: ["Windows Hacks"]
tags: [Windows,Hacks,Java]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

1. Donwload Windows JDK at Oracle's Web Site (e.g: jdk-8u121-windows-x64.exe)

2. Install 7-zip portable

3. Extract with 7-zip the files from jdk-8u121-windows-x64.exe to C:\Java (or wherever you want)

4. With the command line, go to the folder you extracted the .exe files and execute cab extraction

    - cd C:\Java\.rsrc\1033\JAVA_CAB10
    - extract32 111
	
5. A file named tools.zip will be created, then unzip it

6. Execute the commands

    - cd C:\Java\.rsrc\1033\JAVA_CAB10\java
    - for /r %x in (*.pack) do .\bin\unpack200 -r "%x" "%~dx%~px%~nx.jar" (this will convert all .pack files into .jar files)

7. Setup JAVA_HOME and PATH manually