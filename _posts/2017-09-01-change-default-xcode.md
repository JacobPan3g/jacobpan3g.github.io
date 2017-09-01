---
layout: post
title:  Change System Default Xcode in Mac
date:   2017-09-01 15:13:01 +0800
categories: mac
tags: xcode
author: Jacob Pan
---

* content
{:toc}

Show the default xcode in mac os x:
```
$ xcode-select -p
``` 

Change system default xcode
```
# xcode-select -switch /Applications/Xcode.app
```

If there are more than one xcode installed in mac os x, the second one will be named "xcode 2". Sometimes, it'll raise some errors because the " "(space) in the name. 

For instance, to build libnet, I followed the `BUILD-FROM-GIT.txt` at the top of project. Because my default xcode is named "xcode 2", it throw an error as
`/bin/sh: /Applications/Xcode: No such file or directory`. After I switched to "xcode" using the cmd above, the build process success.


---
> Jacob Pan [( jacobpan3g.github.io/ )](http://jacobpan3g.github.io)
