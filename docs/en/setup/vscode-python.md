# VS Code & Python

This guide walks you through installing Visual Studio Code and setting it up for Python development.

## 1. Install Visual Studio Code

Download and install VS Code from the official website:  
[https://code.visualstudio.com/](https://code.visualstudio.com/)

Follow the installer for your operating system (Windows, macOS, or Linux).

## 2. Install the Python Extension

1. Open VS Code.
2. Go to the **Extensions** panel (Ctrl+Shift+X / Cmd+Shift+X).
3. Search for **Python** (by Microsoft).
4. Click **Install**.

## 3. Select a Python Interpreter

1. Open the Command Palette (Ctrl+Shift+P / Cmd+Shift+P).
2. Type `Python: Select Interpreter`.
3. Choose the Python interpreter from your Miniconda environment (if set up).

> See [Miniconda setup](miniconda.md) if you have not set up Miniconda yet.

## 4. Verify Your Setup

Open a new terminal in VS Code (Terminal → New Terminal) and run:

```bash
python --version
```

You should see a version number like `Python 3.11.x`.

## 5. Useful Extensions (Optional)

- **Pylance** — improved IntelliSense for Python
- **Jupyter** — run Jupyter notebooks inside VS Code
- **GitLens** — enhanced Git integration

---

[← Back to Setup Overview](index.md)
