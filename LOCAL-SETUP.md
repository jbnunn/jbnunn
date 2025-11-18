# macOS Local Development Setup

This document describes the tools, configs, and workflows I use on my macOS desktop. I've highly customized it to feel more like Arch Linux, while retaining the benefits of being on Mac hardware.

![Desktop](./images/desktop.png)

## Core Tools

### Neovim

[Neovim](https://neovim.io/) - Neovim is a modern, highly customizable fork of the Vim text editor designed to improve usability and extensibility. It retains Vim's powerful core while offering a more modern architecture, a more robust plugin system, better stability, and asynchronous operations.

### FZF

[FZF](https://github.com/junegunn/fzf) - An interactive filter program for any kind of list: files, command history, processes, git commits, etc.

### Bat

[Bat](https://github.com/sharkdp/bat) - A command-line tool that acts as a more powerful alternative to the traditional `cat` command for viewing file contents. It offers enhanced features like syntax highlighting, line numbers, and Git integration, while still working as a drop-in replacement for cat in many situations, including when piping output to other programs.

### Ghostty

[Ghostty](https://ghostty.org/) - After years of using iTerm2, I'm trying Ghostty. It's a fast, native, GPU-accelerated terminal emulator with a focus on performance and simplicity. Built in Zig, it offers excellent macOS integration while keeping resource usage minimal.

### SketchyBar

[SketchyBar](https://github.com/FelixKratz/SketchyBar) - A highly customizable status bar replacement for macOS. It allows for extensive modification, letting me add dynamic elements like CPU usage, battery levels, custom icons, etc.

Screenshot Placeholder:
![SketchyBar](./images/sketchybar.png)

### Yabai

[Yabai](https://github.com/koekeishiya/yabai) - Tiling window manager for macOS. It gives me a look and feel I've become accustomed to after using [Hyprland](https://wiki.archlinux.org/title/Hyprland) on Arch Linux and [Omarchy](https://www.omarchy.org).

Screenshot Placeholder:
![Yabai Tiling](./images/yabai.png)

### skhd

[skhd](https://github.com/jackielii/skhd.zig) - A simple hotkey daemon for macOS. It lets me bind keyboard shortcuts to system commands and scripts, and works seamlessly with Yabai for window management shortcuts, letting me control my entire desktop environment from the keyboard. My favorite shortcut lets me use cmd + return to open a new terminal window:

```
cmd - return : ghostty
```

### Zsh

[Zsh](https://www.zsh.org/) - My shell of choice for at least the past decade.

### Starship

[Starship](https://starship.rs/) - A minimal, fast, and customizable terminal prompt. Works great with Zsh and keeps my prompt clean while still being informative.

### LazyGit

[LazyGit](https://github.com/jesseduffield/lazygit) - Simple terminal UI for Git. It feels more intuitive than other Git UIs I've tried in editors like VS Code.

### Stow

[GNU Stow](https://www.gnu.org/software/stow/) - A symlink farm manager that makes it easy to manage dotfiles. Instead of manually copying configuration files around, Stow creates symlinks from a central repository to their proper locations in the home directory. This makes version control and deployment of dotfiles across multiple machines straightforward and reversible.
