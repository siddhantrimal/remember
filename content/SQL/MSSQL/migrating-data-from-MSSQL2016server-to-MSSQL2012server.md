+++
title= "Migrating Data From MSSQL2016server to MSSQL2012server"
date= 2017-11-12T11:45:46+05:45
description = ""
draft= false
weight=2
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

1. Right click on Database and select `Database > Tasks`
1. Select __Generate Scripts__
1. Proceed with _Next_ until it asks you to specify how the script should be saved or published
	1. Click __Advanced__ to fine-tune your requirements
	1. ___Enable___ SQL Triggers, Indexes and Primary Key (Unique Key)
	1. Set script for Server version: ___SQL Server 2012___
	1. Set types of data to script: ___Schema and Data___
1. After fine-tuning, hit next to see a summary.
1. Click next to finish the job. Restore in the target database.
