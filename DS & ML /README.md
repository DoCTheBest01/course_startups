---

# 🧠 Data Analysis & Machine Learning Course — Environment Setup Guide

Welcome to the course!
This document will guide you through setting up a clean and stable Python environment on your system using **WSL**, **Conda**, and **Jupyter Notebook** — ensuring full compatibility for machine learning workflows.

---

## 🧩 1. Install Windows Subsystem for Linux (WSL)

WSL allows you to run a full Linux environment on Windows — perfect for Python and ML development.

### Steps:

1. **Open PowerShell as Administrator**
   Press **Win + X → Terminal (Admin)**.

2. **Run the following command:**

   ```bash
   wsl --install
   ```

   This installs Ubuntu by default (recommended).

3. **Restart your computer** when prompted.

4. **Open Ubuntu** from the Start Menu.
   When it starts, it’ll ask you to:

   * Create a **username**
   * Create a **password**

5. **Update your system:**

   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

✅ **You now have a Linux environment ready for development!**

---

## 🧪 2. Install Miniconda

We’ll use **Miniconda** (lightweight Conda distribution) to manage packages and environments.

### Steps:

1. **Download Miniconda installer for Linux:**

   ```bash
   wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
   ```

2. **Run the installer:**

   ```bash
   bash Miniconda3-latest-Linux-x86_64.sh
   ```

   * Press **Enter** through the prompts.
   * Type **yes** to accept the license.
   * Type **yes** again when asked to initialize Conda.

3. **Activate Conda:**

   ```bash
   source ~/.bashrc
   ```

4. **Verify installation:**

   ```bash
   conda --version
   ```

---

## 🧱 3. Create a Conda Environment with Compatible Python Version

We’ll create a dedicated environment for the course.

### Find a CUDA-compatible Python version

TensorFlow and PyTorch have historically supported Python **3.8–3.10** well for GPU-based setups.
Even though we won’t use deep learning here, it’s good to stay compatible.

👉 **Recommended:** Use **Python 3.10** for maximum library compatibility.

### Steps:

1. **Create the environment:**

   ```bash
   conda create -n mlcourse python=3.10
   ```

2. **Activate it:**

   ```bash
   conda activate mlcourse
   ```

3. **Verify Python version:**

   ```bash
   python --version
   ```

---

## 📒 4. Install Jupyter Notebook

Jupyter allows you to write and execute Python code interactively.

### Install:

```bash
conda install jupyter
```

### Launch:

```bash
jupyter notebook
```

Your browser will open automatically at:

```
http://localhost:8888
```

### (Optional) Create a shortcut command:

You can make a shell alias for quick launching:

```bash
echo 'alias jp="jupyter notebook"' >> ~/.bashrc
source ~/.bashrc
```

Now, simply type:

```bash
jp
```

---

## 🧹 5. Summary of Commands

| Purpose           | Command                                  |
| ----------------- | ---------------------------------------- |
| Update Ubuntu     | `sudo apt update && sudo apt upgrade -y` |
| Install WSL       | `wsl --install`                          |
| Install Miniconda | `bash Miniconda3-latest-Linux-x86_64.sh` |
| Create env        | `conda create -n mlcourse python=3.10`   |
| Activate env      | `conda activate mlcourse`                |
| Install Jupyter   | `conda install jupyter`                  |
| Launch Jupyter    | `jupyter notebook`                       |

---
