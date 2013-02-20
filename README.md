jekyll-yuml
===========

# Jekyll yuml Plugin

[yuml][] (DIagrams Through yuml.me) is

>Create and share simple UML diagrams in your 
>blogs, wikis, forums, bug-trackers and emails.

This plugin allows you to write yuml markup within a yuml block, generate the
image file and replace the markup with the image. If the image could not be
generated, the plugin falls back to a `<pre>` block with the yuml markup.

[yuml]: http://yuml.me/


## Installation

Install yuml downloader from https://github.com/wandernauta/yuml on a path in your system

/usr/local/bin works just fine

and place the `yuml.rb` plugin in your sites `_plugins` directory.


## Usage

Once installed `yuml` blocks with yuml markup can be inserted:

    {% yuml %}
    [note:note1 goes here{bg:cornsilk}]
    [a]-[b]
    [b]-[c]
    {% endyuml %}

When re-generating the site, the generated image is inserted into the page:

![yuml output](https://github.com/kikitux/jekyll-yuml/blob/master/sample.png?raw=true)

yuml options can be passed through the tag:

    {% yuml -v -s plain %}
    [note:text]
    {% endyuml %}

_Note_: If you haven't auto-regenerate enabled, the images might not get copied.
In this case you have to run a second Jekyll pass. 
