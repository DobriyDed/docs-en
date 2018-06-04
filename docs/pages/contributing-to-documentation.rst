Contributing to documentation
=============================

Here's a handy cheatsheet for the markup in this documentation

https://github.com/ralsina/rst-cheatsheet/blob/master/rst-cheatsheet.rst

Github
------

If you are ok with using a web interface or just want to make some small change you can use the 'Edit on Github' buttons

Local Build
-----------

If you'd rather work on your own machine, in a more powerful editor, here are some steps to do this

Make sure python & pip are installed

Install Sphinx::

    pip install sphinx sphinx-autobuild sphinx_rtd_theme

Create a new folder::

    mkdir csmm-docs
    cd csmm-docs

Clone the documentation repository to your machine::

    git init
    git pull https://github.com/niekcandaele/CSMM-issues

Write some docs!

Build your new version::

     make html

Open index.html from the _build folder to see the docs.

Autmatically rebuild when a file changes::

    sphinx-autobuild . _build/html



Once you have changes to add, open up a pull request!

