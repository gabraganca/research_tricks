Scientific Research Tricks
==========================

Research is awesome! But today, due to several reasons, it is lacking some
things and making some error during its development.

My objective with this project is to gather some tips and tools to improve how
research is done.


Copyright 2014 DPPG@ON Organization.

License: Creative Commons Attribution 4.0 International License.

http://creativecommons.org/licenses/by/4.0/


Version Control System
----------------------

At some point of your research did you make a bad choice or a have done mistake
and had to go back some steps? Of course you did. Research is not done
following a recipe on some cookbook. Mistakes are done. One should try to avoid
mistakes, but do not regret about it. Learn from it.

The problem that I want to address here is what can you do when do you do a
mistake. You will probably want to take some steps back. If you are a very
methodical person, you will have every step taken wrote down on some logbook or
similar. But I guess that not everybody is like this.

Or maybe you keep track of changes like this:

![A Story Told in file names](http://www.phdcomics.com/comics/archive/phd052810s.gif "PhD comics #1323")

This is not an optimized way of tracking your files. I can see only one
possible future to this and it is a totally mess.

So, why do you not try a
[Version Control System (VCS)](http://en.wikipedia.org/wiki/Revision_control)?

A VCS ["is the management of changes to documents, computer programs, large
web sites, and other
collections of information."](http://en.wikipedia.org/wiki/Revision_control).
With this you can keep track of any change you do on your research and fall-back
 to any point that you want.

One VCS widely used today is [`git`](http://git-scm.com/). It was created by
[Linus Torvalds](http://en.wikipedia.org/wiki/Linus_Torvalds), the same creator
of the [Linux Kernel](http://en.wikipedia.org/wiki/Linux_kernel). Fun fact:
like Linux, Linus named `git` after himself. Git is British English slang for a
stupid or unpleasant person, and Linus said ["I'm an egotistical bastard, and
I name all my projects after myself. First 'Linux', now 'git'
."](https://git.wiki.kernel.org/index.php/GitFaq#Why_the_.27Git.27_name.3F).
Git is free and open source.

You can try the basics of `git`
[here](http://try.github.io/levels/1/challenges/1) and this
[book](http://git-scm.com/book) by [Scott Chacon](http://scottchacon.com) or
this
[another book](http://chimera.labs.oreilly.com/books/1230000000561/index.html)
by [Richard E. Silverman](http://www.qoxp.net/) can also help.

Backup and Sharing
------------------

So do you want to do a backup of your research and/or work on multiple
computers? You could try a USB stick or a portable HD. That is a way to do it,
but maybe not the best. Maybe a cloud storage service like
[Dropbox](https://www.dropbox.com/) or
[Google Drive](https://drive.google.com/). I would guess that this a better way
to do it. Dropbox has a rudimentary VCS built-in. Maybe you want to share with
your collaborators? You could create a shared folder on Dropbox.

But may I suggest something better? Something stronger?
[Github](https://github.com/about).
It ["is a web-based hosting service for software development projects that use
the Git revision control system."](https://en.wikipedia.org/wiki/GitHub) You
can store all your Git projects on Github and share with you collaborators.
You can browse your and others research online on your preferred browser.
Today you almost not need to know `git` to use it.

Regular expressions
-------------------

How to find some pattern on a text.


Useful links:

* [Debbuggex](http://www.debuggex.com/): nice resource to check regex;
* [Regex Crossword](http://regexcrossword.com/): practice or learn some regex
  skills by playing crossword.


Shell
-----

["A Unix shell is a command-line interpreter or shell that provides a 
traditional user interface for the Unix operating system and for 
Unix-like systems."][shell]. Some people are afraid of the 
shell. Do not. The shell is one of your most powerful ally. If you know it 
well and dominate it, what you can do is almost magic.

If your are running Linux, you will probably have [Bash][bash] as your 
[Unix shell][shell]. If you are running Windows you can try [Cygwin][cygwin].

I highly recommend seeing the [Software Carpentry][swcarpentry] tutorial 
[track on the Shell][shell_track]. It is very good and it will give you all the basics 
on the Shell.

For example, below I listed some commands that can speed up your workflow.

* List files on one folder and send it to a file:
  `ls path/to/folder > list_of_files.txt`;
* Finding files:
  `find path/to/folder -name filename`
* Finding files with RegEx:
  `find path/to/folder | grep 'add-your-regex-here'`
* Finding patterns inside files with RegEx:
  `find path/to/folder | xargs grep 'add-your-regex-here'`
* Removing files found with previous command:
  `find path/to/folder | grep 'add-your-regex-here' | xargs rm`
* Compare directories:
  `diff -rq dirA dirB`
* Convert all figures in a folder from one type to other:
  `for f in *.jpg; do convert ./"$f" ./"${f%.jpg}.png"; done`


Bonus Tip: [Bash git prompt](https://github.com/magicmonty/bash-git-prompt)
is a resource that gives basic `git` information of the repository directly
on the prompt.

[bash]: https://en.wikipedia.org/wiki/Bash_(Unix_shell)
[shell]: http://en.wikipedia.org/wiki/Unix_shell
[cygwin]: http://www.cygwin.com/
[swcarpentry]: http://software-carpentry.org/index.html
[shell_track]: http://software-carpentry.org/v4/shell/index.html



Script programming
------------------

You can learn python basics at
[CodeAcademy](http://www.codecademy.com/tracks/python). I have tried and it is
very nice.

Another interactive way to learn python is the
[learnpython.org](http://www.learnpython.org/). Give it a try.

There is a tutorial for non-programmers
[here](http://en.wikibooks.org/wiki/Non-Programmer%27s_Tutorial_for_Python_3).

There is also the now famous
[Learn Python the Hard Way](http://learnpythonthehardway.org/). It seems that
it focus on exercise and repetition as learning tools.

This [link](http://pythonbooks.revolunet.com/) and
[this](http://readwrite.com/2011/03/25/python-is-an-increasingly-popu#awesm=~o98NZtqHzwYofe)
contains a compilation of free books.

If you want to know which python modules/packages are installed in your system,
you just have to type in your shell:

~~~
pip freeze
~~~

And of course, this assumes that you have
[`pip`](https://pypi.python.org/pypi/pip) installed in your system.


Installing python packages on your system could result on some headache.
For example, I stayed one afternoon trying to figure it out why my package was
not running after I reinstalled it. The reason was that I was getting conflicts
between the new and the old version. The solution was to use
[virtualenv](https://pypi.python.org/pypi/virtualenv) and
[`virtualenvwrapper`][venvw].

[venvw]: http://virtualenvwrapper.readthedocs.org/en/latest/index.html

as the name says `virtualenv` creates a python virtual environment. this allows
the user to install any python package without worryng in messing the system
packages. also, the user can create any number of virtual environments,
for example, one for each project.

Good editor
-----------

it is very important to have a good editor.

if you are the nerd-geek-kind-of-awesome guy, you should probably try
vim or emacs.

Automation
----------

how to automate things using python. this is great when you do a miskate and
had to run several things again.

some links to check:

* [@astrofrog course](https://github.com/astrofrog/py4sci)
* [@jrjohansson tutorials](https://github.com/jrjohansson/scientific-python-lectures)


negative results
-------------

negative results are still results. publish them. why publish it?
just look the following cartoon and i guess you will understand.

![negative data](http://upmic.files.wordpress.com/2013/06/negative-data.png "from the upturned microscope")

got it?

probably, a journal will not accepted a paper showing negative results. and
because of this, enters [figshare](http://www.figshare.com).
This resource ["allows users to upload any file format to be made visualisable
in the browser so that figures, datasets, media, papers, posters, presentations
and filesets can be disseminated in a way that the current scholarly publishing
model does not allow.](http://figshare.com/about). Each image, presententation
or any other kind of data receives a
[DOI](http://en.wikipedia.org/wiki/Digital_object_identifier)
that will uniquely identify your data and it will allow others to cite it.

Visualization
-------------

How to visualize your data is a very important step. I must say, crucial. It is
very hard to obtain any results without it. Unless you are a statistic ninja,
and even that, you would probably use visualization to convince your audience
of your findings.

One of the fathers of this field is
[Edward Tufte][Tufte]. I have not yet read it, but his first book, [The Visual
Display of Quantitative Information][Tufte_book], is very highly recommended.

[Tufte]: http://www.edwardtufte.com/tufte/index
[Tufte_book]: http://www.edwardtufte.com/tufte/books_vdqi

So, how one can visualize data? There are several tools available. You could
use a spreadsheet editor, like [LibreOffice Calc][OOffice]. The resources are
limited, but you can get a visualization quickly and it is very good when one
does not have any other skils. And if you want to make better plots with it,
you will probably want to try [RAW](http://raw.densitydesign.org/).

[OOffice]: https://www.libreoffice.org/features/calc/

One can draw it by hand, or use [GIMP](http://www.gimp.org/) or
[Inkscape](http://inkscape.org/), for example. But, for that, it would probably
be good to have some artistic skills. And also, if something change on your
data, you would probably have to start it from scratch.

Also, one could code some routine to do visualization. The advantage of this
method is that probably you will only have to code it once, i.e. the code is
data independent. If the data changes, you only have to run it again. Well,
achieving this will only depend of your coding skill.

There are several good visualization toolkits on the wild, like
[`D3`](http://d3js.org/) for javascript. If you want to learn D3, the book by
[Scott Murray](http://alignedleft.com/about/),
_Interactive Data Visualization for the Web_, is now
[available online for free][d3_free]. And, for python, we have
[`Matplotlib`](http://matplotlib.org/index.html),
[`Mayavi`](http://code.enthought.com/projects/mayavi/)
and [`ggplot`](https://github.com/yhat/ggplot?source=cc#ggplot-from-yhat).
[`Ggplot2`](http://ggplot2.org/) is a very well-known plotting system for
[R][Rlang] and `ggplot` is specially good for those that are learning python
but have a solid background in R. And if you want the `D3` awesomeness in your
python code, try [Vincent](https://github.com/wrobstory/vincent).

[Rlang]: http://www.r-project.org/
[d3_free]: http://chimera.labs.oreilly.com/books/1230000000345/index.html


Also, [Bret Victor](http://worrydream.com/#!/Bio) is working on a software
that will allow to dynamically draw your visualizations. If you want to know
more about it, you can check his [talk](http://vimeo.com/66085662) and
[here](http://worrydream.com/DrawingDynamicVisualizationsTalkAddendum/).
It is really impressive!

And according to [Nathan Yau](https://twitter.com/flowingdata) from
[Flowing Data](http://flowingdata.com/), there is only one way to learn
visualization: [work with data][fd_post].

[fd_post]: http://flowingdata.com/2013/07/12/getting-started-with-visualization-after-getting-started-with-visualization/

I also recommend his [first book](http://flowingdata.com/visualize-this/) as a
starting point to do visualization. He address what type of visualization there
are, the tools available and all on a very pleasant reading content.
I have not yet read his [second](http://flowingdata.com/data-points/), but I am
very anxious to get a copy.

