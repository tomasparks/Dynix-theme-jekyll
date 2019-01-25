---
layout: post
title:  "Usenet Archiving Update"
date:   2016-08-23
categories: compression archiving dtn
tags: ZPAQ zpaq backup archive archiving dtn usenet
---
* I have given thunderbird the middle finger for download usenet articles[^1]
* I found [nget](http://nget.sourceforge.net/), its an old program, but still works :)


~~~~~~~
nget -dfim --host $url \n
 --no-decode -m yes \n
 -P '$folder' \n
 -g $group \n
 -r ""

$url is the nttp server
$folder is were you want the articles saved
$group is the group you want to download
~~~~~~~

[^1]: I still need to use it to create the group list :( 
