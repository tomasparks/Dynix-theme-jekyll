---
layout: post
title:  "Rhythmbox scrobbling notes system"
date:   2017-12-31
icons: indieweb, scrobble, scrobbling, music, notes, note
syndication:
- https://news.indieweb.org/en
---

I've just written [Rhythmbox](https://en.wikipedia.org/wiki/Rhythmbox) scrobbling system for my notes

the php script takes rhythmdb.xml located at /home/tom/.local/share/rhythmbox/ and creates a yml file

{% github_sample_ref /tomasparks/website/98c350c7f0f100a08637c89f0475b01b8d4c5b3d/_notes/local/2017/r12.yml 0 4 %}
{% highlight yaml %}
{% github_sample /tomasparks/website/98c350c7f0f100a08637c89f0475b01b8d4c5b3d/_notes/local/2017/r12.yml 0 4 %}
{% endhighlight %}

### Source Code ###

{% github_sample_ref /tomasparks/website/c2215b2476f200f4e8d289fa55268b716cad07a9/_rake/rhythmdb2notes.php %}
{% highlight php %}
{% github_sample /tomasparks/website/c2215b2476f200f4e8d289fa55268b716cad07a9/_rake/rhythmdb2notes.php %}
{% endhighlight %}

i've updated and cleaned notes.php

{% github_sample_ref /tomasparks/website/98c350c7f0f100a08637c89f0475b01b8d4c5b3d/_rake/notes.php %}
{% highlight php %}
{% github_sample /tomasparks/website/98c350c7f0f100a08637c89f0475b01b8d4c5b3d/_rake/notes.php %}
{% endhighlight %}

