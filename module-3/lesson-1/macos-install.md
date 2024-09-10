# Module 2, Lesson 1: Installing Python on macOS

## Introduction

In this lesson, we will go through two methods of installing Python on macOS:
1. Installing Python using **Homebrew**.
2. Installing Python **manually** from the official website.

## Method 1: Installing Python with Homebrew

**Homebrew** is a package manager for macOS that makes it easier to install software.

### Step 1: Install Homebrew (if not installed)
If you don't have Homebrew installed, open the Terminal app and run the following command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

After installation, verify it by running:

```bash
brew --version
```

### Step 2: Install Python via Homebrew

Once Homebrew is installed, you can install Python by running:

```bash
brew install python
```

### Step 3: Verify Python Installation

To verify if Python was installed successfully, check the version by running:

```bash
python3 --version
```

You should see the Python version printed in the terminal, such as `Python 3.x.x`.

## Method 2: Installing Python Manually from python.org

If you prefer not to use Homebrew, you can download and install Python manually.

### Step 1: Download the Python Installer

1. Visit the official Python website: [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click the **Download Python 3.x.x** button, where `x.x` is the latest version.

### Step 2: Run the Installer

1. Once the download is complete, open the `.pkg` file.
2. Follow the prompts in the installation wizard:
    - Agree to the License Agreement.
    - Choose the installation location (the default is usually fine).
    - Install the package.

### Step 3: Verify Python Installation

After the installation completes, open the Terminal app and run:

```bash
python3 --version
```

You should see the installed version of Python.

### Step 4 (Optional): Add Python to Your PATH

If the terminal does not recognize `python3`, you may need to add Python to your PATH. Add the following line to your `~/.bash_profile`, `~/.zshrc`, or `~/.bashrc`, depending on your shell:

```bash
export PATH="/usr/local/bin/python3:$PATH"
```

Then, apply the changes by running:

```bash
source ~/.bash_profile  # or ~/.zshrc or ~/.bashrc
```

## Summary

You now have two methods to install Python on macOS:
- Using **Homebrew** for a quick and easy installation process.
- **Manual installation** from the official Python website.

Once installed, you can start using Python by typing `python3` in your terminal.