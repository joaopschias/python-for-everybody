# Module 2, Lesson 1: Installing Python on Windows

## Introduction

In this lesson, we will go through the steps to install Python on a Windows machine. Python provides an easy-to-use installer that simplifies the process.

## Step 1: Download Python Installer

1. Go to the official Python website: [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click the **Download Python 3.x.x** button, where `x.x` is the latest version.

### Important:
Make sure you download the correct version for your system:
- For 64-bit systems, download the 64-bit installer (`Windows x86-64 executable installer`).
- For 32-bit systems, download the 32-bit installer (`Windows x86 executable installer`).

## Step 2: Run the Installer

Once the installer has been downloaded, follow these steps:

1. **Run the installer** by double-clicking the `.exe` file.
2. On the first screen, make sure to check the box that says **Add Python 3.x to PATH**. This is important so you can use Python from the command line.
3. Click **Install Now** to install Python with default settings.

## Step 3: Verify Installation

After the installation finishes:

1. Open the **Command Prompt** by pressing `Windows + R`, typing `cmd`, and hitting Enter.
2. Check if Python is installed and accessible by typing:

```bash
python --version
```

You should see the installed Python version, such as `Python 3.x.x`.

### Step 3.1: Verify Pip Installation

Python’s package manager, `pip`, is installed automatically. Verify the installation by running:

```bash
pip --version
```

You should see the installed version of `pip`.

## Step 4: Install IDE (Optional)

If you don't have an integrated development environment (IDE) for Python, you can install **IDLE**, which comes bundled with Python, or use third-party options like **PyCharm** or **Visual Studio Code**.

To launch **IDLE**, search for it in the Start menu and begin coding in Python immediately.

## Step 5: Set Up Environment Variables (If Needed)

If Python doesn't run in the Command Prompt, you may need to manually add Python to the system environment variables:

1. Open **Control Panel** > **System and Security** > **System**.
2. Click **Advanced system settings** on the left, then click the **Environment Variables** button.
3. In the **System Variables** section, scroll to **Path** and click **Edit**.
4. Click **New** and add the path where Python is installed (for example: `C:\Python39`).
5. Click **OK** to save the changes.

## Summary

You now have Python installed on Windows. You can verify the installation by running `python --version` and `pip --version` in the Command Prompt. With Python installed, you're ready to start coding and can use tools like IDLE, PyCharm, or Visual Studio Code to write and execute Python programs.