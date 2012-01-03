---
layout: default
---

# STL Coders uses Jekyll and Markdown

[ Maruku ]( http://maruku.rubyforge.org/maruku.html )

Maruku implements more features than the standard Markdown.

The following page is a combo of standard Markdown and the 
other cool stuff that Maruku puts in.

Kinda _big_ this is _italics_

This is also *italics* -- kinda lame, should be **bold** in my opinion.

* List 1

    * Subitem 1

    * Subitem 2

    * Subitem 3

    * Subitem 4

    1. List


* List 2

    1. Numbered Sublists have to be done explicitly? 

    2. Numbered List 2

    1. Numbered List 3
     

## Listing Code

{% highlight ruby %}
def awesome
  "for real. I know."
end
{% endhighlight %}

Put four spaces in front of text to get this:

    Six is a serious number
    You know I'm saying?

You can also get the same effect _inline_ with a single backtick: `println "doo"`

This is a big section of Clojure code:

{% highlight clojure %}
(+ 2 2)
{% endhighlight %}

{% highlight ruby %}
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
{% endhighlight %}


## "Meeting" Notes

At STLCoders, we aim to _code_

This is quoted text:

> This is quoted text Lorem ipsum dolor sit amet, consectetur adipisicing elit,
> sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
> minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
> commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit
> esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat
> cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est
> laborum 


# See Also (Links)

- [Cool Page and demo of Markdown]( http://www.darkcoding.net/software/markdown-quick-reference/ )

