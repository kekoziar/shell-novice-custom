---
title: "Introducing the Shell"
teaching: 5
exercises: 0
questions:
- "What is a command shell and why would I use one?"
objectives:
- "Explain how the shell relates to the keyboard, the screen, the operating system, and users' programs."
- "Explain when and why command-line interfaces should be used instead of graphical interfaces."
keypoints:
- "A shell is a program whose primary purpose is to read commands and run other programs."
-  "This lesson uses Bash, the default shell in many implementations of Unix."
-  "Programs can be run in Bash by entering commands at the command-line prompt."
- "The shell's main advantages are its high action-to-keystroke ratio, its support for
automating repetitive tasks, and its capacity to access networked machines."
- "The shell's main disadvantages are its primarily textual nature and how
cryptic its commands and operation can be."
---
### Background

Humans commonly interact with computers in many different ways, but usually, it's through a **graphical user interface**, or GUI ('gooey').  We give instructions by clicking a mouse and using menu-driven interactions.

While a GUI makes it intuitive to use a computer, it scales very poorly when you want to do a repetitive task. Imagine this: for a literature search, you have to copy the third line of one thousand text files in one thousand different directories and paste it into a single file. Using a GUI, you'd not only be clicking for hours at your desk, but, chances are you'd also make mistakes. This is where we take advantage of the Unix shell, which is both a **command-line interface** (CLI) and a scripting language.  This allows repetitive tasks to be automated and fast. Using the shell to write a *script* - which is a file with a sequence of commands - the task in the literature example can be accomplished in seconds.

### The Shell

The most popular Unix shell is Bash (the Bourne Again SHell — so-called because it’s derived from a shell written by Stephen Bourne). Bash is the default shell on most modern implementations of Unix and in most packages that provide Unix-like tools for Windows.  In addition, the command line is often the easiest way to interact with remote machines, supercomputers, and other resources such as the HPCC.

While a GUI presents you with choices to select, Bash choices are not automatically presented to you, so you must learn a few commands and build your vocabulary to work in the shell. However, unlike a spoken language, a small number of commands will get you a long way, and we’ll cover the essentials today.

Now, we are going to learn Bash commands using a narrative with data.  We could use specific research; for example, I recently used Bash to scrape a few hundred webpages.  But, using an example like that won't cover all of the basic commands you should have in your toolbelt.  Instead, we use a fictitious narrative that contains an authentic representation of what many researchers encounter in their day-to-day work. We've just packaged the data in this narrative:


## Nelle's Pipeline: A Typical Problem

Nelle Nemo, a marine biologist,
has just returned from a six-month survey of the
[North Pacific Gyre](http://en.wikipedia.org/wiki/North_Pacific_Gyre),
where she has been sampling gelatinous marine life in the
[Great Pacific Garbage Patch](http://en.wikipedia.org/wiki/Great_Pacific_Garbage_Patch).
She has 1520 samples that she's run through an assay machine to measure the relative abundance of 300 proteins.
She needs to run these 1520 files through an imaginary program she inherited called `goostats.sh`.
On top of this huge task, she has to write up results by the end of the month so her paper can appear in a special issue of *Aquatic Goo Letters*.

The bad news is that if she has to run `goostats.sh` by hand using a GUI,
she'll have to select and open a file 1520 times.
If `goostats.sh` takes 30 seconds to run each file, the whole process will take more than 12 hours of Nelle's attention.
With the shell, Nelle can instead write a script so her computer will complete this mundane task while she focuses her attention on writing her paper.  As a bonus, once she has written her script and workflow, she will be able to use it again whenever she collects more data.

So, let's get started by opening our shell program.  I'm going to open Git-Bash on my windows machine; if you're using a mac, you can type "terminal" to open the terminal.

