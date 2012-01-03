---
layout: default
---

# "Admin" Page

Or something.

# Jekyll

This site is written in Jekyll.

* Recommend to use :rvm:
* Install Pygments
* On Arch I had to run this, (although I would try running jekyll /without/
  this hack first.

    >rvm 1.8.7 do gem uninstall liquid
    >rvm 1.8.7 do gem install liquid --version '2.2.2'

  - Make sure _config.yaml has:

    pygments: true
  
# Installation Notes for Jekyll

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

* List 2

1. Numbered List
1. Numbered List 2
1. Numbered List 2
1. Numbered List 3
     

## Examples of Markdown

[Example](markdown-examples.html)
