+++
title= "7zip Ultra Compression Settings"
date= 2017-11-22T06:43:47+05:45
description = ""
draft= false
# Type of content, set "slide" to display it fullscreen with reveal.js
type="page"
# Creator's Display name
creatordisplayname = "Siddhant Rimal"
# Creator's Email
creatoremail = "siddhantrimal@hotmail.com"
# LastModifier's Display name
lastmodifierdisplayname = "Siddhant Rimal"
# LastModifier's Email
lastmodifieremail = "siddhantrimal@hotmail.com"
+++

This is the best setting currently possible<sup>[1]</sup>

```
7z a -t7z -m0=lzma -mx=9 -mfb=64 -md=32m -ms=on archive.7z dir1
```

{{%expand "For ZIP though..."%}}

{{%alert theme="danger"%}}

```
7z a -mm=Deflate -mfb=258 -mpass=15 -r foo.zip C:\Path\To\Files\*
```

{{%/alert%}}

{{%/expand%}}

[1]: https://superuser.com/a/742034/640827
