+++
title= "Auto IP Setter"
date= 2017-11-16T14:38:05+05:45
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

Copy/Paste the following script and name it as `autoIPchanger.bat`(___not___ `.txt`) as you save it.
{{%notice info%}}
There's a small `copy-to-clipboard` button on the top-right side of every code snippet.
{{%/notice%}}

	@echo off
	REM GHAR
	 CLS
	 ECHO.
	 ECHO =============================
	 ECHO AUTO IP CONFIGURATOR
	 ECHO =============================
	REM ----------PRESET SETTINGS-------
	set varIP=10.0.80.50
	REM WRITE YOUR COMPUTER IP ABOVE
	set varDefaultGateway=10.0.80.1
	set varSubnetMask=255.255.255.192
	set varPrimaryDNS=4.2.2.2
	set varSecondaryDNS=8.8.8.8
	REM --------------------------------
	:init
	 setlocal DisableDelayedExpansion
	 set cmdInvoke=1
	 set winSysFolder=System32
	 set "batchPath=%~0"
	 for %%k in (%0) do set batchName=%%~nk
	 set "vbsGetPrivileges=%temp%\OEgetPriv_%batchName%.vbs"
	 setlocal EnableDelayedExpansion
	:checkPrivileges
	  NET FILE 1>NUL 2>NUL
	  if '%errorlevel%' == '0' ( goto gotPrivileges ) else ( goto getPrivileges )
	:getPrivileges
	  if '%1'=='ELEV' (echo ELEV & shift /1 & goto gotPrivileges)
	  ECHO.
	  ECHO Set UAC = CreateObject^("Shell.Application"^) > "%vbsGetPrivileges%"
	  ECHO args = "ELEV " >> "%vbsGetPrivileges%"
	  ECHO For Each strArg in WScript.Arguments >> "%vbsGetPrivileges%"
	  ECHO args = args ^& strArg ^& " "  >> "%vbsGetPrivileges%"
	  ECHO Next >> "%vbsGetPrivileges%"
	  if '%cmdInvoke%'=='1' goto InvokeCmd 
	  ECHO UAC.ShellExecute "C:\Users\Siddhant\Desktop\auto-IP-changer-master\autoIPsetter.bat", args, "", "runas", 1 >> "%vbsGetPrivileges%"
	  goto ExecElevation
	:InvokeCmd
	  ECHO args = "/c """ + "C:\Users\Siddhant\Desktop\auto-IP-changer-master\autoIPsetter.bat" + """ " + args >> "%vbsGetPrivileges%"
	  ECHO UAC.ShellExecute "%SystemRoot%\%winSysFolder%\cmd.exe", args, "", "runas", 1 >> "%vbsGetPrivileges%"
	:ExecElevation
	 "%SystemRoot%\%winSysFolder%\WScript.exe" "%vbsGetPrivileges%" %*
	 exit /B
	:gotPrivileges
	 setlocal & cd /d %~dp0
	 if '%1'=='ELEV' (del "%vbsGetPrivileges%" 1>nul 2>nul  &  shift /1)
	 ::::::::::::::::::::::::::::
	 ::START
	 ::::::::::::::::::::::::::::
	 REM Run shell as admin
	@echo off
	REM LABA
	for /F "usebackq skip=1 tokens=2" %%a in ("%~F0") do set "BOOLEAN_VALUE=%%a" & goto continue
	:continue
	TITLE Automatically setting IP for %BOOLEAN_VALUE%
	ECHO BOOLEAN_VALUE=%BOOLEAN_VALUE%
	IF %BOOLEAN_VALUE% EQU GHAR GOTO 2
	:1
	netsh interface ip set address name="Ethernet" static %varIP% %varSubnetMask% %varDefaultGateway%
	netsh interface ip set dnsservers name="Ethernet" source=static address=%varPrimaryDNS% register=primary
	netsh interface ip add dns name="Ethernet" address=%varSecondaryDNS%
	GOTO UPDATE_BOOLEAN_VALUE
	:2
	netsh interface ipv4 set address name="Ethernet" source=dhcp
	netsh interface ip set dnsservers name="Ethernet" source=dhcp
	:UPDATE_BOOLEAN_VALUE
	REM The code to change the BOOLEAN_VALUE i.e. a toggler
	if %BOOLEAN_VALUE% equ GHAR (set "BOOLEAN_VALUE=LABA") else set "BOOLEAN_VALUE=GHAR"
	(
	echo @echo off
	echo REM %BOOLEAN_VALUE%
	for /F "usebackq skip=2 delims=" %%a in ("%~F0") do echo %%a
	) > _new_.bat
	move /Y _new_.bat "%~F0" > NUL
	if %BOOLEAN_VALUE% equ GHAR (set "BOOLEAN_VALUE=LABA") else set "BOOLEAN_VALUE=GHAR"
	echo Setting applied for:: %BOOLEAN_VALUE%
	pause
	exit
	REM ::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
	REM :: Get here: https://github.com/siddhantrimal/auto-IP-changer
	REM :: built with Elevate.cmd - Version 4
	REM :: Automatically check & get admin rights
	REM :: referenced from: http://stackoverflow.com/a/12264592/5040900
	REM :: modified by Siddhant-Rimal 03-16-2017 v.1.0
	REM :: enhanced by Siddhant-Rimal 11-16-2017 v.1.1
	REM ::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::


{{%alert%}}
{{<icon name="fa-github" size="xx-large">}}
[This is available on github ](https://github.com/siddhantrimal/auto-IP-changer)
{{%/alert%}}

{{%expand "Click to see older version"%}}

{{%panel theme="danger" footer="03-16-2017 v.1.0"%}}

	@echo off
	REM GHAR
	 CLS
	 ECHO.
	 ECHO =============================
	 ECHO AUTO IP CONFIGURATOR
	 ECHO =============================
	REM ----------PRESET SETTINGS-------
	set varIP=10.0.80.50
	REM WRITE YOUR COMPUTER IP ABOVE
	set varDefaultGateway=10.0.80.1
	set varSubnetMask=255.255.255.192
	REM --------------------------------
	:init
	 setlocal DisableDelayedExpansion
	 set cmdInvoke=1
	 set winSysFolder=System32
	 set "batchPath=%~0"
	 for %%k in (%0) do set batchName=%%~nk
	 set "vbsGetPrivileges=%temp%\OEgetPriv_%batchName%.vbs"
	 setlocal EnableDelayedExpansion
	:checkPrivileges
	  NET FILE 1>NUL 2>NUL
	  if '%errorlevel%' == '0' ( goto gotPrivileges ) else ( goto getPrivileges )
	:getPrivileges
	  if '%1'=='ELEV' (echo ELEV & shift /1 & goto gotPrivileges)
	  ECHO.
	  ECHO Set UAC = CreateObject^("Shell.Application"^) > "%vbsGetPrivileges%"
	  ECHO args = "ELEV " >> "%vbsGetPrivileges%"
	  ECHO For Each strArg in WScript.Arguments >> "%vbsGetPrivileges%"
	  ECHO args = args ^& strArg ^& " "  >> "%vbsGetPrivileges%"
	  ECHO Next >> "%vbsGetPrivileges%"
	  if '%cmdInvoke%'=='1' goto InvokeCmd 
	  ECHO UAC.ShellExecute "!batchPath!", args, "", "runas", 1 >> "%vbsGetPrivileges%"
	  goto ExecElevation
	:InvokeCmd
	  ECHO args = "/c """ + "!batchPath!" + """ " + args >> "%vbsGetPrivileges%"
	  ECHO UAC.ShellExecute "%SystemRoot%\%winSysFolder%\cmd.exe", args, "", "runas", 1 >> "%vbsGetPrivileges%"
	:ExecElevation
	 "%SystemRoot%\%winSysFolder%\WScript.exe" "%vbsGetPrivileges%" %*
	 exit /B
	:gotPrivileges
	 setlocal & cd /d %~dp0
	 if '%1'=='ELEV' (del "%vbsGetPrivileges%" 1>nul 2>nul  &  shift /1)
	 ::::::::::::::::::::::::::::
	 ::START
	 ::::::::::::::::::::::::::::
	 REM Run shell as admin
	@echo off
	REM LABA
	for /F "usebackq skip=1 tokens=2" %%a in ("%~F0") do set "BOOLEAN_VALUE=%%a" & goto continue
	:continue
	ECHO BOOLEAN_VALUE=%BOOLEAN_VALUE%
	IF %BOOLEAN_VALUE% EQU GHAR GOTO 2
	:1
	netsh interface ip set address name="Ethernet" static %varIP% %varSubnetMask% %varDefaultGateway%
	GOTO UPDATE_BOOLEAN_VALUE
	:2
	netsh interface ipv4 set address name="Ethernet" source=dhcp
	:UPDATE_BOOLEAN_VALUE
	REM The code to change the BOOLEAN_VALUE i.e. a toggler
	if %BOOLEAN_VALUE% equ GHAR (set "BOOLEAN_VALUE=LABA") else set "BOOLEAN_VALUE=GHAR"
	(
	echo @echo off
	echo REM %BOOLEAN_VALUE%
	for /F "usebackq skip=2 delims=" %%a in ("%~F0") do echo %%a
	) > _new_.bat
	move /Y _new_.bat "%~F0" > NUL
	if %BOOLEAN_VALUE% equ GHAR (set "BOOLEAN_VALUE=LABA") else set "BOOLEAN_VALUE=GHAR"
	echo Setting applied for:: %BOOLEAN_VALUE%
	pause
	exit
	REM ::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::
	REM :: Get here: https://github.com/siddhantrimal/auto-IP-changer
	REM :: built with Elevate.cmd - Version 4
	REM :: Automatically check & get admin rights
	REM :: referenced from: http://stackoverflow.com/a/12264592/5040900
	REM :: modified by Siddhant-Rimal 03-16-2017
	REM ::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::


{{%/panel%}}

{{%/expand%}}