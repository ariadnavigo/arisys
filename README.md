# arisys - Ariadna's system scripts

These are a series of POSIX shell scripts that I use to create my own working 
environment on my personal computer. Each script is independent from each 
other, except where explicitly noted, and has their own unique set of 
requirements. So please refer to each script's section below if you're planning 
to use any of these.

## Installation

I'm not providing a Makefile for this repo, to avoid giving the impression of
any sorts of support in that regard whatsoever. Do as I do: manually install 
these scripts somewhere in your ``$PATH``. If you want to know where I install
these, it's under ``/usr/local/bin``.

## apps-menu - Automatically generated applications menu

This script reads a list of applications from a file and generates from it a 
menu to run any of those listed commands on sway. Very handy if assigned to a 
key binding.

Dependencies:
1. [sway WM](https://swaywm.org/)
2. [bemenu](https://github.com/Cloudef/bemenu)

## aristatus - swaybar script

This script is in charge of the information I want to be printed out on sway's
status bar.

It shows information from these programs, so all of these are required:
1. [cras](https://github.com/ariadnavigo/cras)
2. [schain](https://github.com/ariadnavigo/schain)
3. [iwd](https://iwd.wiki.kernel.org/)
4. [ALSA](https://www.alsa-project.org)

## cras-menu - Menu for simple management of cras task lists

This script launches a bemenu menu that shows all tasks in your default cras
task list file (i.e. the file set on the ``CRAS_DEF_FILE`` environment
variable). Selecting any of the entries will toggle its status between
**[TODO]** and **[DONE]**.

Dependencies:
1. [cras](https://github.com/ariadnavigo/cras)
2. [bemenu](https://github.com/Cloudef/bemenu)

## Licenses

apps-menu, arimail, aristatus, and sfeedbar are published under an 
MIT/X11/Expat-type License. See ``LICENSE`` file for copyright and license 
details.
