# dotcursor
Like dotemacs, but with less Lisp and more existential dread. 🤖

## What's Inside

A collection of my most useful Cursor AI rules, commands, and skills.

### Commands (`.cursor/commands/`)
Custom commands that define workflows:
- **code-review.md** - Comprehensive code review checklist (data flow, a11y, tests, etc.)
- **implement.md** - Bottom-up, component-based implementation workflow
- **pr.md** - Automated pull request creation process
- **visualize.md** - Use mermaid diagram to visualize the data lineage of the referenced code or project

### Rules (`.cursor/rules/`)
AI behavior guidelines that are always applied:
- **general.mdc** - Never commit without explicit approval
- **pr-creation.mdc** - Clean, minimal PR creation output format

### Skills (`.cursor/skills/`)
Reusable agent skills:
- **capture-skill** - Capture learnings, patterns, or workflows from conversations into reusable skills

### Keybindings (`keybindings.json`)
Custom keyboard shortcuts for Cursor:
- Emacs-style navigation and editing commands
- Quick file/symbol navigation
- Composer mode activation
- Definition jumping and more

## Setup

This repo is designed to be the source of truth for global Cursor configuration. Symlink the directories to make them globally available:

```bash
# Commands (globally available /commands)
ln -s /path/to/dotcursor/.cursor/commands ~/.cursor/commands

# Skills (globally available skills)
ln -s /path/to/dotcursor/.cursor/skills ~/.cursor/skills
```

To use the keybindings, copy `keybindings.json` to:
- macOS/Linux: `~/.config/Cursor/User/keybindings.json`
- Or use Cursor's UI: Preferences → Keyboard Shortcuts → Open Keyboard Shortcuts (JSON)
