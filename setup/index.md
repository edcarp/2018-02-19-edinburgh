---
layout: page
title: Testing Setup
root: ..
---

This directory contains scripts for testing your machine to make sure
you have the software you'll need for your workshop installed.

To run the scripts, you will first need to open a shell:

* Linux users: run the Terminal program, which can be found via the applications menu or the search bar.
* Mac OS users:
  - Either: Go to your Applications. Within Applications, open the Utilities folder. Locate Terminal in the Utilities folder and open it.
  - Or: Use the Mac "Spotlight" computer search function. Search for: Terminal and press [Enter].
* Windows users:
  - Either: Select Start => Git => Git Bash
  - Or: Enter "Git Bash" into the Windows search box.

### Check you have the required Python version

1.  Download [swc-installation-test-1.py](swc-installation-test-1.py).
2.  Move swc-installation-test-1.py into your home directory.
    - Windows users: if using Git Bash, your home directory is `C:\Users\<your-user-name>`.
3.  Run it from the shell:

    ~~~
    $ python swc-installation-test-1.py
    ~~~
    
If all is well you should see:
    
~~~
Passed
~~~

### Check you have the required tools

1.  Download [swc-installation-test-2.py](swc-installation-test-2.py).
2.  Move swc-installation-test-2.py into your home directory.
    - Windows users: if using Git Bash, your home directory is `C:\Users\<your-user-name>`.
3.  Run it from the shell:

    ~~~
    $ python swc-installation-test-2.py
    ~~~

If all is well you should see something like:
    
~~~
check command line shell (virtual-shell)...	pass
check text/code editor (virtual-editor)...	pass
check web browser (virtual-browser)...	pass
check Git (git)...	pass
check PyPI installer (virtual-pypi-installer)...	pass
check Setuptools (setuptools)...	pass
check Nose (nosetests)...	pass
check Nose Python package (nose)...	pass
check py.test...	pass
check pytest Python package (pytest)...	pass
check SQLite 3 (sqlite3)...	pass
check SQLite Python package (sqlite3-python)...	pass
check Python version (python)...	pass
check IPython script (ipython)...	pass
check IPython Python package (IPython)...	pass
check Argparse (argparse)...	pass
check NumPy (numpy)...	pass
check SciPy (scipy)...	pass
check Matplotlib (matplotlib)...	pass
check Pandas (pandas)...	pass

Successes:

command line shell (virtual-shell) Bourne Again Shell (bash) 4.3.48
text/code editor (virtual-editor) XEmacs (xemacs) 21.4
web browser (virtual-browser) Firefox (firefox) 57.0.4
Git (git) 2.7.4
PyPI installer (virtual-pypi-installer) pip 9.0.1
Setuptools (setuptools) 36.5.0.post20170921
Nose (nosetests) 1.3.7
Nose Python package (nose) 1.3.7
py.test 3.2.1
pytest Python package (pytest) 3.2.1
SQLite 3 (sqlite3) 3.20.1
SQLite Python package (sqlite3-python) 3.6.3 |Anaconda, Inc.| (default, Oct 13 2017, 12:02:49) 
[GCC 7.2.0]
Python version (python) 3.6.3 |Anaconda, Inc.| (default, Oct 13 2017, 12:02:49) 
[GCC 7.2.0]
IPython script (ipython) 6.1.0
IPython Python package (IPython) 6.1.0
Argparse (argparse) 1.1
NumPy (numpy) 1.13.3
SciPy (scipy) 0.19.1
Matplotlib (matplotlib) 2.1.0
Pandas (pandas) 0.20.3
~~~

(the exact version numbers may differ)

For Windows users, if you have failures relating to your web browser e.g.

~~~
check web browser (virtual-browser)...  fail
...
check IPython Python package (IPython)...       fail
...
Failures:

check for web browser (virtual-browser) failed:
  web browser (virtual-browser) requires at least one of the following dependenc
ies
  For instructions on installing an up-to-date version, see
  http://software-carpentry.org/setup/
  causes:
  check for Firefox (firefox) failed:
  ...
  check for Google Chrome (google-chrome) failed:
  ...
  check for Chromium (chromium) failed:
  ...
  check for Safari (safari) failed:

check for IPython Python package (IPython) failed:
  some dependencies for IPython Python package (IPython) were not satisfied
  For instructions on installing an up-to-date version, see
  http://ipython.org/install.html
  causes:
  check for IPython-compatible web browser (virtual-browser-ipython) failed:
    IPython-compatible web browser (virtual-browser-ipython) requires at least o
ne of the following dependencies
    ...
    check for Firefox for IPython (firefox-for-ipython) failed:
    ...
    check for Google Chrome for IPython (google-chrome-for-ipython) failed:
    ...  
    check for Chromium for IPython (chromium-for-ipython) failed:
    ...
    check for Safari for IPython (safari-for-ipython) failed:
    ...
~~~

then, so long as you know you have a recent version of Firefox or Google Chrome or Chromium or Safari installed, then these can be ignored.

For all users, if you see other failures:

~~~
$ python swc-installation-test-2.py
check virtual-shell...  fail
...
check for command line shell (virtual-shell) failed:
command line shell (virtual-shell) requires at least one of the following dependencies
For instructions on installing an up-to-date version, see
http://software-carpentry.org/setup/
causes:
check for Bourne Again Shell (bash) failed:
could not find 'bash' executable for Bourne Again Shell (bash)
For instructions on installing an up-to-date version, see
http://software-carpentry.org/setup/
...
~~~

then, follow the suggestions to try and install any missing software. For additional troubleshooting information, you can use the `--verbose` option:

~~~
$ python swc-installation-test-2.py --verbose
check virtual-shell...  fail
...
==================
System information
==================
os.name            : posix
...
~~~
