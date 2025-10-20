# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a tmux configuration repository located at `~/.config/tmux` on macOS. It contains a customized tmux setup with plugin management via TPM (Tmux Plugin Manager).

## Configuration File

**Main config:** `tmux.conf` - The primary tmux configuration file

**Location:** `~/.config/tmux/tmux.conf`

## Plugin Management

**Plugin Manager:** TPM (Tmux Plugin Manager)

**Installed plugins:**
- `tmux-plugins/tpm` - Plugin manager itself
- `tmux-plugins/tmux-sensible` - Basic tmux settings everyone can agree on
- `christoomey/vim-tmux-navigator` - Seamless navigation between tmux panes and vim splits
- `tmux-plugins/tmux-yank` - Copy to system clipboard
- `fabioluciano/tmux-tokyo-night` - Tokyo Night theme
- `tmux-plugins/tmux-resurrect` - Persist tmux sessions after computer restart
- `tmux-plugins/tmux-continuum` - Automatically saves sessions every 15 minutes

**Plugin installation:** After adding a new plugin to `tmux.conf`:
1. Add plugin line: `set -g @plugin 'author/plugin-name'`
2. Reload tmux config: `tmux source ~/.config/tmux/tmux.conf` (or `Prefix + :` then `source ~/.config/tmux/tmux.conf`)
3. Install plugin: `Prefix + I` (capital I)

**Plugin update:** `Prefix + U`

**Plugin removal:**
1. Remove/comment out plugin line from `tmux.conf`
2. Reload config
3. Uninstall: `Prefix + alt + u`

## Key Bindings

**Prefix:** `Ctrl + b` (default)

**Custom bindings:**
- `Ctrl + g` - Synchronize input to all panes in current window
- `Alt + Arrow` - Switch panes (no prefix needed)
- `Shift + Arrow` - Switch windows (no prefix needed)
- `Alt + H/L` - Previous/Next window (no prefix needed)
- `"` - Split window vertically (opens in current path)
- `%` - Split window horizontally (opens in current path)

**Vi-mode (copy mode):**
- `v` - Begin selection
- `Ctrl + v` - Rectangle toggle
- `y` - Copy selection and cancel

## Key Settings

- **Terminal:** `tmux-256color` with RGB color support
- **Mouse support:** Enabled
- **Base index:** Windows and panes start at 1 (not 0)
- **Window renumbering:** Automatic
- **Copy mode:** Vi key bindings
- **Session persistence:** Auto-save every 15 minutes, auto-restore on tmux start

## Reloading Configuration

After making changes to `tmux.conf`:
```bash
tmux source ~/.config/tmux/tmux.conf
```

Or from within tmux: `Prefix + :` then type `source ~/.config/tmux/tmux.conf`

## TPM Installation Path

TPM is installed at: `~/.config/tmux/plugins/tpm/` (gitignored, not tracked in this repo)
