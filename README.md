# 🌈 VS Code Custom UI Setup (React JS Theme)

This repository contains a customized Visual Studio Code setup that enhances UI elements using a custom CSS and JavaScript injection approach. It is tailored for an improved experience with the **default React JS theme** and includes better visual feedback for the command palette, explorer, tooltips, and more.

---

## 📁 Contents

- `custom-vscode.css` – Custom styling to improve font, sidebar, scrollbars, tooltips, file explorer, and command palette.
- `vscode-script.js` – JS logic to manage blur overlays and interactivity for the command palette.
- `art.svg` – *(Optional)* Background artwork or asset for reference or integration.

---

## 💡 Features

### 🖌 Custom CSS (`custom-vscode.css`)
- Monospaced fonts (`Geist Mono`, `Monaspace Radon`)
- Custom highlight colors for:
  - Sidebar and file explorer
  - Scrollbars and shadows
  - Tooltips and command palette
- Glassmorphism-inspired blur effect
- Typography improvements across UI elements
- Smooth command palette and quick-input transitions

### 🧠 JavaScript Enhancements (`vscode-script.js`)
- Dynamically adds a blur backdrop when the command palette opens
- Restores original UI when command palette is closed
- Intercepts `Ctrl+P` / `Cmd+P` and `Esc` for enhanced interaction

---

## 🧩 Recommended Extensions

These customizations were built with the **React JS default theme** in mind. It is recommended to install:

- **Custom CSS and JS Loader**  
  Enables loading of external `.css` and `.js` files inside VS Code.

  **Extension ID**: `be5invis.vscode-custom-css`  
  🔗 [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css)

---

## ⚙️ Setup Instructions

> ⚠️ **Note:** This customization is unofficial and requires modifying VS Code internals. Proceed at your own risk.

### 1. Install Extension

Install **Custom CSS and JS Loader** from the Marketplace.

### 2. Enable Custom Styling

Open your `settings.json` and add:

```json
"vscode_custom_css.imports": [
  "file:///absolute/path/to/custom-vscode.css",
  "file:///absolute/path/to/vscode-script.js"
],
"vscode_custom_css.policy": true

📌 Replace "file:///absolute/path/to/..." with the full file paths on your machine.

3. Reload VS Code
Open the command palette (Ctrl+Shift+P) and run:

Enable Custom CSS and JS
Then restart VS Code to apply the changes.

🧼 Resetting to Default
To revert the customization:

code --disable-extensions
Or manually remove the extension and delete CSS/JS entries from your settings.json.
