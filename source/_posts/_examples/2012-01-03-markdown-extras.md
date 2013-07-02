---

layout: post
title: Markdown Extras
date: 2012-01-03 15:56
author: Git User
categories: [demo, markdown]
summary: Some non-standard markdown extensions

---


Various non-standard implementations of markdown have added their own extensions to the
syntax - which can be useful where compatibility is less of an issue. Here's some that
work on this site.

<!-- more -->


## Common Extensions

Empty brackets after a reference link can be omitted - so long as the meaning is
unambiguous.  e.g. instead of [github][], you can use [github].

[github]: http://github.com

Similar to reference style links, are footnote links[^moreinfo].

[^moreinfo]: here is some more info, that will appear at the bottom of the page.

Automatic creation of [header IDs] makes it easy to link to various
[sections](#common-extensions) within your post.

[header IDs]: http://kramdown.rubyforge.org/converter/html.html#auto-ids

Tables can be created easily, additional formatting such as text alignment
[can also be used](http://kramdown.rubyforge.org/quickref.html#tables).

|header 1|header 2|header 3|
|--------|--------|-------:|
| data 1 | data 2 | data 3 |


## Kramdown

> [kramdown] is the dialect and renderer of markdown used for the site. It adds many
> advanced extensions, some of which are demonstrated here.

[kramdown]: http://kramdown.rubyforge.org/

Attributes allow for modifying [block] and [span] level elements.

[block]: http://kramdown.rubyforge.org/quickref.html#block-attributes
[span]: http://kramdown.rubyforge.org/quickref.html#inline-attributes

One use of attributes is to append class names to elements:

![CentredImage](https://github.com/images/icons/emoji/octocat.png){:.center}

Another is to add custom formatting without using HTML, such as *underline*{:.underline},
*strikeout*{: style="text-decoration: line-through"}, and *colour*{: style="color: red"}.

A [table of contents] can be generated by using the `toc` reference. Normally this would
be used at the start of a long post with lots of headings.

* This text will be replaced with the table of contents.
{:toc}

[table of contents]: http://kramdown.rubyforge.org/converter/html.html#toc


### Header with an explicit header ID  {#manual-id}

The ID that's automatically created for headers may not always be preferred, especially if
the header is fairly long.

Definition lists have a syntax that's similar to normal lists:

term to define
: a definition
: an alternate definition


## More Examples

See the [examples] folder for more uses of markdown and octopress syntax.

[examples]: https://github.com/snhack/snhack.github.com/tree/source/source/_posts/_examples