---
layout: default
title: base
tags: command base
comments: true
---


The "base" command type represents a series of common automation commands:

### Available Commands
- [`appendText(var,appendWith)`](appendText(var,appendWith))
- [`assertArrayEqual(array1,array2,exactOrder)`](assertArrayEqual(array1,array2,exactOrder))
- [`assertContains(text,substring)`](assertContains(text,substring))
- [`assertCount(text,regex,expects)`](assertCount(text,regex,expects))
- [`assertEmpty(text)`](assertEmpty(text))
- [`assertEndsWith(text,suffix)`](assertEndsWith(text,suffix))
- [`assertEqual(expected,actual)`](assertEqual(expected,actual))
- [`assertNotContains(text,substring)`](assertNotContains(text,substring))
- [`assertNotEmpty(text)`](assertNotEmpty(text))
- [`assertNotEqual(value1,value2)`](assertNotEqual(value1,value2))
- [`assertStartsWith(text,prefix)`](assertStartsWith(text,prefix))
- [`assertTextOrder(var,descending)`](assertTextOrder(var,descending))
- [`assertVarNotPresent(var)`](assertVarNotPresent(var))
- [`assertVarPresent(var)`](assertVarPresent(var))
- [`failImmediate(text)`](failImmediate(text))
- [`incrementChar(var,amount,config)`](incrementChar(var,amount,config))
- [`macro(file,sheet,name)`](macro(file,sheet,name))
- [`prependText(var,prependWith)`](prependText(var,prependWith))
- [`repeatUntil(steps,maxWaitMs)`](repeatUntil(steps,maxWaitMs))
- [`save(var,value)`](save(var,value))
- [`saveMatches(text,regex,saveVar)`](saveMatches(text,regex,saveVar))
- [`saveReplace(text,regex,replace,resultVar)`](saveReplace(text,regex,replace,resultVar))
- [`split(text,delim,saveVar)`](split(text,delim,saveVar))
- [`startRecording()`](startRecording())
- [`stopRecording()`](stopRecording())
- [`substringAfter(text,delim,saveVar)`](substringAfter(text,delim,saveVar))
- [`substringBefore(text,delim,saveVar)`](substringBefore(text,delim,saveVar))
- [`substringBetween(text,start,end,saveVar)`](substringBetween(text,start,end,saveVar))
- [`verbose(text)`](verbose(text))
- [`waitFor(waitMs)`](waitFor(waitMs))
