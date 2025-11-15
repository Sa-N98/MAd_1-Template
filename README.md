# Project Setup Guide

## 📚 Interactive Index

* [🚀 1. Configure Git](#-1-configure-git-run-once)
* [🔐 2. Generate SSH Key](#-2-generate-ssh-key-run-once)
* [🚀 3. Start SSH Agent](#-3-start-ssh-agent-run-once)
* [➕ 4. Add SSH Key to Agent](#-4-add-ssh-key-to-agent-run-once)
* [📤 5. Copy Public Key](#-5-copy-public-key-run-once)
* [🧰 GitHub Repo Setup Guide](#-github-repo-setup-guide)

  * [🌐 Create a GitHub Account](#-1-create-a-github-account)
  * [📦 Create a New GitHub Repository](#-2-create-a-new-github-repository)
  * [📥 Clone the Repository](#-3-clone-the-repository-using-ssh)
  * [📂 Enter the Repo Folder](#-4-enter-the-repo-folder)
  * [📤 Add Commit Push](#-5-add-commit-push-optional)
  * [🖥️ VS Code Method](#-6-alternate-way-to-step-5-using-vs-code)

---

## 🚀 1. Configure Git (Run Once)

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

## 🔐 2. Generate SSH Key (Run Once)

```bash
ssh-keygen -t ed25519 -C "you@example.com"
```

**Notes:**

* Press **Enter** for file location
* Press **Enter** for passphrase

---

## 🚀 3. Start SSH Agent (Run Once)

```bash
eval "$(ssh-agent -s)"
```

---

## ➕ 4. Add SSH Key to Agent (Run Once)

```bash
ssh-add ~/.ssh/id_ed25519
```

---

## 📤 5. Copy Public Key (Run Once)

Paste this key into: **GitHub → Settings → SSH and GPG Keys → New SSH Key**

```bash
cat ~/.ssh/id_ed25519.pub
```

---

# 🧰 GitHub Repo Setup Guide

## 🌐 1. Create a GitHub Account

Go to: [**https://github.com**](https://github.com)

---

## 📦 2. Create a New GitHub Repository

1. Go to GitHub Home
2. Click **New** (or + icon → *New repository*)
3. Fill details:

   * **Repository name**
   * Optional **Description**
   * Choose **Public** or **Private**
   * **Do NOT** tick “Add README”
4. Click **Create repository**

---

## 📥 3. Clone the Repository (Using SSH)

Copy the SSH URL:

```
git@github.com:username/repo-name.git
```

Clone it:

```bash
git clone git@github.com:username/repo-name.git
```

---

## 📂 4. Enter the Repo Folder

```bash
cd repo-name
```

---

## 📤 5. Add, Commit, Push (Optional)

```bash
git add .
git commit -m "Initial commit"
git push
```

---

## 🖥️ 6. Alternate Way to Step 5 (Using VS Code)

Repo folder → **Open In  Terminal Here** → Run:

```bash
code .
```

Then use **VS Code Source Control UI** to stage and commit.

### 🎥 Watch the videos below to see how to manage commits in VS Code.

---

### 🪟 Windows

### 🐧 Linux / 🍎 macOS
