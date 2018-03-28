---
title: ssh &raquo; sftpCopyTo(var,profile,local,remote)
parent: ssh
tags: command ssh
comments: true
---


### Description
This command automates the copy of a local resource to a remote path via SFTP.  The remote resource, if exist, will be overwritten.

For output process via `var`, check out [Command Output Processing](index.md#command-output-processing)


### Parameters
- **var** \- the variable name that references the the outcome of this command.
- **profile** \- the profile that encapsulate the SSH connectivity and security information.
- **remote** \- the pattern which specifies the folder, file or a pattern of files.
- **local** \- the directory from which the files should be copied.


### Example
Script:<br/>
![](image/sftpCopyTo_01.png)

Output:<br/>
![](image/sftpCopyTo_02.png)


### See Also
- [`sftpCopyFrom(var,profile,remote,local)`](sftpCopyFrom(var,profile,remote,local))