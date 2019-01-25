---
layout: post
title:  "custom indieweb note system"
date:   2017-12-26
icons: indieweb, notes, note
syndication: 
- https://news.indieweb.org/en
---

I am curently writing a custom indieweb [note](https://indieweb.org/note) system for my webiste, my requirements are different to most/all indieweb implementation as I need three different way of creating notes Text-editor, Browser and Offline

### text-editor ###

I use a text editor to add entries to [YAML](https://en.wikipedia.org/wiki/YAML) file

{% github_sample_ref /tomasparks/website/07641044ff952012604941d9fb8f759365ba6280/_notes/local/2017/10.yml 0 4 %}
{% highlight yaml %}
{% github_sample /tomasparks/website/07641044ff952012604941d9fb8f759365ba6280/_notes/local/2017/10.yml 0 4 %}
{% endhighlight %}

### web Browser / mircopub ###

Unimplementated because I have not found a browser plugin/addon that support my wishlist[^2] yet, the closest i've found is [Omnibear](https://indieweb.org/Omnibear)

### Offline / CSV ###

I use a PDA[^1], when I away from my computers, the PDA has good database software witch can export [CSV](https://en.wikipedia.org/wiki/Comma-separated_values) files

{% github_sample_ref /tomasparks/website/07641044ff952012604941d9fb8f759365ba6280/_notes/pda/2017/12.csv  0 4 %}
{% highlight csv %}
{% github_sample /tomasparks/website/07641044ff952012604941d9fb8f759365ba6280/_notes/pda/2017/12.csv 0 4 %}
{% endhighlight %}

### data format ###

I am using the SQL format to demonstrate the data format

{% highlight SQL %}
CREATE TABLE data (
	date CHAR(255),
    type CHAR(255),
    tags CHAR(255),
    url CHAR(255),
    message TEXT
);
{% endhighlight %}

 * type is for the [post type](https://indieweb.org/posts#Kinds_of_Posts) excluding articles
 * tags are a csv encoded key:value pairs
 * url are for [Uniform Resource Identifier](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier), I am currently using CSV encoded key:value pairs, I am looking at using the [Url Query](https://en.wikipedia.org/wiki/Query_string) format in the future

NOTE: data fomrat MUST be human editable
 * No [url encoding](https://en.wikipedia.org/wiki/Percent-encoding)
 
### Source Code ###

{% github_sample_ref /tomasparks/website/07641044ff952012604941d9fb8f759365ba6280/_rake/notes.php %}
{% highlight php %}
{% github_sample /tomasparks/website/07641044ff952012604941d9fb8f759365ba6280/_rake/notes.php %}
{% endhighlight %}

[^1]: It's as psion 5mx Pro
[^2]: Support like/comments, UPDATE: I found [own your comments](https://github.com/barnabywalters/own-your-comments) and [IndieWeb Reply Browser-Extension](https://github.com/barnabywalters/IndieWeb-Reply-Browser-Extension), but they seam like they have code rot :(
