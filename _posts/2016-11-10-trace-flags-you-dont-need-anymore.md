---
layout: post
title: Trace flags that you don't need any more
published: true
---
SQL2016 has done away with trace flags so you won't be needing any of these in future. These are the trace flags I use on all installations and why.


-T1117 Grow All Files in a FileGroup Equally. Very important for tempdb. SQL2016 requires setting AUTOGROW_ALL_FILES per filegroup in user databases. Turned on by default for tempdb in SQL2016.

-T1118 Full Extents Only. Important for tempdb, helps with SGAM contention. SQL2016 Database setting MIXED_PAGE_ALLOCATION OFF which is the new default behaviour.

-T2371 dynamic auto update statistics threshold. SQL2016 standard behaviour, no longer configurable.

-T2562 DBCC CHECKDB "batch" mode. OK this one sneaked through, it's still applicable to 2016. Let's hope somebody enabled it for us on Azure huh?

-T4199 Query optimiser hotfixes. Enabled by default in SQL2016 as a database level setting QUERY_OPTIMIZER_HOTFIXES for compatibility mode 130.


I find the easiest way to set these flags is to go into SQL Configuration Manager, open up properties for the SQL Server and go to the Startup Parameters Tab. They have to be added one-by-one.
