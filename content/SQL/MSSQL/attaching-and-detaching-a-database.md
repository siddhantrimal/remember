+++
title= "Attaching and Detaching a Database"
date= 2017-11-12T11:02:28+05:45
description = ""
draft= false
weight=1
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

Detaching
```SQL
EXEC sp_detach_db 'SMSsid', 'true'
```

Attaching
```SQL
EXEC sp_attach_db @dbname = N'SMSsid', @filename1 = N'C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\SMSsid.mdf', @filename2 = N'C:\Program Files\Microsoft SQL Server\MSSQL13.MSSQLSERVER\MSSQL\DATA\SMSsid_log.ldf'
```

{{%notice info%}}
Don't forget to stop all service instances before performing a detach.
{{%/notice%}}
