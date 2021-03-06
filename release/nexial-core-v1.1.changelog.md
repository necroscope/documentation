---
title: nexial-core 1.1 (2018-05-??)
parent: release
tags: release nexial-core 1.1
comments: true
---


## BETA

--------------------------------------------------

### <a href="https://github.com/nexiality/nexial-core/releases/tag/nexial-core-1.1" class="external-link" target="_nexial_target">Release 1.1</a>
2018-05-??


##### Please Note
If you have test scripts created in Sentry, be sure to `bin/sentry2nexial.cmd` script for your project **PRIOR** to 
using with Nexial.


#### General
- upgrade to kotlin 1.2.31
- add check to NexialS3Helper to ensure required properties are set before use
- any "output to cloud" procedure could fail-fast due to improper/missing S3 connectivity details.
- reduce log verbosity for 3rd-party library
- added/fixed multiple unit tests
- fixed extra line creation when performing data variable refactoring via DataVariableUpdater 
- allow project.properties setting to proliferate even when no secret file is found
- enhanced `bin/` scripts so that they can be run without being in the `bin/` directory directly.
- enhanced `bin/nexial-project.sh` to support project directory not under the standard `C:\projects\` or 
  `/Users/<username>/projects` directory.
- implemented "delayed" logging strategy (LogbackUtils)
  - when nexial first started, all file-based logs are pointing to ${java.io.tmpdir}
  - when the "out" directory is determined, file-based logs are redirected to ${out}/logs directory
- implemented performance improvement on reading Excel files
  - delete "temp" Excel files ONLY if they were "dup-then-open"
  - implemented functional calls to eliminate excessive worksheet reads
- skip pause when running nexial under JUnit

[base]
- rename command `number.assertBetween(num,lower,upper)` to `number.assertBetween(num,min,max)` to improve readability
- base.verbose()
  - reduce console log for base.verbose() command (not necessary)
  - add original script param as comment when generating result of a base.verbose() call
- base.macro()
  - maintain the flow control as defined by the calling scripts.

[nexial filter]
- nexial filter now supported in flow control as well as CSV Expression (already the case since 1.0)
- nexial filter now supported in flow control as well as CSV Expression (already the case since 1.0)
- added more conditions to nexial filter. Now the complete list is:
 - >, >=, <, <=, =, !=, is/in, is not/not in, contain, start with, end with, is undefined, is defined, has length of, is empty, is not empty, match (regex)
- nexial filter now uses pipe (`|`) as separate for item listing.  item listing should be enclosed in [...] unless there's only 1 item.

[expression]
- Expression defaults to using scale of 25 (i.e. 25 decimal places) when dealing with double.  Currently applied to LIST and NUMBER.
- Expression defaults to rounding "up" when dealing with double.  Currently applied to LIST and NUMBER.
- fixed NUMBER expression when dealing with whole number.  Previous implementation converts whole number to decimal number, but this is now fixed.
- fixed EXCEL.clear where it was missing last column.
- `CSV » htmlTable`: render CSV into a HTML table.

[CSV expression]
- `removeColumns` now supports one or many columns referenced by name or index (zero-based)

[desktop]
- command desktop.scanTable(var,name) to desktop.getRowCount(var,name)

[jms]
- fixed bad reflection class in WebSphereMQJmsClientConfig.  Both BeanUtils and MethodUtils failed since they mistakenly took the MQConnectionFactory as a Map instance.

[step]
- `observe(prompt)`: fixed output to render response as second parameter.

[web]
- shipped with [geckodriver 0.20.1 (Firefox)](https://github.com/mozilla/geckodriver/blob/release/CHANGES.md#0201-2018-04-06):
	- Avoid attempting to kill Firefox process that has stopped.	
	- With the change to allow Firefox enough time to shut down in 0.20.0, geckodriver started unconditionally killing 
	  the process to reap its exit status. This caused geckodriver to inaccurately report a successful Firefox shutdown 
	  as a failure.
	- The regression should not have caused any functional problems, but the termination cause and the exit status are 
	  now reported correctly.

[ws]
- fixed `oauth()` to support OAuth response that contains multiple entitlements, products, etc. (Essentially JSON array).

