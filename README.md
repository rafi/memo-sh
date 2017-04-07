# memo-sh

Easy and fun management of your memos and notes.
Inspired by [github.com/mattn/memo](https://github.com/mattn/memo)

## Features

* Create memos with custom path formats, e.g. `%Y-%m/%d/{SLUG}.md`
* Displays a tree hierarchy of your memos
* Quickly edit a memo with fuzzy selectors like
  [`fzf`](https://github.com/junegunn/fzf),
  [`peco`](https://github.com/peco/peco), etc.
* Fast grep search throughout memos with `ag`, `ack`, `grep`, etc.

## Requirements

* [`tree`](http://mama.indstate.edu/users/ice/tree/), or change `$MEMO_TREE`
* [`the-silver-searcher`](https://github.com/ggreer/the_silver_searcher),
  or change `$MEMO_GREP`
* `$EDITOR` set to your favorite editor

## Install

Simply copy the single script, for example:
```sh
$ cd ~/.local/bin
$ curl -LO https://github.com/rafi/memo-sh/raw/master/memo
$ chmod ug+x memo
```

## Usage

```txt
memo [global options] <command> [command options]

COMMANDS:
  new, n     create memo
  list, l    list memo
  edit, e    edit memo
  delete, d  delete memo
  grep, g    grep memo
  config, c  configure
  serve, s   serve memos over http
  help, h    list of commands

GLOBAL OPTIONS:
  --help, -h      show help
  --disable-yaml  disable yaml matter
  --version, -v   print the version
```

## Configuration

Configuration via environment-variables:

- `EDITOR` - Preferred user editor
- `MEMO_DIR` - Base directory for all memos, _default: `~/.local/share/memo`_
- `MEMO_FMT` - Format for new memos, _default: `%Y-%m/%d-{SLUG\}.md`_
- `MEMO_GREP` - Command to use for grep, _default: `ag` (the silver searcher)_
- `MEMO_TREE` - Command to use for list, _default: `tree -FR --dirsfirst`_
- `MEMO_SELECT` - Command to use for selecting a single memo, _default: `fzf`_

## Credits

Inspiration came from [memo](https://github.com/mattn/memo)
by Yasuhiro Matsumoto (a.k.a. @mattn)

## Similar Projects

- [Memo](https://github.com/mattn/memo) -
  Go application with internal Markdown server
- [Notes](https://github.com/pimterry/notes)

## License

MIT License, created by Rafael Bodill
