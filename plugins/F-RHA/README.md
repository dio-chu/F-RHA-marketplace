# f-rha

A collection of React UI components and hooks for the f-rha library.

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

## Installation

Install via Claude Code plugin manager:

```bash
claude plugin install f-rha
```

## Usage

After installation, Claude will automatically use these skills when you ask about f-rha components or hooks.

```jsx
import { Button, Dialog, Input, Radio } from "f-rha";
import { useDebounce, useLocalStorage } from "f-rha";
```
