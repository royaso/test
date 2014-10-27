
-   -   [Menu](#)

-   

-   [Screencasts](/episodes)
-   [Articles](/blog)
-   [Categories](/categories)
-   [Training](/training)
-   [Publications](/publications)
-   [Subscribe](/subscribe)

-   Vimcasts
-   [Screencasts](/episodes)
-   [Articles](/blog)
-   [Categories](/categories)
-   [Training](/training)
-   [Publications](/publications)
-   [Subscribe](/subscribe)
-   

[VimCasts.org](/ "Go to Vimcasts.org homepage")
===============================================

Check out my new project: [Peer to Peer](http://peertopeer.io/) - watch
how experts solve tech problems.

[Learn more](http://peertopeer.io/)

Check out my new project: [Peer to Peer](http://peertopeer.io/) - watch
how experts solve tech problems.

[Learn more](http://peertopeer.io/)

Operating on search matches using gn {.title}
------------------------------------

\#63 {.episode_number}
----

Run time: 4:35

Feb 11, '14

Feb 11, 2014

The `gn` command (introduced in Vim 7.4) makes it easy to operate on
regions of text that match the current search pattern. It’s especially
useful when used with a regex that matches text regions of variable
length.

#### Download

-   [OGG](http://media.vimcasts.org/videos/63/gn-command.ogv) 6.5 MB
-   [Quicktime](http://media.vimcasts.org/videos/63/gn-command.m4v) 9.6
    MB

Run time: 4:35

[Read transcript](/transcripts/63/en/)

[Shownotes](#shownotes)

Here’s what Vim’s documentation has to say about the `gn` command
([`:help gn`](http://vimhelp.appspot.com/visual.txt.html#gn)):

> Search forward for the last used search pattern, like with `n`, and
> start Visual mode to select the match. If the cursor is on the match,
> visually selects it. If an operator is pending, operates on the match.

You know how pressing `n` tells Vim to jump to the start of the next
match? Well, `gn` tells Vim to start visual mode and *select the next
match*. When used in this fashion, the `gn` command makes Vim’s search
behave like most graphical text editors, where the search command
selects the current match. As you might expect, the `gN` command lets
you visually select the previous match.

I find the `gn` command especially useful in [Operator-pending
mode](http://vimdoc.sourceforge.net/htmldoc/intro.html#Operator-pending-mode).
For example, `dgn` will delete the next match, `cgn` will do the same
then switch to Insert mode, `gUgn` will convert the next match to
uppercase characters. Look up
[`:h operator`](http://vimhelp.appspot.com/motion.txt.html#operator) for
more ideas.

### Using `gn` with the dot command

Suppose that we have a document containing several occurrences of the
word ‘Normal’ and we’d like to change each occurrence to ‘Visual’. We
can run `/Normal` to search for the word ‘Normal’, then type
`cgnVisual<Esc>` to change the next match to the word ‘Visual’. You’re
probably familiar with the technique of pressing `n.` to repeat the
change for each subsequent match. In [Practical
Vim](http://pragprog.com/book/dnvim/practical-vim), I call this pattern
of usage *The Dot Formula*. It lets us use two keystrokes per change.

In this context, we can do better. The dot command repeats the last
change, which is equivalent to typing `cgnVisual<Esc>`. We could
translate that into plain English as: “change the next match”. We don’t
have to press `n.` because `.` does the job by itself. That makes it
just one keystroke per change!

### You need Vim 7.4.110 to use `gn`

You can use the `gn` command if you are running Vim 7.4 at [patch level
110](http://ftp.vim.org/pub/vim/patches/7.4/7.4.110) or greater.

The `gn` feature was first introduced by Christian Brabandt in Vim 7.3
with patch [610](http://ftp.vim.org/pub/vim/patches/7.3/7.3.610), then
the functionality was refined with patches
[625](http://ftp.vim.org/pub/vim/patches/7.3/7.3.625),
[636](http://ftp.vim.org/pub/vim/patches/7.3/7.3.636),
[645](http://ftp.vim.org/pub/vim/patches/7.3/7.3.645),
[647](http://ftp.vim.org/pub/vim/patches/7.3/7.3.647), and
[1275](http://ftp.vim.org/pub/vim/patches/7.3/7.3.1275). The feature was
made widely available in Vim 7.4, but if you are running a version less
than patch level 110 then the `gUgn` command demonstrated in this video
won’t work.

### Practical Vim - tip 84

In the 1st edition of [Practical
Vim](http://pragprog.com/book/dnvim/practical-vim), tip 84 goes over a
different approach for making this same kind of change, which is nowhere
near as tidy! When I wrote this edition, the `gn` feature hadn’t yet
been added to Vim. I’ll have to revise this tip when the time comes to
write a new edition of Practical Vim.

If you’re stuck on an older version of Vim, note that you can get
similar functionality by installing the
[textobj-lastpat](https://github.com/kana/vim-textobj-lastpat) plugin by
Kana Natsuno. I used to consider this to be an essential plugin, but
don’t now that the `gn` command is built-in to Vim.

### Further reading

-   [`:help gn`](http://vimhelp.appspot.com/visual.txt.html#gn)
-   [`:help operator`](http://vimhelp.appspot.com/motion.txt.html#operator)
-   [`:help .`](http://vimdoc.sourceforge.net/htmldoc/repeat.html#.)
-   [Practical Vim](http://pragprog.com/book/dnvim/practical-vim), tip
    84: Operate on a complete search match

[Comments](#comments)

Like this video? Spread the word!

-   [](http://twitter.com/home?status=Operating%20on%20search%20matches%20using%20gn%20http://vimcasts.org/episodes/operating-on-search-matches-using-gn/)
    twitter
-   [](https://plus.google.com/share?url=Operating%20on%20search%20matches%20using%20gn%20http://vimcasts.org/episodes/operating-on-search-matches-using-gn/)
    google+
-   [](https://www.facebook.com/sharer/sharer.php?u=http://vimcasts.org/episodes/operating-on-search-matches-using-gn/)
    facebook
-   [](mailto:?subject=Operating%20on%20search%20matches%20using%20gn&body=http%3A%2F%2Fvimcasts.org%2Fepisodes%2Foperating-on-search-matches-using-gn%2F)
    email

[«
Previous](/episodes/creating-mappings-that-accept-a-count/ "Creating mappings that accept a count")
[Next
»](/episodes/using-external-filter-commands-to-reformat-html/ "Using external filter commands to reformat HTML")

* * * * *

### Browse similar content

-   [](/categories/editing-text)

    #### Editing text

    15 screencasts

-   [](/categories/visual-mode)

    #### Visual mode

    8 screencasts

-   [](/categories/search)

    #### search

    7 screencasts

-   [](/categories/regular-expressions)

    #### Regular expressions

    7 screencasts

-   [](/categories/repetition)

    #### Repetition

    6 screencasts

* * * * *

Level-up your Vim
-----------------

### Training

Boost your productivity with a [Vim training class](/training). Join a
public class, or book a private session for your team.

> Drew hosted a private Vim session for the shopify team that was one of
> the best workshops I have ever attended.
>
> John Duff, Director of Engineering at Shopify

### Publications

Make yourself a faster and more efficient developer with the help of
[these publications](/publications), including Practical Vim (Pragmatic
Bookshelf 2012), which has over 50 five-star reviews on Amazon.

> After reading it, I've switched to vim as my default editor on a daily
> basis with no regrets. **★★★★★**
>
> Javier Collado

![](/images/practical-vim/practical-vim-cover-550.jpg)

### Learn to use Vim efficiently in your Ruby projects

In association with Thoughtbot, one of the most well respected Rails
consultancies in the world, I've produced a series of screencasts on how
to make navigating your Ruby projects with Vim ultra-efficient. Along
the way, you’ll also learn how to make Ruby blocks a first-class text
object in Vim. This lets you edit Ruby code at a higher level of
abstraction. [Available to buy from
Thoughtbot.](https://learn.thoughtbot.com/products/21-navigating-ruby-files-with-vim).

![](/images/thoughtbot-robot-logo.png)

* * * * *

-   [About](/about)
-   [Announcements](/announcements)
-   [Leave a tip](/tipjar)

Vimcasts.org established MMX
=======
2014年 10月 26日 星期日 16:35:25 CST
2014年 10月 27日 星期一 09:14:22 CST
