# dotcursor
Like dotemacs, but with less Lisp and more existential dread. 🤖

## What's Inside

A collection of my most useful Cursor AI rules and commands.

### Commands (`.cursor/commands/`)
Custom commands that define workflows:
- **implement.md** - Bottom-up, component-based implementation workflow
- **pr.md** - Automated pull request creation process

### Rules (`.cursor/rules/`)
AI behavior guidelines that are always applied:
- **general.mdc** - Never commit without explicit approval
- **pr-creation.mdc** - Clean, minimal PR creation output format

### Keybindings (`keybindings.json`)
Custom keyboard shortcuts for Cursor:
- Emacs-style navigation and editing commands
- Quick file/symbol navigation
- Composer mode activation
- Definition jumping and more

## Usage

Copy the `.cursor/` directory (or individual files) to your project.

To use the keybindings, copy `keybindings.json` to:
- macOS/Linux: `~/.config/Cursor/User/keybindings.json`
- Or use Cursor's UI: Preferences → Keyboard Shortcuts → Open Keyboard Shortcuts (JSON)
