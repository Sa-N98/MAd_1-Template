# Project Setup Guide

## 📑 Table of Contents

* [Git Setup Guide](#git-setup-guide)

  * [1. Configure Git Identity](#1-configure-git-identity)
  * [2. Generate SSH Key](#2-generate-ssh-key)
  * [3. Start SSH Agent](#3-start-ssh-agent)
  * [4. Add SSH Key to Agent](#4-add-ssh-key-to-agent)
  * [5. Copy Public Key](#5-copy-public-key)
* [GitHub Repository Setup](#github-repository-setup)

  * [1. Create GitHub Account](#1-create-a-github-account)
  * [2. Create New Repository](#2-create-a-new-repository)
  * [3. Clone Repository](#3-clone-the-repository)
  * [4. Navigate to Repository](#4-navigate-to-repository)
  * [5. Commit and Push Changes](#5-commit-and-push-changes)
  * [6. Using VS Code](#6-using-vs-code)
* [Python Virtual Environment Setup](#python-virtual-environment-setup)

---

# Git Setup Guide

## 1. Configure Git Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

> Use the same name and email as in your GitHub settings.

### Check Configuration

```bash
git config --list
```

---

## 2. Generate SSH Key

```bash
ssh-keygen -t ed25519 -C "you@example.com"
```

**Notes:**

* Press **Enter** for file location
* Press **Enter** for passphrase

---

## 3. Start SSH Agent

```bash
eval "$(ssh-agent -s)"
```

---

## 4. Add SSH Key to Agent

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## 5. Copy Public Key

Paste into: **GitHub → Settings → SSH and GPG Keys → New SSH Key**

```bash
cat ~/.ssh/id_ed25519.pub
```

---

## Common Git Commands

| Command               | Description             |
| --------------------- | ----------------------- |
| `git status`          | Check repository status |
| `git add <file>`      | Stage file              |
| `git add .`           | Stage all changes       |
| `git commit -m "msg"` | Commit changes          |
| `git push`            | Push to remote          |
| `git pull`            | Pull latest changes     |

---

# GitHub Repository Setup

## 1. Create a GitHub Account

Go to: **[https://github.com](https://github.com)**

---

## 2. Create a New Repository

1. Go to GitHub Home
2. Click **New**
3. Fill details:

   * Repository name
   * Optional description
   * Public/Private
   * **Do NOT** tick “Add README”
4. Click **Create Repository**

---

## 3. Clone the Repository

Copy SSH URL:

```
git@github.com:username/repo-name.git
```

Clone:

```bash
git clone git@github.com:username/repo-name.git
```

---

## 4. Navigate to Repository

```bash
cd repo-name
```

---

## 5. Commit and Push Changes

```bash
git add .
git commit -m "Initial commit"
git push
```

---

## 6. Using VS Code

Open repo folder in terminal → run:

```bash
code .
```

Then use **VS Code Source Control** to stage and commit.

### Windows Video

*(Add link here later)*

### Linux / macOS Video: [Linux/macOS VS Code Git Tutorial](https://www.youtube.com/watch?v=RtlJ1nqlvFc)

---

# Python Virtual Environment Setup

## 1. Check if Python Is Installed

```bash
python --version
```

or

```bash
python3 --version
```

You should see something like:

```
Python 3.x.x
```

---

## 2. Check if pip Is Installed

```bash
pip --version
```

or

```bash
pip3 --version
```

---

## 3. Create a Virtual Environment Inside Your Project

```bash
python3 -m venv venv
```

or

```bash
python -m venv venv
```

---

## 4. Activate the Virtual Environment

### macOS / Linux

```bash
source venv/bin/activate
```

### Windows (PowerShell)

```bash
venv\Scripts\activate
```

After activation, you should see something like:

```
(venv) $
```

---

## 5. Install Dependencies

```bash
pip install flask
```
#### Note: add dependency name to requirements.txt

---

## 6. Add venv to .gitignore

```
venv/
__pycache__/
```
#### Note: Create .gitignore file if not there 
---
