---
layout: post
title: AWS SDK - GetLogEvents does not return all LogEvents
---

A (seemingly) undocumented feature of CloudWatch's GetLogEvents operation is that, if you don't set a startTime in your command request, you will potentially NOT start reading the log events of your LogStream from the start.

This doesn't seem too silly to me, given the indexing issues that come with such systems (that are designed to handle huge amount of data). What seems silly to me, though, is to not obviously document this behavior.

If you find yourself not retrieving all logs from a LogStream using the GetLogEvents command (e.g. via a GetLogEventsCommand when using the AWS JavaScript SDK), you should set the startTime parameter in the request body of your GetLogEventsCommand. I personally set it to the timestamp of the first event of the stream (which you can find the firstEventTimestamp field of a LogStream).

<!--more-->