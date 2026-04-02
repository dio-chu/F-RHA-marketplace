# f-rha Plugin

A Claude Code plugin providing skills for the f-rha React component library.

## Structure

```
F-RHA/
├── .claude-plugin/
│   └── plugin.json       # Plugin manifest
├── CHANGELOG.md
├── README.md
└── skills/
    ├── components/
    │   ├── button/
    │   │   ├── .claude-plugin/plugin.json
    │   │   └── skills/button/SKILL.md
    │   ├── dialog/
    │   │   ├── .claude-plugin/plugin.json
    │   │   └── skills/dialog/SKILL.md
    │   ├── input/
    │   │   ├── .claude-plugin/plugin.json
    │   │   └── skills/input/SKILL.md
    │   └── radio/
    │       ├── .claude-plugin/plugin.json
    │       └── skills/radio/SKILL.md
    └── hooks/
        ├── use-debounce/
        │   ├── .claude-plugin/plugin.json
        │   └── skills/use-debounce/SKILL.md
        └── use-local-storage/
            ├── .claude-plugin/plugin.json
            └── skills/use-local-storage/SKILL.md
```

## Skills

### Components

| Skill | Description |
|-------|-------------|
| `f-rha-button` | Button component with variants (primary, secondary, outline) and sizes |
| `f-rha-dialog` | Modal dialog with overlay, title, footer, and keyboard close support |
| `f-rha-input` | Text input with label, placeholder, error message, and disabled state |
| `f-rha-radio` | Radio button group for single-selection with per-option disabled support |

### Hooks

| Skill | Description |
|-------|-------------|
| `f-rha-use-debounce` | Debounce a rapidly changing value to reduce re-renders or API calls |
| `f-rha-use-local-storage` | Persist React state to localStorage with JSON serialization |

## Usage

After installation, Claude will automatically use these skills when you ask about f-rha components or hooks.

```jsx
import { Button, Dialog, Input, Radio } from "f-rha";
import { useDebounce, useLocalStorage } from "f-rha";
```
