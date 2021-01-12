# Preface

Extra runners for asyncrun to run your command in:

- new gnome-terminal window.
- new gnome-terminal panel.
- new xterm window.
- new [floaterm](https://github.com/voldikss/vim-floaterm) window.
- different tmux panes.
- the [terminal_help](https://github.com/skywind3000/vim-terminal-help) window.

## Supported Runners

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

Run command in a new gnome-terminal tab:

```VimL
:AsyncRun -mode=term -pos=gnome_tab  ls -la
```

NOTE: `-pos=external` is an alias of `-pos=gnome` on Linux.

### Xterm

Run command in a new `xterm` window:

```VimL
:AsyncRun -mode=term -pos=gnome_tab  ls -la
```

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

### Tmux

Run command in another tmux panel ([vimux](https://github.com/benmills/vimux) is required):

```VimL
:AsyncRun -mode=term -pos=tmux  ls -la
```

### Terminal Help

Run command in the [terminal_help](https://github.com/skywind3000/vim-terminal-help) window:

```VimL
:AsyncRun -mode=term -pos=termhelp  ls -la
```

## Help Required

- [ ] iterm2 runner
- [ ] terminal.app runner
- [ ] windows terminal runner

## Credit

TODO

