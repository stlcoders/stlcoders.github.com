---
layout: default
---

# Jekyll uses Maruku to render Markdown

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
     

## Listing Code

Put four spaces in front of text to get this:

    Six is a serious number
    You know I'm saying?

You can also get the same effect _inline_ with a single backtick: `println "doo"`

This is a big section of Groovy code:

{% highlight groovy %}
println "doo"
def foo = "doo".reverse()
println "Doo reversed is: ${foo}"
{% endhighlight %}

{% highlight groovy %}
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



# Felix's

Felix's has been very hospitable to the STL Coders, having helped with
powering our massive-awesome 4-year old Macbooks and providing great pizza
and reasonably priced drinks.  Their pizza does **indeed** rock.  Thanks again
to Felix's, and check them out at
[http://www.felixsrestaurant.com](http://www.felixsrestaurant.com)

# See Also (Links)

- [Cool Page and demo of Markdown]( http://www.darkcoding.net/software/markdown-quick-reference/ )


Download
--------

[Markdown 1.0.1][dl] (18 KB) -- 17 Dec 2004

[dl]: http://daringfireball.net/projects/downloads/Markdown_1.0.1.zip


Introduction
------------

Markdown is a text-to-HTML conversion tool for web writers. Markdown
allows you to write using an easy-to-read, easy-to-write plain text
format, then convert it to structurally valid XHTML (or HTML).

Thus, "Markdown" is two things: (1) a plain text formatting syntax;
and (2) a software tool, written in Perl, that converts the plain text
formatting to HTML. See the [Syntax][] page for details pertaining to
Markdown's formatting syntax. You can try it out, right now, using the
online [Dingus][].

  [syntax]: /projects/markdown/syntax
  [dingus]: /projects/markdown/dingus

The overriding design goal for Markdown's formatting syntax is to make
it as readable as possible. The idea is that a Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. While
Markdown's syntax has been influenced by several existing text-to-HTML
filters, the single biggest source of inspiration for Markdown's
syntax is the format of plain text email.

The best way to get a feel for Markdown's formatting syntax is simply
to look at a Markdown-formatted document. For example, you can view
the Markdown source for the article text on this page here:
<http://daringfireball.net/projects/markdown/index.text>

(You can use this '.text' suffix trick to view the Markdown source for
the content of each of the pages in this section, e.g. the
[Syntax][s_src] and [License][l_src] pages.)

  [s_src]: /projects/markdown/syntax.text
  [l_src]: /projects/markdown/license.text

Markdown is free software, available under a BSD-style open source
license. See the [License] [pl] page for more information.

  [pl]: /projects/markdown/license


Discussion List <a id="discussion-list" />
---------------

I've set up a public [mailing list for discussion about Markdown] [ml].
Any topic related to Markdown -- both its formatting syntax and
its software -- is fair game for discussion. Anyone who is interested
is welcome to join.

It's my hope that the mailing list will lead to good ideas for future
improvements to Markdown.

  [ml]: http://six.pairlist.net/mailman/listinfo/markdown-discuss


Installation and Requirements <a id="install" />
-----------------------------

Markdown requires Perl 5.6.0 or later. Welcome to the 21st Century.
Markdown also requires the standard Perl library module [Digest::MD5]
[md5], which is probably already installed on your server.

  [md5]: http://search.cpan.org/dist/Digest-MD5/MD5.pm


### Movable Type ###

Markdown works with Movable Type version 2.6 or later (including
Movable Type 3.0).

1.  Copy the "Markdown.pl" file into your Movable Type "plugins"
	directory. The "plugins" directory should be in the same directory
	as "mt.cgi"; if the "plugins" directory doesn't already exist, use
	your FTP program to create it. Your installation should look like
	this:

        (mt home)/plugins/Markdown.pl

2.  Once installed, Markdown will appear as an option in Movable Type's
	Text Formatting pop-up menu. This is selectable on a per-post basis:
	
	![Screenshot of Movable Type 'Text Formatting' Menu][tfmenu]
	
	Markdown translates your posts to HTML when you publish; the posts
	themselves are stored in your MT database in Markdown format.

3.	If you also install SmartyPants 1.5 (or later), Markdown will
	offer a second text formatting option: "Markdown With
	SmartyPants". This option is the same as the regular "Markdown"
	formatter, except that it automatically uses SmartyPants to create
	typographically correct curly quotes, em-dashes, and ellipses. See
	the [SmartyPants web page][sp] for more information.

4.	To make Markdown (or "Markdown With SmartyPants") your default
	text formatting option for new posts, go to Weblog Config:
	Preferences.

Note that by default, Markdown produces XHTML output. To configure
Markdown to produce HTML 4 output, see "Configuration", below.

  [sp]: http://daringfireball.net/projects/smartypants/



### Blosxom ###

Markdown works with Blosxom version 2.0 or later.

1.  Rename the "Markdown.pl" plug-in to "Markdown" (case is
    important). Movable Type requires plug-ins to have a ".pl"
    extension; Blosxom forbids it.

2.  Copy the "Markdown" plug-in file to your Blosxom plug-ins folder.
    If you're not sure where your Blosxom plug-ins folder is, see the
    Blosxom documentation for information.

3.  That's it. The entries in your weblog will now automatically be
	processed by Markdown.

4.	If you'd like to apply Markdown formatting only to certain
	posts, rather than all of them, Markdown can optionally be used in
	conjunction with Blosxom's [Meta][] plug-in. First, install the
	Meta plug-in. Next, open the Markdown plug-in file in a text
	editor, and set the configuration variable `$g_blosxom_use_meta`
	to 1. Then, simply include a "`meta-markup: Markdown`" header line
	at the top of each post you compose using Markdown.

  [meta]: http://www.blosxom.com/plugins/meta/meta.htm


### BBEdit ###

Markdown works with BBEdit 6.1 or later on Mac OS X. It also works
with BBEdit 5.1 or later and MacPerl 5.6.1 on Mac OS 8.6 or later. If
you're running Mac OS X 10.2 (Jaguar), you may need to install the
Perl module [Digest::MD5] [md5] from CPAN; Digest::MD5 comes
pre-installed on Mac OS X 10.3 (Panther).

1.  Copy the "Markdown.pl" file to appropriate filters folder in your
	"BBEdit Support" folder. On Mac OS X, this should be:

        BBEdit Support/Unix Support/Unix Filters/

    See the BBEdit documentation for more details on the location of
    these folders.

    You can rename "Markdown.pl" to whatever you wish.

2.  That's it. To use Markdown, select some text in a BBEdit document,
	then choose Markdown from the Filters sub-menu in the "#!" menu, or
	the Filters floating palette



Configuration  <a id="configuration"></a>
-------------

By default, Markdown produces XHTML output for tags with empty elements.
E.g.:

    <br />

Markdown can be configured to produce HTML-style tags; e.g.:

    <br>


### Movable Type ###

You need to use a special `MTMarkdownOptions` container tag in each
Movable Type template where you want HTML 4-style output:

    <MTMarkdownOptions output='html4'>
        ... put your entry content here ...
    </MTMarkdownOptions>

The easiest way to use MTMarkdownOptions is probably to put the
opening tag right after your `<body>` tag, and the closing tag right
before `</body>`.

To suppress Markdown processing in a particular template, i.e. to
publish the raw Markdown-formatted text without translation into
(X)HTML, set the `output` attribute to 'raw':

    <MTMarkdownOptions output='raw'>
        ... put your entry content here ...
    </MTMarkdownOptions>


### Command-Line ###

Use the `--html4tags` command-line switch to produce HTML output from a
Unix-style command line. E.g.:

    % perl Markdown.pl --html4tags foo.text

Type `perldoc Markdown.pl`, or read the POD documentation within the
Markdown.pl source code for more information.


Acknowledgements <a id="acknowledgements" />
----------------

[Aaron Swartz][] deserves a tremendous amount of credit for his feedback on the
design Markdown's formatting syntax. Markdown is *much* better thanks
to Aaron's ideas, feedback, and testing. Also, Aaron's [html2text][]
is a very handy (and free) utility for turning HTML into
Markdown-formatted plain text.

[Nathaniel Irons][], [Dan Benjamin][], [Daniel Bogan][], and [Jason Perkins][]
also deserve thanks for their feedback.

[Michel Fortin][] has ported Markdown to PHP; it's a splendid port, and highly recommended for anyone looking for a PHP implementation of Markdown.

  [Aaron Swartz]:		http://www.aaronsw.com/
  [Nathaniel Irons]:	http://bumppo.net/
  [Dan Benjamin]:		http://hivelogic.com/
  [Daniel Bogan]:		http://waferbaby.com/
  [Jason Perkins]:		http://pressedpants.com/
  [Michel Fortin]:		http://www.michelf.com/projects/php-markdown/
  [html2text]:          http://www.aaronsw.com/2002/html2text/
 
  [tfmenu]: /graphics/markdown/mt_textformat_menu.png

