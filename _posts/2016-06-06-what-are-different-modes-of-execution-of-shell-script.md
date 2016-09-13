---
id: 137
title: What is the difference in different modes of execution of shell script ?
date: 2016-06-06T11:50:04+00:00
author: ananthulasrikar
layout: post
guid: http://srikar.io/?p=137
permalink: /what-are-different-modes-of-execution-of-shell-script/
categories:
  - Uncategorized
---
Lets say hello.sh is the sample script to execute

$ sh hello.sh
  
$ pwd/hello.sh

Above commands creates a new process and execute the script, where as below commands runs with the same process id of the shell ( Does not create another process to execute the shell)

$ . ./hello.sh
  
$source hello.sh