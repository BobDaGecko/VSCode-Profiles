# VSCode Profile: `cpp::default`

A specialized Visual Studio Code profile for C and C++ development, layered on top of the global [`default`](https://github.com/BobDaGecko/VSCode-Profiles/tree/main/profiles/default) profile. This profile includes tools for Clang-based development, CMake integration, and standard formatting and code style conventions for modern C/C++ workflows.

---

## 🧩 Additional Extensions

These extensions are included **in addition to** those defined in the [`default`](https://github.com/BobDaGecko/VSCode-Profiles/tree/main/profiles/default) profile:

| Extension                               | Purpose                                        |
| --------------------------------------- | ---------------------------------------------- |
| `llvm-vs-code-extensions.vscode-clangd` | Clangd-based IntelliSense and formatting       |
| `ms-vscode.cpptools`                    | C/C++ language support and debugging           |
| `ms-vscode.cpptools-extension-pack`     | Convenience pack for C/C++ development         |
| `ms-vscode.cpptools-themes`             | Color themes for C/C++ semantic highlighting   |
| `ms-vscode.cmake-tools`                 | CMake integration for build and config support |
| `twxs.cmake`                            | Syntax highlighting for `.cmake` files         |
| `hars.cppsnippets`                      | Useful code snippets for C++                   |

---

## ⚙️ Additional & Overridden Settings

This profile includes **language-specific settings** and tools specific to C/C++ development:

### 📚 Language Overrides

#### `[cpp]` and `[c]`

- **Formatter**: `clangd` (`llvm-vs-code-extensions.vscode-clangd`)
- **Tab Size**: `4`
- **Insert Spaces**: `true`
- **Rulers**: `80`, `100` (visual line length guides)

---

### 🛠 IntelliSense & Tooling

- **IntelliSense Engine**: `default`
- **Configuration Provider**: `ms-vscode.cmake-tools`
- **Logging Level**: `Warning`
- **Formatting Provider**: `clangFormat`
- **Fallback Style**: `Google`
- **CMake Source Directory**: `${workspaceFolder}`

---

## ✅ Recommended Use Cases

- System programming in **C** or **C++**
- Projects using **CMake** as a build system
- Compatible with Clang toolchains and `clangd`-based environments

---

## 📦 Extension Management

To install all required extensions for this profile:

```bash
cat extensions.txt | xargs -L 1 code --install-extension
```

---

## 📄 About

**Version:** `1.0`

This profile is licensed under the [MIT License](https://opensource.org/licenses/MIT).

Copyright © 2023–2025 [Kellen Siczka](https://github.com/BobDaGecko)

📁 Part of the [BobDaGecko/VSCode-Profiles](https://github.com/BobDaGecko/VSCode-Profiles) collection.

Built with <span style="color:red">♥</span> in Chicago, US by **Kellen Siczka** (aka `BobDaGecko`)
