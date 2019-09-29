# Sublime Jump Along Indent #

[![Sublime Version](http://img.shields.io/badge/sublime_text-3-orange.svg?style=flat)](http://www.sublimetext.com/3)
[![Build Status](http://img.shields.io/travis/mwean/sublime_jump_along_indent/master.svg?style=flat)](https://travis-ci.org/mwean/sublime_jump_along_indent)
[![Release Version](http://img.shields.io/badge/release-v0.4.0-blue.svg?style=flat)](https://github.com/mwean/sublime_jump_along_indent/releases/latest)
[![MIT Licesne](http://img.shields.io/badge/license-MIT-red.svg?style=flat)](https://github.com/mwean/sublime_jump_along_indent/blob/master/LICENSE)

## Description ##

A Sublime Text 3 plugin to move the cursor to next/previous line at the same indentation level as the current line.

There are two commands: `jump_next_indent` and `jump_prev_indent`.

![Before jumping downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/pre_jump.png) → ![After jumping downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/post_jump.png)

If the cursor is to the left of an indented line, it will jump to the next line that is at that level or less.

![Before jumping downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/pre_jump_inset.png) → ![After jumping downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/post_jump_inset.png)

If there are several lines on the same indent level, the cursor will jump to the beginning or end of the block of lines.

![Before jumping downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/pre_jump_block.png) → ![After jumping downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/post_jump_block.png)

### Extending selection ###

With the option `extend_selection: true` you can extend the selection while jumping:

![Before selecting downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/pre_jump.png) → ![After selecting downward](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/post_select.png)

### Jumping to a different indent level ###

You can also use the `indent_offset` option to jump to a more or less-indented line. For example, with `indent_offset = -1`:

![Before jumping up and out](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/pre_jump_out.png) → ![After jumping up and out](https://s3.amazonaws.com/mwean-github/sublime_jump_along_indent/post_jump_out.png)


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   add the following setting to your **`Package Control.sublime-settings`** file, if it is not already there
   ```js
   [
       ...
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
       ...
   ]
   ```
   * Note,
     the **`https://raw...`** line must to be added before the **`https://packagecontrol...`**,
     otherwise you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`JumpAlongIndent`** and press <kbd>Enter</kbd>

See also:
1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


## Usage ##

The plugin comes with a set of default keybindings:

  - `alt+up`: Jump to previous indented line
  - `alt+down`: Jump to next indented line
  - `alt+shift+up`: Jump to previous indented line and extend selection
  - `alt+shift+down`: Jump to next indented line and extend selection

## Credits ##

Some of the methods in `file_scanner.py` were adapted from the [VintageEx](https://github.com/SublimeText/VintageEx) plugin.
