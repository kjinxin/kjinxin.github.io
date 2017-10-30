---
layout: post
comments: true
categories: diary
title: Hadoop-cmd
---
## Common commands
Copy to local: 
hadoop fs -get /hdfs/source/path /localfs/destination/path
hadoop fs -copyToLocal /hdfs/source/path /localfs/destination/path

delete files:
hadoop fs -rm filename
