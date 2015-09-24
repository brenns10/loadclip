---
---
<meta http-equiv="content-type" content="text/html; charset=utf-8">

Loadclip
========

A simple script to load any text into your clipboard.  Essentially, it maintains
a dictionary mapping shortcut names to more complicated text.  You run the
command `loadclip [shortcut]`, and the text appears in your clipboard.

The dictionary is stored in `~/.loadclip.json`.  I've included a copy of one
that associates "shrug" with ¯\\\_(ツ)_/¯.  Very useful.

If you have some text (like ¯\\\_(ツ)_/¯) that needs to be escaped in JSON, you
should use `loadclip --new-key`.  Otherwise, I'd just edit the JSON file, since
the `loadclip --new-key` script doesn't allow you to do multiline text (very
useful for addresses and stuff).

If you want a popup to prompt you for a shortcut, use `loadclip --popup`.

Installation
------------

1. You'll need to install `tk` and `pyperclip`.  There may be a Ubuntu package
   for those, I don't really know.  In Arch: `pacman -S python-pyperclip tk`
   works.

2. Make sure to copy the example `.loadclip.json` file into your home directory.

3. Put `loadclip` in your PATH.  It's easiest to do this in a local bin folder
   (`~/bin` or `~/.local/bin` are common).  You may need to add these to your
   path.  Do this by putting the following into your `~/.profile`:

       export PATH=$PATH:~/bin

4. Once it's in your path, you can start using it!
