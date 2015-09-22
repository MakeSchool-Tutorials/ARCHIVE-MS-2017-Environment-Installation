---
title: "Python Install Instructions"
slug: python-install-instructions
---

#Python Environment

Make sure you install the iOS environment first - the instructions assume you have, because you will need Command Line Tools and Homebrew installed already.

##Python 3

OS X comes with a version of Python (2.7) installed by default. We can call that the *system Python*. But that version is old! Python 3 was released in 2008, and it came with a bunch of syntax changes that were incompatible with 2.x versions of Python. This created a fork in the language, as many large Python projects (including many helpful libraries) didn't want to invest the time to convert to 3.x.  But that was then; it's now recommended that all new Python projects are made in Python 3.x. For more information, see [this article](https://wiki.python.org/moin/Python2orPython3). 

So we're going to install the newest Python.

> [info]
*These instructions are derived from [this great post](http://www.marinamele.com/2014/07/install-python3-on-mac-os-x-and-use-virtualenv-and-virtualenvwrapper.html)*.

Use Homebrew to install Python 3 and its dependencies:

	$ brew install python3
	
Once that's finished, you should be able to see which version of Python installed like this:

	$ python3 --version

That will also install the Python package manager, called `pip`, which can be used to download Python libraries. Because we're using Python 3, you should always use `pip3`, which is the Python 3 version.

##Virtualenv

By default, `pip` and `pip3` install packages into a directory used by Python system-wide. This can create problems, because different Python projects might be dependent on different versions of libraries. Upgrading a library on one project might break all of your other projects, which is a nightmare.

`virtualenv` is the solution to this problem. Here's the [official documentation](https://virtualenv.pypa.io/en/latest/), but the TL;DR is that for each project it creates a virtual environment in which packages are installed, and ensures that the project is not dependent on any packages outside the virtual environment. 

To install `virtualenv`, use the following command

	$ pip3 install virtualenv
	
As you create each Python project, you will also want to create an associated virtual environment in which you can install packages.

## Atom

Download and install Atom. Atom is a an open-source text editor maintained by Github, that we will use to write our Python source.

https://atom.io/

## Atom Python Packages

Follow the "Linter for Atom" and "Further customisation for Python to follow PEP8" instructions [here](http://www.marinamele.com/install-and-configure-atom-editor-for-python) to install a package that will give you live Python validation as you type.

**Note - You should replace all instanes of `pip` with `pip3` to make sure you're issuing commands to your new Python 3 install, and not the system Python.**