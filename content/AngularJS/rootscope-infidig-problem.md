+++
title= "Rootscope Infidig Problem"
date= 2017-12-03T16:09:38+05:45
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

![Rootscope-infidig-consoleerror][1]

This happens when you're trying to execute a js function which modifies the content inside the ViewModel as it loops. To avoid it, avoid looping inside an angular recursion.

[1]: /img/AngularJS/rootscope-infidig-consoleerror.PNG
