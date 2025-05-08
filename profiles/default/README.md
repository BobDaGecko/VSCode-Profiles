# VSCode Profile: `default`

A global, general-purpose Visual Studio Code profile focused on enhancing the developer experience through consistency, readability, and productivity. This profile is language-agnostic and designed to serve as a base for more specific profiles.

---

## 🧩 Installed Extensions

Install with: `cat extensions.txt | xargs -L 1 code --install-extension`

| Extension                                               | Purpose                                         |
| ------------------------------------------------------- | ----------------------------------------------- |
| `dracula-theme.theme-dracula`                           | Clean, high-contrast UI theme                   |
| `pkief.material-icon-theme`                             | Intuitive file and folder icons                 |
| `esbenp.prettier-vscode`                                | Code formatting across many languages           |
| `streetsidesoftware.code-spell-checker`                 | Spell checking for code, markdown, and comments |
| `gruntfuggly.todo-tree`                                 | Highlights and tracks TODOs and FIXMEs          |
| `formulahendry.code-runner`                             | Run code snippets quickly in the editor         |
| `mhutchie.git-graph`                                    | Git visualization tool                          |
| `usernamehw.errorlens`                                  | Highlights errors and warnings inline           |
| `shardulm94.trailing-spaces`                            | Visualizes and removes trailing whitespace      |
| `oderwat.indent-rainbow`                                | Highlights nested indentation levels            |
| `quicktype.quicktype`                                   | Generate types from JSON data                   |
| `louiswt.regexp-preview`                                | Live preview for regular expressions            |
| `github.copilot`, `github.copilot-chat`                 | AI coding assistant                             |
| `github.vscode-github-actions`                          | GitHub Actions integration                      |
| `github.vscode-pull-request-github`, `github.remotehub` | GitHub pull requests and repo insights          |
| `ms-vscode-remote.*`                                    | WSL, SSH, and remote dev support                |
| `vsls-contrib.gistfs`                                   | Browse GitHub Gists as virtual file systems     |

---

## ⚙️ Key Settings Overview

### 🔧 Editor

- **Font Family**: `'JetBrainsMono Nerd Font Mono'`, fallback to `'Fira Code'`, `'Fira Mono'`, `Menlo`, `Monaco`, `'Courier New'`, `monospace`
- **Font Ligatures**: Enabled
- **Cursor Blinking**: `smooth`
- **Line Height**: `17`
- **Tab Size**: `2` (global default)
- **Insert Spaces**: Enabled (in language-specific overrides)
- **Format on Save**: Enabled
- **Default Formatter**: `esbenp.prettier-vscode`
- **Bracket Pair Colorization**: Enabled
- **Inline Suggestions**: Enabled
- **Minimap**: Disabled
- **Code Lens**: Enabled
- **Quick Suggestions**: Snippets no longer prevent quick suggestions

### 🧾 Files

- **Insert Final Newline**: Enabled
- **Trim Final Newlines**: Enabled
- **Auto Save**: Disabled (`off`)

### 🧪 Terminal

- **Font Family**: Matches editor font
- **Scrollback**: `5000` lines
- **Startup Directory**: `${workspaceFolder}`

### 🧵 Workbench

- **Editor: Highlight Modified Tabs**: Enabled
- **Color Theme**: `Dracula Theme`
- **Icon Theme**: `material-icon-theme`
- **Startup Editor**: `none`
- **Zoom Level**: `0`

### 🔍 Git

- **Commit Subject Length Validation**: Max 60 characters
- **Sync Confirmation**: Disabled

### 🐞 Debugging

- **Allow Breakpoints Everywhere**: Enabled

### 🔍 TODO Tree

#### Custom Highlights:

- `TODO`

  - Icon: `check`
  - Type: `line`

- `FIXME`
  - Foreground: `#ff0044`
  - Background: `#000000`
  - Icon Colour: `#ff0044`
  - Gutter Icon: `true`

#### Default Highlight:

- Icon: `alert`
- Type: `text`
- Foreground: `#ff00ff`
- Background: `#000000`
- Opacity: `50`
- Icon Colour: `#00bbff`
- Gutter Icon: `true`

### 📖 Spell Checker (Code Spell Checker)

- **Language**: `en`
- **User-defined Words**:
  - `kellen`
  - `siczka`
  - `bobdagecko`

---

### 🧩 Extensions Behavior

- **Ignore Recommendations**: `false` (extensions can still be recommended by VSCode)

---

## ✅ Recommended Use Cases

- Markdown writing, scripting, and exploratory coding
- GitHub-based workflows and prototyping
- Base profile for language-specific extensions and settings

---

## 📁 Location

Typically stored under:

```
~/.config/Code/User/profiles/<uuid>/settings.json
```

Or synced via a dotfiles manager at:

```
~/dev/personal/shell/dotfiles/configurations/vscode/profiles/default/
```

---

## 📌 Notes

This profile is intended to be clean and extensible. Language-specific preferences (like for C++, Python, Rust, etc.) should inherit or override this as needed.

---

## 📄 About

**Version:** `1.0`

This profile is licensed under the [MIT License](https://opensource.org/licenses/MIT).

Copyright © 2023–2025 [Kellen Siczka](https://github.com/BobDaGecko)

📁 Part of the [BobDaGecko/VSCode-Profiles](https://github.com/BobDaGecko/VSCode-Profiles) collection.

Built with <span style="color:red">♥</span> in Chicago, US by **Kellen Siczka** (aka `BobDaGecko`)
