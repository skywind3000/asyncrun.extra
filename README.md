# What is it ?

Extra runners for [asyncrun](https://github.com/skywind3000/asyncrun.vim) to run your command in `gnome-terminal`, `tmux`, `floaterm` and more:

| Runner | Description |
|-|-|
| [gnome](#gnome-terminal) | run command in a new gnome-terminal window |
| [gnome-tab](#gnome-terminal) | run command in a new gnome-terminal tab |
| [xterm](#xterm) | run command in a new xterm window |
| [external](#external) | run command in cmd.exe / gnome-terminal / xterm if possible |
| [floaterm](#floaterm) | run command in a [floaterm](https://github.com/voldikss/vim-floaterm) window |
| [floaterm-reuse](#floaterm) | run command in a reusable [floaterm](https://github.com/voldikss/vim-floaterm) window |
| [tmux](#tmux) | run command in another tmux pane |
| [termhelp](#termhelp) | run command in the [terminal_help](https://github.com/skywind3000/vim-terminal-help) window |

## Installation

For vim-plug:

```VimL
Plug 'skywind3000/asyncrun.vim'
Plug 'skywind3000/asyncrun.extra'
```

[asyncrun](https://github.com/skywind3000/asyncrun.vim) version 2.7.8 or latter is required.


## Available Runners

### Gnome-terminal

Run command in a new `gnome-terminal` window:

```VimL
:AsyncRun -mode=term -pos=gnome  ls -la
```

GVim Screencast:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_gnome_gvim.gif)

Terminal Vim:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_gnome.gif)

Run command in a new gnome-terminal tab:

```VimL
:AsyncRun -mode=term -pos=gnome_tab  ls -la
```

Screencast:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_gnome_tab.gif)

NOTE: `-pos=external` is an alias of `-pos=gnome` on Linux.

### Xterm

Run command in a new `xterm` window:

```VimL
:AsyncRun -mode=term -pos=xterm  ls -la
```

Screencast:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_xterm.gif)

### External

The default `external` runner in asyncrun can run commands in cmd.exe:

```VimL
:AsyncRun -mode=term -pos=external  echo Hello, World !!
```

The command above runs in cmd.exe:

![](https://github.com/skywind3000/images/raw/master/p/asynctasks/demo-4.png)

The default `external` runner in asyncrun works on Windows only, and will do nothing if you are using Linux.

This plugin provide an enhanced version of `external` runner which detect what OS currently in used and choose an appropriate external terminal (`cmd.exe`, `gnome-terminal` or `xterm`) when possible.

### Floaterm

Run command in [floaterm](https://github.com/voldikss/vim-floaterm):

```VimL
:AsyncRun -mode=term -pos=floaterm  ls -la
```

With more `floaterm` options:

```VimL
:AsyncRun -mode=term -pos=floaterm -position=bottomright -width=0.4  ls -la
:AsyncRun -mode=term -pos=floaterm -focus=0  ls -la
```

Gif:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_floaterm.gif)

**Hint**: try `-pos=floaterm_reuse` if you want to reuse existing floaterm window.

### Tmux

Run command in another tmux panel ([vimux](https://github.com/benmills/vimux) is required):

```VimL
:AsyncRun -mode=term -pos=tmux  ls -la
```

Gif:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_tmux.gif)

### Terminal Help

Run command in the [terminal_help](https://github.com/skywind3000/vim-terminal-help) window:

```VimL
:AsyncRun -mode=term -pos=termhelp  ls -la
```

Gif:

![](https://github.com/skywind3000/images/raw/master/p/asyncrun_extra/p_help.gif)

## Help Required

- [ ] iterm2 runner
- [ ] terminal.app runner
- [ ] windows terminal runner

## Credit

TODO

