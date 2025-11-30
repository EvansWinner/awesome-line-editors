# Awesome Line Editors

(and some not-so-awesome ones)

(For some meaning of "awesome," anyway. "Interesting," might be more accurate.)
(and also for various meanings of "line editor")

**or, Making Teletype Tech Useful Again!**


## Praeliminaria

**THIS IS A WORK IN PROGRESS AND JUST STARTED. MORE TO COME. STAY TUNED.**

**→&nbsp;[Skip Intro](#the-editors)&nbsp;←**

![The Sacred Hermetic Order of ed(1)](img/edPunchCard.png)

### Table of Contents
- [Praeliminaria](#praeliminaria)
  - [Advertisement](#advertisement)
  - [I can't be bothered to watch the videos, or I still don't get the point](#i-cant-be-bothered-to-watch-the-videos-or-i-still-dont-get-the-point)
    - [First, distraction-free -- hey, a bird!](#first-distraction-free----hey-a-bird)
    - [Thumb typing](#thumb-typing)
    - [And then the usual excuse](#and-then-the-usual-excuse)
    - [Oh, and Suckless](#oh-and-suckless)
    - [Finally, one weird thing](#finally-one-weird-thing)
  - [Some quick notes first](#some-quick-notes-first)
    - [Line editors, context editors, character editors, oh my!](#line-editors-context-editors-character-editors-oh-my)
    - [How do I learn to use a line editor?](#how-do-i-learn-to-use-a-line-editor)
  - [Some general external resources](#some-general-external-resources)
  - [Disclaimers](#disclaimers)

- [The Editors](#the-editors)
  - [ECCE](#ecce) 
  - [EDIT](#edit)
  - [EDLIN](#edlin)
  - [Edbrowse](#edbrowse)
  - [Teco](#teco)
  - [ed](#ed)
  - [edam](#edam)
  - [em](#em)
  - [ex](#ex)
  - [led 1](#led-1)
  - [led 2](#led-2)
  - [qed](#qed)
  - [sam -d](#sam--d)
  - [sued](#sued)
- [Appendices](#appendices)
  - [Appendix A: Honorable Mentions](#appendix-a-honorable-mentions)
    - [ALE](#ale)
    - [ATTO](#atto)
    - [ED.COM](#edcom)
    - [led 3](#led-3)
  - [Appendix B: Mainly of Historical Interest](#appendix-b-mainly-of-historical-interest)
  - [Appendix C: Others](#appendix-c-others)
    - [buup](#buup)
    - [cmd-line-text-editor](#cmd-line-text-editor)
    - [ed clone in go](#ed-clone-in-go)
    - [edd](#edd)
    - [edlin-clone](#edlin-clone)
    - [edlin-text-editor](#edlin-text-editor)
    - [Fed](#fed)
- [Colophon](#colophon)

And also, "character editors" and "context editors" as well.

And no, I'm not talking about

- the people who will fix your memoirs line-by-line for a fee; or
- those command line editing functions like readline or
  [linenoise](https://github.com/antirez/linenoise)
  that are for editing a single line of input at your terminal shell.

**I am talking about text editors of yore**, like the Unix ``ed(1)`` editor,
which operated in terms of lines (or, yes, like Teco,
which theoretically operated in terms of individual characters)
and **which were originally designed to work on a Teletext terminal**
(or Teletype machine? What's the difference?) **with a
printer printing one line at a time like God intended**, instead of
a video display, like these
new-fangled modern computers for lazy people.
I'm talking about those paragons of the *conversational user interface*,
the REPLs of text editing: line editors.


### Advertisement 

Before anything else,
since a YouTube video is worth a thousand ill-chosen words,
check out a couple of impressive demos.
There are lots of other videos of people using line editors on YouTube
(almost all using the Unix ``ed(1)`` editor)
but most were done by college students
who just discovered ``ed`` yesterday and don't know anything about it.
They're mostly kind of embarrassing, frankly (the videos, I mean).
But these below are the two cool ones I've found
because they were done by legit wizards: 

 - [Ed text editor](https://www.youtube.com/watch?v=BNYpmLH6IjQ)&nbsp;![Youtube](img/youtube.png) 
 - [Lambda Island 40. The Ultimate Dev Setup](https://www.youtube.com/watch?v=6oPRUzzP9DU)&nbsp;![YouTube](img/youtube.png) 


### I can't be bothered to watch the videos, or I still don't get the point 

Yeah, OK, fair enough.
For most people, there is zero reason to be interested in line editors.
For what it's worth, here is how I came to appreciate them.


#### First, distraction-free -- hey, a bird!

It all started as one of those
"distraction-free writing environment" things.
It may seem strange,
but many writers find that one of the biggest enemies to productivity is
the tendency to stop when you're flowing
and get distracted by editing what you've written.
The common wisdom is to separate writing (drafting) and editing.
One solution is to write long-hand.
This works just until your hand gains strength and speed
and you learn that it's easy to quickly scratch something out
and re-write it.
And re-write it, over and over.

So the next step in the saga is to get a typewriter.
You can waste a lot of time tinkering with typewriters;
they're fun and they do fit the bill.
Editing while drafting with a typewriter is indeed a big hassle,
which encourages drafting without stopping, and editing later.

But it also keeps you rooted to one place.
It's not something you can take to the local coffee shop
unless you want to annoy everyone around you
and generally look like a hipster jackass.
(Of course, if you can stomach that, then more power to you;
and if you *are* a hipster jackass,
then you just go on and be the best hipster jackass you can be, you!)

So, enter the humble line editor.
You can learn to enter text into ``ed(1)`` in five minutes,
but the basic idea is that learning to do any real editing
with a line (or character) editor is so difficult, that you won't bother.
You'll just type away, and then once you've finished drafting something,
you'll save it and open the file to edit in a proper text editor
like THE, or Emacs, or vi, or Microsoft Blub 3.0, right?

There's only one problem. It actually turns out that it only takes a little while before you'll learn
how to edit text in ``ed(1)`` quite quickly, and soon you will find yourself using ``ed`` voluntarily to make
little edits in config files, and then soon you'll realize that you like the minimal interface and the
no-bullshit feel of the line editor. You'll find yourself stopping what you're doing while writing your
first draft, and getting sucked into endless editing, and completely lose your flow.

It turns out distraction-free writing is a state of mind, not a tool-set.

But then I continue to like line editors for other reasons, one of which I can sum up in just two words:


#### Thumb typing

Another part of the writing saga is trying to work out how to have the tools you need any time, anywhere
you are. For me, part of that is using
[Termux](https://termux.dev/en/)
on my Android phone. I like Termux and have gotten good
at using it. I plug my phone into a port-replicator with a real keyboard, get power to the phone,
and output to a proper monitor. But there are times when I'm waiting in line at the DMV and don't have a keyboard.
In short, I'm typing with my thumbs on a soft keyboard—and more often than I'd like to admit. 

It seems slightly ironic to me, but the ultra-modern technology of the cell phone / pocket computer
has brought back a situation in which the extremely terse command language of a line editor is a value
just as it was when the I/O model was a Teletype line printer sans CRT or curses library, &c.
Thumb typing makes every extra character an annoyance, and even when ``Control`` and ``Alt`` and ``Escape`` are present
on the keyboard, key chording in general is an annoyance too. That leaves out Emacs for certain and makes
``vi`` barely tolerable. ``ed`` and similar editors could have a renaissance, at least among hipster-nerd-writers,
I guess.


#### And then the usual excuse

But in all seriousness, these days, line editors mostly have one purpose: to work when nothing else
will. For example, if your Linux machine is so hosed that it can't figure out
its terminal characteristics, and nothing works but command line programs in ``/bin`` that
don't try to do anything fancy with the screen, then a line editor is what you
will need for cleaning up that config file. (This can really happen; it's
happened to me.)


#### Oh, and Suckless

Blah blah, small, blah, fast and lightweight, blah blee bleh, [suckless](https://suckless.org/),
can be statically linked, blah blah, isn't a [systemd](https://ihatesystemd.com/why/) service or whatever,
Does One Thing and Does it Well[™](http://www.catb.org/esr/writings/taoup/html/ch01s06.html)—you
know, all that rap.

Ok, but for really, there is something sort of pleasant and comforting
about the minimal "suckless" style of doing things—when it works.


#### Finally, one weird thing

Line editors tend to be very terse, and to expose what amounts to
a language for the manipulation of textual data.
Teco's command language is even Turing-complete. I don't know it
well enough to comment extensively, but if you appreciate the kind of thinking that went into Ken
Iverson's
[Notation as a Tool of Thought](https://www.jsoftware.com/papers/tot.htm)
and think that
[APL](https://en.m.wikipedia.org/wiki/APL_(programming_language))&nbsp;![Wikipedia](img/wikipedia.png)
is a great numerical language, and Wouldn't
it be nice to have something with similar terseness specialized for text manipulation?—well, then maybe
line editors are your thing. APL god
[Aaron Hsu](https://www.sacrideo.us/)
seems to have thought so when he wrote his editor
[ALE](https://github.com/arcfide/ALE) ![GitHub](img/github.png)
(on which see below, though in fact if you asked him what is a great language for text
processing with the terseness of APL, I bet he would answer: "APL!").


## Some quick notes first

### Line editors, context editors, character editors, oh my!

Quick note, just like I said above: There is a distinction to be made between 
"line editors" and "character editors." The distinction may not actually be all that distinct.
In the classic Unix ``ed(1)'' editor, the conceptual unit of structure is the line.
You navigate to and between and around lines. Once you've found a line you like, if you want to
change something for example, you issue a (s)ubstitute command and use a regular expression to
specify what you want to change; then you specify what you want to change it to, as a string.
So that's nice. It takes a little getting used to. It's great, though, when you want to do a lot
of the same thing all at once, since you can use regular expressions to specify multiple lines at
the same time.

On the other hand, what if you want to do complex changes within one line? For that, you
want an editor that has surgical commands for digging into lines at a character level. But then, it's
debatable whether that is really any faster than either using regexes—or sometimes just retyping the line
entire.

In any case, some editors, like Teco (the Famed Father of Emacs) are called "character" or "character-level"
editors. For my purposes, they mostly all operate in such a way that they are like a little
[REPL](https://en.m.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop)&nbsp;![Wikipedia](img/wikipedia.png)
for a text
editing programming language—a
[DSL](https://en.wikipedia.org/wiki/Domain-specific_language)&nbsp;![Wikipedia](img/wikipedia.png)
usually not Turing-complete, though famously, Teco's is;
and so I'm lumping them all together here.
Heck, maybe "REPL-based text editors" would be a better name for them.

As a further note, sometimes you may run across the term "context editor."
In this context, a context editor seems to be the name given to an editor which allows you to select lines by searching,
and not only by inputting a raw line number.
That may seem too obvious a feature to bother getting excited about,
but my impression is that it was a major selling point back in the day.
The CP/M ED.COM editor is one that calls itself a context editor;
another more obvious one is ECCE, which stands for "Edinburgh Compatible Context Editor."
Most "modern" "line editors," like ``ed(1)`` and so on, are also context editors.


### How do I learn to use a line editor?

Well, first, pick one. I'll wait.

OK, now that you've picked ``ed(1)``, let me mention a couple of things.

1. It's not as hard to learn to use effectively as you think.
2. Google for ``ed`` tutorials. There are a number of them. Go through a couple to get a feel for things;
then read the two PDFs I link to by Brian Kernighan under ``ed(1)`` below.
3. Just use the editor for daily stuff for a while and it will start to click.
   Here's a nice
   [cheatsheet](https://github.com/pkrumins/ed-cheat-sheet)
   to help you along.


## Some general external resources

- Obligatory Wikipedia page
  [Line editor](https://en.wikipedia.org/wiki/Line_editor)&nbsp;![Wikipedia](img/wikipedia.png)
- There is also a list on Wikipedia
  [here](https://en.wikipedia.org/wiki/List_of_text_editors#Line_editors)&nbsp;![Wikipedia](img/wikipedia.png)
- A YouTube playlist, of somewhat dubious quality... curated by myself:
  [Awesome Line Editors! \(And some not so awesome\)](https://www.youtube.com/watch?v=6ai0L__MROQ&list=PL-qKtep4qPg47t15pl4U4PE6NutDFn89F)&nbsp;![YouTube](img/youtube.png)
- Well, mainly, there is the page on the Text Editor Wiki:
  [lineEditorsFamily](https://www.texteditors.org/cgi-bin/wiki.pl?LineEditorFamily).
  Unfortunately much on that wiki is out of date,
  and also most of the editors don't seem to have a realistic way to usefully
  be run on modern systems (see [Disclaimers](#disclaimers))
- There is someone's idea of a
  [family tree](https://web.mit.edu/kolya/misc/txt/editors)
  of the older of these editors.
  It is a cleaned up version of what Eric Fischer posted on alt.folklore.computers. The complete
  [thread](https://groups.google.com/g/alt.folklore.computers/c/5BnmLRl-FZM/m/HgwdC31cUO4J)
  can be found on Google Groups.
- Need your text editor to come with a side of formal verification? Here's
  [Formal Ed](https://github.com/bor0/formal-ed)&nbsp;![GitHub](img/github.png), 
  verified by Boro Sitnikovski with the
  [Coq](https://coq.inria.fr/)
  proof assistant, and here's his
  [paper](https://arxiv.org/abs/2006.03525).
  Mind, I don't understand a word of it, but obviously I had to include it.
- I include a link to RFC 569,
  [NETED: A Common Editor for the ARPA Network](https://www.rfc-editor.org/rfc/rfc569.txt)
  here from 1973 just because it's kind of facinating and sort of illuminating. Kinda-sorta.
  

## Disclaimers

Just to set the record straight.


### Focus on practically usable programs

The point and target of this page is to make line editors useful, so its purpose is practical. I have indulged in some extra
"honorable mentions" below for fun, and in some links to things of historical interest, but the main focus is on things that
can be actually compiled and run on "modern" systems and used daily. This excludes things that require emulators
to run, unless the VM is integrated into the host OS so tightly that it's a matter of just clicking on an icon or running a single
thing from the command line to get the editor (not the VM) to run.
Termux counts as realistic, as does maybe
[WSL](https://en.m.wikipedia.org/wiki/Windows_Subsystem_for_Linux)&nbsp;![Wikipedia](img/wikipedia.png) or the equivalent 
you can run on a Chromebook. But, say, the
[Hercules](https://sdl-hercules-390.github.io/html/)
mainframe emulator
([fantastically](https://www.prince-webdesign.nl/tk5)
cool as it may be) would be a case of not a "realistic way to usefully" run it. Same with 8 bit systems and emulators like
[Commodore](https://en.m.wikipedia.org/wiki/Commodore_International)&nbsp;![Wikipedia](img/wikipedia.png)
computers /
[Vice](https://vice-emu.sourceforge.io/),
&c., &c.

In any case, I consider "modern" systems to be:

  - Unix and obviously Unix-like systems like Solaris, BSD, GNU/Linux, MacOS, Minix
  - Android, using something like Termux
  - IOS, using something like
    [iSH](https://ish.app/)
  - Microsoft Windows
  - FreeDOS and maybe even MS-DOS and similar
  - Even IBM mainframe and midrange systems like
    [z/OS](https://en.m.wikipedia.org/wiki/Z/OS)&nbsp;![Wilipedia](img/wikipedia.png),
    [z/VM](https://en.m.wikipedia.org/wiki/Z/VM)&nbsp;![Wikipedia](img/wikipedia.png),
    and whatever their marketing department calls
    [OS/400](https://www.ibm.com/products/ibm-i)
    these days.
   - Maaaaaybe VMS or some flavor thereof


Also, I exclude editors embedded in single applications for use there only
(like, in multi-user dungeon programs, or whatever you call them).

Finally, I am only including editors that are meant for interactive use,
even when they are also used for scripting. So something like the standard
Unix ``sed`` command is out.

This is the standard I am using in deciding what to include below, mostly.  It
is also where I would most appreciate PRs for this page if you have anything you
can add to it.

Now, if you have interesting info about other line editors (there must be a lot
from the old 8-bit days I don't know about, among other things) then please do
send the information along and it can go in the appendices.


### Stuff could be wrong

Please send me a PR, or just a comment, with corrections or additions.  I'm just
one person, with a real job, and you know, a family and a mortgage and all that.


# The Editors

In strict 
[ASCII sort order](https://www.cs.cmu.edu/~pattis/15-1XX/common/handouts/ascii.html)....


## ECCE

[Text Editor Wiki Page](http://texteditors.org/cgi-bin/wiki.pl?Ecce) |
[Wikipedia Page](https://en.wikipedia.org/wiki/Edinburgh_Compatible_Context_Editor)&nbsp;![Wikipedia](img/wikipedia.png)

Ecce Homo? No, homo,
[ECCE](https://ecce.sourceforge.net/)!

With what, exactly, is
[Hamish Dewar's](https://en.wikipedia.org/wiki/Hamish_Dewar)&nbsp;![Wikipedia](img/wikipedia.png)
The Edinburgh Compatible Context Editor compatible?
Well, if they mean that it's compatible with being
[implemented](https://history.dcs.ed.ac.uk//apps/ecce/)
and re-implemented on one OS and in one language after another,
then ECCE is definitely highly compatible.

I was able to build the editor and give it a basic smoke test from the c source
[here](https://ecce.sourceforge.net/download/#source) on both MacOS and Termux on Android.
I cut/pasted the code to a file, ecce.c,
then typed ``cc ecce.c``, then typed ``mv a.out ecce`` and ``./ecce file`` and it just worked. That's saying something for a
1625-line single-file c program (plus a few more hundred of comments and blanks)
based on something originally written in
[IMP](https://en.wikipedia.org/wiki/Edinburgh_IMP)&nbsp;![Wikipedia](img/wikipedia.png)
back in the 1960s.

There is a nice
[manual](https://ecce.sourceforge.net/manual.html)
on the same Sourceforge homepage linked above maintained by Graham Toal.


## EDIT

[Text Editor Wiki Page](https://texteditors.org/cgi-bin/wiki.pl?TSO_EDIT)


### Commentary and one-liners

IBM's EDIT command hails from as far back as
[TSO](https://en.wikipedia.org/wiki/Time_Sharing_Option)&nbsp;![Wikipedia](img/wikipedia.png)
on
[MVS](https://en.wikipedia.org/wiki/MVS)&nbsp;![Wikipedia](img/wikipedia.png)
at least,
and is still current on
[TSO/E](https://www.ibm.com/docs/en/zos/2.4.0?topic=descriptions-tsoe).
under z/OS.

### Versions

There are no-doubt as many versions of EDIT as there are versions of TSO, and therefore of IBM mainframe operating systems.

#### Docs and Tutorials

[Jay Mosley](https://www.jaymoseley.com/)
has an extensive
[TSO Tutorial](https://www.jaymoseley.com/hercules/tso_tutor/tsotutor.htm)
including the use of EDIT, and there are about 100 pages of documentation
in (among many other places) an old IBM
[TSO Command Language Reference](http://bitsavers.org/pdf/ibm/370/OS_VS2/Release_3.7_1976/GC28-0646-3_OS_VS2_TSO_Command_Language_Reference_Rel_3.7_Jan76.pdf)&nbsp;![PDF](img/pdf.png)
on
[Bitsavers](http://www.bitsavers.org/).


#### Getting It

The only way to access EDIT is on a mainframe or on an emulated mainframe.
Emulations are out of scope here, so you would have to have access to some actual big iron.
If you do, you do. If you don't, you don't.

Let me know—I would love to know—if there are any reimplementations of EDIT on other systems.


## EDLIN 

[Wikipedia Page](https://en.wikipedia.org/wiki/Edlin)&nbsp;![Wikipedia](img/wikipedia.png) |
[Text Editor Wiki Page](https://texteditors.org/cgi-bin/wiki.pl?EDLIN)


### Commentary and one-liners

I'm really not sure about EDLIN (as it is sometimes written, or Edlin, as the FDOS project writes it).
[Tim Paterson's](https://en.wikipedia.org/wiki/Tim_Paterson)&nbsp;![Wikipedia](img/wikipedia.png)
original seems as if it may have been intended
to be a clone or simplified version of the ED.COM editor from the old CP/M operating
system (about which see the ED.COM entry).
While the MS-DOS
[source](https://github.com/microsoft/MS-DOS/tree/main/v4.0/src/CMD/EDLIN)&nbsp;![GitHub](img/github.png)
has been released by Microsoft,
it is Assembly code and could be challenging to assemble or re-implement.

The FreeDOS project has done an
[implementation](https://github.com/FDOS/edlin)&nbsp;![GitHub](img/github.png)
in c, and I have been able to compile and run it on several POSIX or POSIX-adjacent systems,
but my skimming some documentation suggests that
the FreeDOS implementation is a simplified version
possibly lacking in character editing features DOS EDLIN *may* have had.
\[Please correct me if I'm wrong.\]

EDLIN came standard on MS-DOS machines and I believe up to about Windows 7,
in some versions, at any rate. It is a little more friendly 
than ``ed(1)`` and a good deal little less powerful, at least the FreeDOS version seems so to me.
It is a functional text editor, though, for
most use cases other, perhaps, than use in scripts.


### Versions

#### xx-DOS version (MS-DOS, PC-DOS, whatever) versions

It may be possible to legitimately use one of the old versions for DOS if you have old hardware
but not so old you can't get data off of it. Otherwise, this is here mainly for historical interest.


#### Docs and Tutorials

There is a nice
[document](https://uncljoedoc.tripod.com/a/edlin.htm)
with what I can only assume is the docuemntation for an old version of Edlin. It goes into some detail.


#### Getting It

It is included with MS-DOS, so if you have that, you should have EDLIN.


#### Source

- **Microsoft MS-DOS v.4** [source](https://github.com/microsoft/MS-DOS/tree/main/v4.0/src/CMD/EDLIN)&nbsp;![GitHub](img/github.png). 


#### Binaries

*TBD*


### FreeDOS version

This is the one you will want to get and probably compile for modern systems.


#### Docs and Tutorials

Here are a couple of videos about Edlin from the FreeDOS project's YouTube
  [channel](https://www.youtube.com/@freedosproject)&nbsp;![YouTube](img/youtube.png):

  - [Using FreeDOS - EDLIN](https://www.youtube.com/watch?v=CIlJeKuSl9w)&nbsp;![YouTube](img/youtube.png)   
  - [Patreon bonus - Programming in EDLIN](https://www.youtube.com/watch?v=MUmiluneuoo)&nbsp;![YouTube](img/youtube.png)

The FreeDOS tutorial page images don't seem to work, so here is a snapshot from the Wayback Machine:
[How to edit text with Edlin](https://web.archive.org/web/20231021151327/https://freedos.org/books/get-started/18-using-edlin/)&nbsp;![Wayback Machine](img/archive.png)


### Getting It


##### Source

- [Source](https://github.com/FDOS/edlin)&nbsp;![GitHub](img/github.png)
  from the FreeDOS project, but compiles on POSIX systems.


#### Binaries

 - **Microsoft Windows 10**: There are native Windows binaries of FreeDOS EDLIN available
   [here](https://darrengoossens.wordpress.com/2019/05/25/native-edlin-on-windows-10/).
 - **Ubuntu Linux**: There seems to be an apt package
   [available](https://launchpad.net/ubuntu/+source/edlin)


## Edbrowse 

Many Linux distributions will allow you to install Edbrowse from the package manager.
If not, it's
[here](https://github.com/CMB/edbrowse).

Edbrowse is a web browser complete with Javascript engine,
modeled on the user interface style of `ed(1)` and complete with --
you guessed it -- a text editor, also modeled on `ed(1)`.
It's really a kind of complete user interface for the blind.
In the end, it may be the most complex, complete, and impressive
bit of work on this page. At some point I would like to have more to say about it.

In the meantime, here's some
[documentation](https://edbrowse.org/usersguide.html).
Enjoy.


## Teco

[Wikipedia Page](https://en.wikipedia.org/wiki/TECO_(text_editor))&nbsp;![Wikipedia](img/wikipedia.png) |
[Text Editor Wiki Page](https://texteditors.org/cgi-bin/wiki.pl?TECO)

Teco is a text editing programming language masquerading as a REPL-like text editor.
It seems to be the nine-hundred pound gorilla of the bunch.
It is [nortoriously](https://scienceblogs.com/goodmath/2006/09/22/worlds-greatest-pathological-l-1)
difficult to learn (though perhaps not "pathologically" so)
and its code so notoriously difficult to read that it can be an amusing
[game](https://www.catb.org/~esr/jargon/html/T/TECO.html).
It is also the source of the world's first software
"[Easter egg](https://www.acriticalhit.com/make-love-not-war-first-software-easter-egg/)."

Teco does not, by itself, seemt to be well integrated into the Unix style of doing things,
and I have spent very little time looking at it myself, since my interest is mainly practical,
but for what it's worth:

### Versions

#### DOS

- [Here](http://ftpmirror1.infania.net/pub/simtelnet/msdos/editor/pctco295.zip)
  is an old FTP archive (Simtelnet archive) version for MS-DOS which I was able to get working in a DOS emulator,
  with the understanding being that by "working" I mean that I was able to start it
  then exit it. Not much else.
- And here is
  [another](http://ftpmirror1.infania.net/pub/simtelnet/msdos/editor/teco.zip)
  version someone cooked up also from a Simtelnet archive.
  This one too I was able to run and exit but with it nothing more have done.

#### POSIXish

But seriously, folks, if you want to try using Teco, what you probably want is either
[TECOC](https://github.com/blakemcbride/TECOC)&nbsp;![GitHub](img/github.png) or
[TECO-64](https://github.com/fpjohnston/TECO-64)&nbsp;![GitHub](img/github.png).
(My money is on the later, as it seems to be a little better integrated into the modern Unix-like environment.)
I have been able to compile both on a variety of system including Termux and MacOS.

### Documentation

- There is a FreeBSD
  [man](https://man.freebsd.org/cgi/man.cgi?teco)
  page for Teco. Presumably there is or was therefore a version of Teco available from their software repositories.
- Here's the old DEC [manual](https://usermanual.wiki/Document/DEC10UTECAADdecsystem10IntroductionToTECOTextEditorAndCorrector.319080858.pdf)&nbsp;![PDF](img/pdf.png)
- Here's the old TENEX [manual](https://dn790008.ca.archive.org/0/items/tenex-teco/Image071617171818.duplex_text.pdf)&nbsp;![PDF](img/pdf.png)
- See the Github archives for TECOC and TECO-64 for more updated manuals.
  
## ed

[Wikipedia Page](https://en.wikipedia.org/wiki/Ed_(software))&nbsp;![Wikipedia](img/wikipedia.png) |
[Text Editor Wiki Page](https://texteditors.org/cgi-bin/wiki.pl?Ed)

(Aka. ``ed(1)``, and yes yes, also aka.,
"[The standard text editor](https://www.gnu.org/fun/jokes/ed-msg.html)."
(Obligatory link for everyone who hasn't already heard the joke—all both of you.))

``ed`` is, in addition to being the standard text editor as see above, also
probably the only line editor anyone reading this ought ever to bother with.
It comes standard or is easily gotten on any Linux, Unix, BSD, or on MacOS; and it 
has been ported to Microsoft Windows. It is mature, stable, and reliable.

Therefore it is uninteresting. Well, that's not entirely true, but the nerd
in me wants to find other options.

If ``ed(1)`` isn't on your Linux or BSD system, wipe your hard drive and install a better
distribution. Failing that, try something like ``sudo xbps-install ed`` or for you poor benighted souls, try
``sudo port install ed`` or ``sudo apt install ed``—you get the idea.

If you would like to know how it works, Google for a tutorial or two, and then when you've got a taste
of it, read Brian Kernighan's two classic tutorials, in order: 1) 
[A tutorial introduction to the UNIX text editor](https://www.nyx.net/~ewilli/edtut.pdf)&nbsp;![PDF](img/pdf.png) and 2)
[Advanced Editing on UNIX](https://cscie26.dce.harvard.edu/~dce-lib113/reference/progtools/EdTut.pdf)&nbsp;![PDF](img/pdf.png)

### Versions

There is no doubt much to be said about different versions of ``ed,`` and I don't know what it all is yet,
but in the meantime, there is a nice 
[writeup](https://unix.stackexchange.com/questions/657459/what-is-the-difference-between-gnu-ed-and-the-version-of-ed-that-ships-with-unix)
on Stack Exchange about some differences between the BSD version, the
[GNU](https://www.gnu.org/)
version, and the
[Plan 9 Operating System](https://en.wikipedia.org/wiki/Plan_9_from_Bell_Labs)&nbsp;![Wikipedia](img/wikipedia.png) version.

Also of possible note is the
[Heirloom Project](https://heirloom.sourceforge.net/) version of 
[ed](https://github.com/ryanwoodsmall/heirloom-project/tree/master/heirloom/ed)&nbsp;![GitHub](img/github.png)
and the musl C library version of
[same](https://github.com/ryanwoodsmall/heirloom-project/tree/musl/heirloom/ed)&nbsp;![GitHub](img/github.png).

## edam
[edam](https://github.com/phonologus/edam) is a clone of Rob Pike's sam editor for the [Plan9](https://9p.io/plan9/) OS, but without the graphical display, so it is is the equivalent of running 'sam -d'. I had some trouble getting it to compule on Termux and other less popular systems, but it compiled fine and ran on x64 Ubuntu.

/sam/ (and therefore edam as well) works similarly to ed, but uses "[structural regular expressions]( http://doc.cat-v.org/bell_labs/structural_regexps/se.pdf))&nbsp;![PDF](img/pdf.png)" (similar to the Vim-like [Vis](https://github.com/martanne/vis)![GitHub](img/github.png), supports multiple buffers (like qed) and allows selection to include more than a single line. 

## em

'em' is the "Editor for Mortals," written by Peter Salus. It compiles
from
[this](https://github.com/rsdoiel/em-1.0.0)![GitHub](img/github.png)
source on my x64 Ubuntu Linux system, and runs.  It is also available on
from [pkgsrc](https://www.pkgsrc.org/). It aims to be an easier to use
editor similar to the Unix 'ed' editor.

There is a [man
page](https://www.coulouris.net/cs_history/em_story/QMC_Unix_manual.html);
and notes from an
[interview](http://www.eecs.qmul.ac.uk/~gc/history/index.html) with
Peter Salus makes interesting reading.


## ex

*TBD*


## led 1 

This is the "led" that is written in Lisp and compiled to Lua.

*TBD*


## led 2

This is the "led" that is a re-implementation of the CP/M ED.COM editor.

Sage Hendricks has a re-implementation if the CP/M ED.COM for \*nix systems called
[led](https://github.com/sage-etcher/leaf-context-editor)&nbsp;![GitHub](img/github.png)
(for "leaf context editor").
I have been able to build it on a couple of platforms,
but either I don't know how to invoke it, or it doesn't work. 
If you're a c hacker, please make it work and let me know. 


## qed

[Wikipedia Page](https://en.wikipedia.org/wiki/QED_(text_editor))&nbsp;![Wikipedia](img/wikipedia.png) |
[Text Editor Wiki Page](https://texteditors.org/cgi-bin/wiki.pl?Qed)

``qed`` (sometimes written QED)  was, it is said, written for an old 1960s machine using an old 1960s 
operating system. Various later versions appeared and eventually it was
re implemented in c, and there is a version available called
[qed-new](https://github.com/phonologus/qed-new)&nbsp;![GitHub](img/github.png)
with Unicode support which will compile and run,
at least minimally, on POSIXy systems I've tried, with a little tinkering.

This one has become my daily driver editor -- for first drafts, that is
(and I still don't know it very well).
It sports multiple buffers, which is nice if you're into that kind of thing.
It and "sam -d" might be the most powerful line editors around.


Brought to you by the same person behind qed-new above, is a project to produce a nice, updated version
of --

 - --the [manual](https://github.com/phonologus/qed-book)&nbsp;![GitHub](img/github.png)

Some other links of general interest, of which the second is contained in the first:

- [Some ``qed`` / ``ex`` / ``vi`` historical documents](https://www.reddit.com/r/vim/comments/1o6s9m/some_qed_ex_vi_historical_documents/)
- [An incomplete history of the QED text editor](https://www.bell-labs.com/usr/dmr/www/qed.html)


## sam -d

/sam/ is a GUI-based editor for the Plan 9 Operating system with a
command language similar to ed. It requires X libraries to build on
Linux, but once built it can be invoked in a terminal with "sam -d" and
operates similarly to ed, but with the addition of the use of
"structural regular expressions" (for more on which, see Rob Pike's
[document](
http://doc.cat-v.org/bell_labs/structural_regexps/se.pdf))&nbsp;![PDF](img/pdf.png).


## sued

If you like your lightweight minimalistic line editors with a side order of dozens of dependencies, then
[sued](https://github.com/AeriaVelocity/sued),
implemented in rust by Arsalan "Aeri" Kazmi, might just be for you.

But all snark aside, sued represents a genuinely creative and independent-minded rethinking of the line editor paradigm.
(I can't believe I just wrote that with a straight face, but it's true.)
In particular, unlike most or all others, it is modeless, in the sense that it starts up in insert mode,
and then to send it commands, you write the command words prefixed with a tilde (~) character
(which you can change if you want) at the beginning of a line
and merrily continue in insert mode the whole while.
The command set is idiosyncractic and even sometimes funny.
It's a slick addition to the line editor pantheon and worth trying out.
I got it to `cargo build sued` on my Android running Termux without issue and that's pretty cool by itself.

If you have more to add about this editor, please send me more or send a PR.


# Appendices


## Appendix A: Honorable Mentions


### ALE

*honorable mention* 

[Aaron Hsu's](https://www.sacrideo.us/)
editor
[ALE](https://github.com/arcfide/ALE)&nbsp;![GitHub](img/github.png)
is a line editor modeled on ``ed(1)`` in, apparently, something like 68 lines of characteristically inscrutable APL,
including blank lines for formatting.
I have not tested it in large part because it appears to be written for the
[Dyalog](https://www.dyalog.com/)
version of APL, for which you can get a
[free-for-noncommercial-use license](https://www.dyalog.com/download-zone.htm)
—which I have done in the past with great interest,
but at the moment I'm not set up for it and therefore have not been able to,
though I yet might—test it, that is.

I include it here, under "honorable mentions" only because its environment is so specialized
that it would not have much general use, and seems to be really a single-application editor.


### ATTO

*honorable mention* (Doesn't really seem to be usable.)

A very small line editor that really wants to use conio in the Microsoft environment, by Dieter Schoppitsch,
it is not to be confused with the Emacs-alike of the same name. See more information below under "buup." 

Dieter's original web page about ATTO archived from 2016 is
[here](https://web.archive.org/web/20160826220131/http://web.uta4you.at/shop/atto/index.htm)&nbsp;![Wayback Machine](img/archive.png)

I've posted a copy of the
[code](https://github.com/EvansWinner/atto_line_editor)&nbsp;![GitHub](img/github.png)
with some small changes to get it to compile under Linux.
From there you can find Dieter's original page on the Wayback Machine.

I also have started working a little on a slightly modified version for POSIX environments
(see [buup](#buup) below).


### ED.COM

[Text Editor Wiki Page](https://texteditors.org/cgi-bin/wiki.pl?ED)

*honorable mention*

Not really available on modern systems.

ED.COM is a line editor that was used on the
[CP/M](https://en.wikipedia.org/wiki/CP/M)&nbsp;![Wikipedia](img/wikipedia.png)
operating system, a kind of precursor to DOS.
All I know about ED.COM I learned from a pair of videos
done by someone whose name I haven't found, but whose channel on YouTube is called
[TechTinkering](https://www.youtube.com/@TechTinkering)&nbsp;![YouTube](img/youtube.png):
 - [I Love ED on CP/M](https://www.youtube.com/watch?v=7pqaj050X7g)&nbsp;![YouTube](img/youtube.png)
   and the shorter,
 - [A Very Quick Tour of ED on CP/M](https://www.youtube.com/watch?v=DY58jTcidxE)&nbsp;![YouTube](img/youtube.png)

ED (which I style ED.COM in the CP/M style to differentiate it from the
Unix ``ed(1)``) appears to be something like a mix between a line-based
editor and a character- based editor, like Teco. This makes it appear
complicated, byzantine—and interesting. I get the impression that it was
written in assembly language and that a port to modern systems would
amount to a complete re-write. See the entry for [led](#led-2) for an
attempt at that.

There are also a
 - [manual](http://cpmarchives.classiccmp.org/cpm/Library/Manuals/CPM_1.4_ED_Users_Manual_1978.pdf)&nbsp;![PDF](img/pdf.png)
    available, and
 - a roughly 35-page chapter in
   [The CP/M handbook with mp/m](https://.org/details/The_CPM_Handbook_with_MPM/mode/1up)&nbsp;![Wayback Machine](img/archive.png) by Rodnay Zaks.


### led 3

*(dis?)honorable mention*

What does ``ed(1)`` have to keep track of?
Well, the name of the current file,
the current line number, and a buffer full of contents to be written
the next write. Right? So, what if we were willing to tell ``ed`` what
file we are working on with every command? And what if the program
were set to write our changes after every operation? And what if we
were also willing to tell it what line number or substring to operate
on with every command? Well, then we could have a perfectly state-less
editor. We wouldn't need a separate editing environment at all, really.
We could just write a command line program
that edited text files one command-line
command at a time, one line at a time.

And this insane idea is what is behind Patrick Taylor's ``led`` program
for DOS. I guess it is, anyway. Anyway, you can download
[led101.zip](https://ftp.icm.edu.pl/pub/windows/garbo/pc/fileutil/led101.zip)
from that link on some random old DOS software archive
or any of several others. Have fun and good luck and all that.
Note that there is no source code included with that zip .
Maybe it would be fun to re-implement.

It seems like an interesting idea, and is probably more meant for use
in batch files rather than for interactive use, but in any case, it's
the weirdest one I've come up with so far.


## Appendix B: Mainly of Historical Interest

The past is coming soon... or something.


## Appendix C: Others

This is mostly going to be school final projects on GitHub I think.
"Implement a line editor like ``ed``.
Include commands to open a file, write a file, print and replace lines."
I think there are a lot of them, but I'll probably only include them
if they at least compile and don't segfault when run.
Maybe there will be something valuable.


### buup

Not quite usable yet.

[buup](https://github.com/EvansWinner/buup)&nbsp;![GitHub](img/github.png)
is basically my own attempt to modify [ATTO](#atto) for Linux use,
but not really ready to be used... kinda like this page itself, really.

## cmd-line-text-editor

Nothing known about this yet.

https://github.com/craigbarstow/cmd-line-text-editor

## ed clone in go

An ed [clone](https://go.dev/) in [go](https://go.dev/).
Just what it sounds like, unless what it sounds to you like is ``ed.``
I don't understand what is so difficult about naming things.
I haven't looked at this yet.


## edd

I don't know anything about [edd](https://github.com/bojle/edd)&nbsp;![GitHub](img/github.png) yet.


## edlin clone

[This one](https://github.com/howerj/edlin)&nbsp;![GitHub](img/github.png)
the author unhelpfully calls "edlin" even though it is a clone.
I haven't looked at it yet.


## edlin-text-editor

[edlin-text-editor](https://github.com/shleppy/edlin-text-editor)&nbsp;![GitHub](img/github.png),
as it's author calls it, is a school assignment with a somewhat less-than-original name.
I haven't looked at it yet.


## edpy

Someone had to write an ``ed`` clone in Python. [This](https://github.com/mmanguno/edpy)&nbsp;![GitHub](img/github.png)
is it. I'm just glad it wasn't me. At least they didn't call it "pyed."

## Fed

[Fed](https://github.com/scotws/Fed)&nbsp;![GitHub](img/github.png)
is a line editor in Fourth, specifically [gforth](https://gforth.org/).
I haven't looked at it yet.


---


# Colophon

This was mostly written with [vim](https://www.vim.org/), frankly. Shoot me.
Some was in ``vi``, and yes, some in ``ed``. Right at this moment, I'm typing
in GitHub's web-based editor. So, I fear commitment
(though evidently not Git commitment).

Why this silly page about text editors? Because when you can't think of anything to make,
you end up spending all your time sharpening your tools.
I wanted a mission and despite my sins, nobody will give me one.


---
<p align="center">
  Brought to you by—<br />
  <img src="img/edMotto.jpg" alt="The Hermetic Order of ed(1)" width=300 /> 
</p>
