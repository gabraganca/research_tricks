Scientific Research Tricks
==========================

Research is awesome! But today, due to several reasons, it is lacking some things and making some error during its development.

My objective with this project is to gather some tips and tools to improve how research is done.


Version Control System
----------------------

At some point of your research did you did a bad turn at some point or a mistake and had to go back some steps? Of course you did. Research is not done following a recipe on some cookbook. Mistakes are done. One should try to avoid mistakes, but do not regret about it. Learn from it. 

The problem that I want to address here is what can you do when do you do a mistake? You will probably wnat to take some steps back. If you are a very methodical person, you will have every step taken wrote down on some logbook or similar. But I guess that not everybody is like this. Why do you not try a Version Control System (VCS).

A VCS ["is the management of changes to documents, computer programs, large web sites, and other collections of information."] (http://en.wikipedia.org/wiki/Revision_control) With this you can keep track of any change you do on your research and fallback to any point that you want.

One VCS widely used today is [git](http://git-scm.com/). It was created by Linus Torvalds, the same creator of the Linux Operation System. Fun fact: like Linux, Linus named git after himself. Git is British English slang for a stupid or unpleasant person, and Linus said ["I'm an egotistical bastard, and I name all my projects after myself. First 'Linux', now 'git'."](https://git.wiki.kernel.org/index.php/GitFaq#Why_the_.27Git.27_name.3F). Git is free and open source. 

You can try the basics of git [here](http://try.github.io/levels/1/challenges/1) and this [book](http://git-scm.com/book) can also help.

Backup and Sharing
------------------

So do you want to do a backup of your research and/or work on multiple computers? You could try a USB stick or a portable HD. That is a way to do it, but maybe not the best. Maybe a cloud storage service like [Dropbox](https://www.dropbox.com/) or [Google Drive](https://drive.google.com/). I would guess that this a better way to do it. Dropbox has a rudimentary VCS built-in. Maybe you want to share with your collaborators? You could create a shared folder on Dropbox.

I will suggest something better. [Github](https://github.com/about). It ["is a web-based hosting service for software development projects that use the Git revision control system."](https://en.wikipedia.org/wiki/GitHub) You can store all your Git projects on Github and share with you collaborators. You can browse your and others research online on your preferred browser. You can even modify text files online.

Regular expressions
-------------------

How to find some pattern on a text.

Bash
----
You are doing your research on Linux, right? No? Well, so you would probably want to skip this section. 

If your are running Linux, you will probably have [Bash](https://en.wikipedia.org/wiki/Bash_(Unix_shell)] as your [Unix shell](http://en.wikipedia.org/wiki/Unix_shell). Some people are afraid of the terminal. Do not. The terminal is one of your most powerful ally. If you know it well and dominate it, what you can do is almost magic. 

Talk about some commands and use of pipe to send the result of one command to another

e.g

* Finding files with RegEx: find path | grep 'add-your-regex-here'
* Removing files found with previous command: find path | grep 'add-your-regex-here' | xargs rm


Script programming
------------------

Talk how to use Script programming, specially about python.

You can learn python basics at [CodeAcademy](http://www.codecademy.com/tracks/python). I have tried and it is very nice.

There is a tutorial for non-programmers [here](http://en.wikibooks.org/wiki/Non-Programmer%27s_Tutorial_for_Python_3).

This [link](http://pythonbooks.revolunet.com/) and [this](http://readwrite.com/2011/03/25/python-is-an-increasingly-popu#awesm=~o98NZtqHzwYofe) contains a compilation of free books. 


Unit testing
------------


Automation
----------

How to automate things using python. This is great when you do a miskate and had to run several things again.

