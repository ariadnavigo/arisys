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

## arimail - Start email setup with IMAP support

This script launches all commands required to an email setup based on neomutt
and isync, such that everything is guaranteed to be sync'ed up, including
delete operations.

It requires setting up ``$IMAP_CONFIG`` to isync's configuration path.

Dependencies:
1. [neomutt](https://neomutt.org)
2. [isync](https://isync.sourceforge.io/)

## aristatus - swaybar script

This script is in charge of the information I want to be printed out on sway's
status bar.

It shows information from these programs, so all of these are required:
1. [cras](https://sr.ht/~arivigo/cras)
2. [schain](https://sr.ht/~arivigo/schain)
3. [iwd](https://iwd.wiki.kernel.org/)
4. [ALSA](https://www.alsa-project.org)

## sfeedbar - sfeed integration into bemenu

This scripts creates a menu from RSS feeds parsed by sfeed. It also allows 
retrieval of updated RSS feeds.

This script assumes sfeed to be set up like this, which is **not** the default
configuration. Please refer to sfeed's documentation to set it up like this:

* ``$HOME/.config/sfeed/sfeedrc``: location of sfeed's master config file
* ``$HOME/.cache/sfeed/feeds/``: sfeed's cache.

Dependencies:
1. [sfeed](https://codemadness.org/git/sfeed/log.html)
2. [bemenu](https://github.com/Cloudef/bemenu)

## Licenses

apps-menu, arimail, aristatus, and sfeedbar are published under an 
MIT/X11/Expat-type License. See ``LICENSE`` file for copyright and license 
details.
