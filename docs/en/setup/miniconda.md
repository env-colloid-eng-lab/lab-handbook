# Miniconda

Miniconda is a lightweight Python distribution that includes the `conda` package manager. It is the recommended way to manage Python environments in this lab.

## 1. Download Miniconda

Go to the official Miniconda page and download the installer for your OS:  
[https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

- **Windows**: Download the `.exe` installer and run it (or use the Linux installer inside WSL).
- **macOS / Linux**: Download the `.sh` installer.

## 2. Install Miniconda (macOS / Linux / WSL)

```bash
bash Miniconda3-latest-Linux-x86_64.sh
```

Follow the prompts. When asked whether to initialize conda, answer `yes`.

Restart your terminal, then verify:

```bash
conda --version
```

## 3. Create a New Environment

It is good practice to create a separate environment for each project:

```bash
conda create -n myenv python=3.11
conda activate myenv
```

## 4. Install Common Packages

```bash
conda install numpy pandas matplotlib jupyter
```

## 5. Useful conda Commands

| Command | Description |
|---------|-------------|
| `conda activate myenv` | Activate an environment |
| `conda deactivate` | Deactivate current environment |
| `conda env list` | List all environments |
| `conda install <pkg>` | Install a package |
| `conda update conda` | Update conda itself |

---

[← Back to Setup Overview](index.md)
