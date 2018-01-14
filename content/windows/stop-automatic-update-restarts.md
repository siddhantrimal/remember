+++
title= "Stop Automatic Update Restarts"
date= 2018-01-14T10:00:06+05:45
description = "How to stop Windows 10 from automatically executing scheduled restarts for updates"
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

It can be a real PITA to have been working on something when windows suddenly starts restarting automatically because an internal update has been scheduled. Active hours is another unforgiving pain as Microsoft seems to have made it for robots rather than us puny humans - It absolutely does not let you update outside of work hours. If you have been suffering for long, worry not, it ends here.

#### Algorithm to disable automatically scheduled restarts for updates in  Windows 10.

__STEP-1__

* `Task Scheduler > UpdateOrchestrator > Reboot > DISABLE`

__STEP-2__

* Goto `C:\Windows\System32\Tasks\Microsoft\Windows\UpdateOrchestrator`

* Rename `Reboot` to `Reboot.Sid`

* Create an empty new folder and rename it as `Reboot`

__STEP-3__

* Rejoice as automatic updates that mess with your life stop forever!

> [Source](http://cod3r.blogspot.com/2017/03/StopSpontaneousUpdateRestartsInWindows10.html)
