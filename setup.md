---
layout: page
title: "Setup"
permalink: /setup/
---

## Required software
To participate in the python workshop, you will need access to the software described below: 

- **Python version 3.x** : [Python](https://python.org) is a popular language for scientific computing, and great for general-purpose programming as well. Installing all of its scientific packages individually can be a bit difficult, however, so we recommend the all-in-one installer [Anaconda](https://www.continuum.io/anaconda). Regardless of how you choose to install it, please make sure you install Python version 3.x (e.g., 3.4 is fine). Also, please set up your python environment at least a day in advance of the workshop.  If you encounter problems with the installation procedure, ask your workshop organizers via e-mail for assistance so you are ready to go as soon as the workshop begins.
- **IDE** : An IDE is a program that you use to write, test and execute python programs. There are many IDE's on the market but we recommend [Pyzo](https://pyzo.org) because it's interface is simple and it provides a good compromise between simplicity and functionality for beginners. 

## Installing Python Using Anaconda




#### Windows - [Video tutorial](https://www.youtube.com/watch?v=xxQ0mzZ8UvA)

1. Open [http://continuum.io/downloads](http://continuum.io/downloads#_windows) 
    with your web browser.

2. Download the Python 3 installer for Windows.

3. Double-click the executable and install Python 3 using _MOST_ of the
    default settings. The only exception is to check the 
    **Make Anaconda the default Python** option.

#### Mac OS X - [Video tutorial](https://www.youtube.com/watch?v=TcSAln46u9U)

1. Open [http://continuum.io/downloads](http://continuum.io/downloads#_macosx) 
    with your web browser.

2. Download the Python 3 installer for OS X.

3. Install Python 3 using all of the defaults for installation.

#### Linux
Note that the following installation steps require you to work from the shell. 
If you run into any difficulties, please request help before the workshop begins.

1.  Open [http://continuum.io/downloads](http://continuum.io/downloads#_unix) with your web browser.

2.  Download the Python 3 installer for Linux.

3.  Install Python 3 using all of the defaults for installation.

    a.  Open a terminal window.

    b.  Navigate to the folder where you downloaded the installer

    c.  Type

    ~~~
    $ bash Anaconda3-
    ~~~
    {: .source}

    and press tab.  The name of the file you just downloaded should appear.

    d.  Press enter.

    e.  Follow the text-only prompts.  When the license agreement appears (a colon
        will be present at the bottom of the screen) hold the down arrow until the 
        bottom of the text. Type `yes` and press enter to approve the license. Press 
        enter again to approve the default location for the files. Type `yes` and 
        press enter to prepend Anaconda to your `PATH` (this makes the Anaconda 
        distribution the default Python).

## Installing Pyzo

#### Windows

1. Open [http://www.pyzo.org/start.html](http://www.pyzo.org/start.html) with your web browser.
2. Under step 1, click on the pyzo for windows link.
3. Click next.
4. Click next.
5. Click next.
6. Click next.
7. Wait for the program to finish installing then click finish.

#### Mac Osx

1. Open [http://www.pyzo.org/start.html](http://www.pyzo.org/start.html) with your web browser.
2. Under step 1, click on the pyzo for OSX link.
3. Right click the installer file and then click open.
4. Right click the file that says pyzo and click open.
5. When it has finished installing open pyzo.

#### Ubuntu

1. Open [http://www.pyzo.org/start.html](http://www.pyzo.org/start.html) with your web browser.

## Getting the Data

The data we will be using is taken from the [gapminder](http://gapminder.org) dataset.
To obtain it, download and unzip the file 
[python-novice-gapminder-data.zip][data-zip].
In order to follow the presented material, you should launch a Jupyter 
notebook in the "data" directory (see [Starting Python](#Starting-Python)).

Head to the [first lesson](https://uoa-eresearch.github.io/python_intro_tutorial/01/) to check that you've set up the software correctly.

[data-zip]: {{site.github.repository_url}}/blob/gh-pages/files/python-novice-gapminder-data.zip?raw=true
