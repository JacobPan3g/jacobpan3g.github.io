---
layout: post
title:  Covert Files' Encode From GBK to UTF-8 in One Time
date:   2017-09-01 15:25:01 +0800
categories: cmd
tags: shell
author: Jacob Pan
---

* content
{:toc}

To convert file encode from GBK to UTF-8

```
find <dir> -type d -exec mkdir -p <utf dir>/{} \;
find <dir> -type f -exec bash -c "iconv -f GBK -t UTF-8 {} > <utf dir>/{}" \;
```

Above, `iconv -f GBK -t UTF-8 <file> > <out file>` can convert encode. In Linux, option `-o <out file>` can instead by `>`.

`{}` in the `find -exec` command represents each line of the output of `find`.


---
> Jacob Pan [( jacobpan3g.github.io )](http://jacobpan3g.github.io)


