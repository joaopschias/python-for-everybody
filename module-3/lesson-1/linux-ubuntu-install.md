# Module 2, Lesson 1: Installing Python on Linux Ubuntu

## Introduction

In this lesson, we will learn how to install Python on Linux Ubuntu using two different methods:
1. Installing Python using the **APT package manager**.
2. Installing Python **manually** from the source.

## Method 1: Installing Python using APT

APT (Advanced Package Tool) is the default package manager for Ubuntu and provides the simplest way to install Python.

### Step 1: Update the Package List

Before installing Python, update the package list to ensure that you're getting the latest versions available:

```bash
sudo apt update
```

### Step 2: Install Python 3

Ubuntu typically comes with Python pre-installed, but you can install or upgrade it using the following command:

```bash
sudo apt install python3
```

### Step 3: Verify Python Installation

After installation, verify it by checking the Python version:

```bash
python3 --version
```

You should see something like `Python 3.x.x`.

### Step 4: Install Pip (Optional)

`pip` is the package manager for Python, and you can install it using:

```bash
sudo apt install python3-pip
```

To verify `pip` is installed correctly, run:

```bash
pip3 --version
```

## Method 2: Installing Python from Source

If you need a specific version of Python or want to compile it yourself, you can install Python from the source.

### Step 1: Install Build Dependencies

First, install the necessary packages to build Python:

```bash
sudo apt update
sudo apt install build-essential libssl-dev libffi-dev zlib1g-dev \
  libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm \
  libncurses5-dev libncursesw5-dev xz-utils tk-dev
```

### Step 2: Download the Python Source Code

Go to the [official Python website](https://www.python.org/downloads/source/) and find the latest version. You can download it via `wget`:

```bash
wget https://www.python.org/ftp/python/3.x.x/Python-3.x.x.tgz
```

Replace `3.x.x` with the desired version.

### Step 3: Extract the Downloaded File

After the download is complete, extract the tarball:

```bash
tar -xf Python-3.x.x.tgz
```

### Step 4: Build and Install Python

Navigate to the extracted directory and configure the build:

```bash
cd Python-3.x.x
./configure --enable-optimizations
```

Then compile the source code:

```bash
make -j 8
```

The `-j 8` flag specifies parallel compilation with 8 cores. Adjust based on your system.

Finally, install Python:

```bash
sudo make altinstall
```

**Note**: `altinstall` is used to prevent replacing the system's default `python` command.

### Step 5: Verify the Installation

Check the version of the newly installed Python:

```bash
python3.x --version
```

Replace `3.x` with the specific version you installed.

## Summary

You now have two methods to install Python on Linux Ubuntu:
- **APT package manager** for a simple and quick installation process.
- **Manual installation from the source** if you need a specific version or want to optimize the build.

After installation, you can start using Python by typing `python3` in your terminal.