Loadclip
========

This script allows you to load text into your clipboard.  It maintains a JSON
dictionary in `~/.loadclip.json`.  Run `loadclip [key]` to load the matching
JSON value into the clipboard.  It's convenient for quickly being able to paste
long or difficult to type text wherever you'd like.

If you run `loadclip --popup`, the program will pop up a little prompt.  Type a
key, hit enter, and it will copy the value into the clipboard.  This is pretty
useful for if you were to bind the program to a keyboard shortcut.

If you run `loadclip --new-key`, the program will prompt you for a key and a
value, and then save these into the dictionary..  This is useful for correctly
escaping Unicode characters in strings, since it does so automatically.

Installation
------------

1. You'll need to install `tk` and `pyperclip`.  There may be a Ubuntu package
   for those, I don't really know.  In Arch: `pacman -S python-pyperclip tk`
   works.
2. You can either copy my included `loadclip.json` to `~/.loadclip.json`,
   symlink it in, or create your own.  Just make sure you put one there.
3. Put `loadclip` into your PATH (typically in `~/bin` or `~/.local/bin`).
   Symlinking would be best, but copying works too.
4. Once it's in your path, you can start using it!
