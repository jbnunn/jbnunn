# Neovim Configuration

My personal Neovim configuration using LazyVim as a base with custom modifications.

## Installation

To use this configuration:

```bash
# Backup your existing config (if any)
mv ~/.config/nvim ~/.config/nvim.backup

# Clone or symlink this configuration
ln -s /path/to/this/nvim ~/.config/nvim

# Or copy the files
cp -r nvim/ ~/.config/nvim/
```

## Structure

- `init.lua` - Main configuration entry point
- `lua/config/` - Core configuration files
  - `autocmds.lua` - Auto commands
  - `keymaps.lua` - Key mappings
  - `lazy.lua` - Lazy.nvim plugin manager setup
  - `options.lua` - Neovim options
  - `no-completion.lua` - Completion configuration
- `lua/plugins/` - Plugin configurations
  - `disable-completion.lua` - Completion disabling
  - `leap.lua` - Leap motion plugin
  - `markdown-preview.lua` - Markdown preview
  - `example.lua` - Example plugin configurations

## Features

- Based on LazyVim
- Custom key mappings
- Markdown preview support
- Motion enhancements with Leap
- Configurable completion settings

## Requirements

- Neovim >= 0.9.0
- Git
- A Nerd Font (optional, for icons)
