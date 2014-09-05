# viack

Some words which help the interface beween [ack](http://beyondgrep.com/) and [vim](https://duckduckgo.com/l/?kh=-1&uddg=http%3A%2F%2Fwww.vim.org%2F).

## Usage

viack allows lines in [bash](https://www.gnu.org/software/bash/) like

```shell
ap -w main -v
```

which tells ack to search all python files for the word main, and tells vim to open all those files searching for the word main

Also allows lines like

```shell
vai sys
```

which searches all python files for any "import sys" or "from sys import", and vims those files with that search

This code [WFM](http://www.urbandictionary.com/define.php?term=wfm) and I use it daily, but [caveat lector](http://www.urbandictionary.com/define.php?term=ymmv)

## Install

```shell
git clone https://github.com/jalanb/viack.git
source viack/viack
```

## Options
[RTFS](https://github.com/jalanb/viack/blob/master/viack)

## How does it work?

Makes [bash functions with abbreviated names](https://github.com/jalanb/viack/blob/master/viack), all of which [eventually](https://github.com/jalanb/viack/blob/master/viack#L122) hand over to [a python program](https://github.com/jalanb/viack/blob/master/viack.py) which interprets arguments (bit messy - separating args for viack/ack/vim), and does some conversion of ack to vim regexps, before sending the correct vim command to stdout. Bash captures that and runs it.

## Readers who got this far went on to view:

* [Thomas Sibley](http://tsibley.net/)'s [viack](https://github.com/tsibley/viack)
* [Miles Whittaker](https://plus.google.com/+MilesWhittaker_mjwhitta/about)'s [zoom](https://bitbucket.org/mjwhitta/zoom)
* [Sampson Chen](http://sampsonchen.com/)'s [sack](https://github.com/sampson-chen/sack)