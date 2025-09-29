# Git & GitHub Commands Documentation

This file explains the basic commands for working with **Git** and pushing projects to **GitHub**. The explanations are provided in a clear, right-to-left format, making it easy for any developer, whether a beginner or a professional, to use directly without needing to memorize the commands.

---

## Pushing a New Project for the First Time

```bash
git init
git add .
git status
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/username/repository-name.git
git push -u origin main
```

**Explanation:**
- `git init` → Initializes the project folder as a Git repository.
- `git add .` → Adds all files to be staged for commit.
- `git status` → Checks the status of the files.
- `git commit -m "first commit"` → Saves a snapshot of the files with a descriptive message.
- `git branch -M main` → Sets the primary branch name to **main**.
- `git remote add origin <URL>` → Connects the local project to the remote repository on GitHub.
- `git push -u origin main` → Pushes the files to GitHub for the first time.

---

## Updating an Existing Project on Your Machine

```bash
git status
git add .
git status
git commit -m "update project"
git push
```

**Explanation:**
- `git status` → Reviews the changes in the files.
- `git add .` → Adds all modified files.
- `git commit -m "update project"` → Saves the changes with a message.
- `git push` → Pushes the updates to GitHub.

---

## Updating a Project Not on Your Machine (Clone)

```bash
git clone https://github.com/username/repository-name.git
cd repository-name
```

**After making changes:**
```bash
git status
git add .
git commit -m "your commit message"
git push
```

**Explanation:**
- `git clone <URL>` → Downloads the project from GitHub to your machine.
- `cd repository-name` → Navigates into the project folder.
- `git status` → Reviews the modified files.
- `git add .` → Stages the modified files.
- `git commit -m "message"` → Saves the changes.
- `git push` → Pushes the changes to GitHub.

---

## Account Management (Connecting Git with GitHub)

### 1. Add Account (Username + Email)
```bash
git config --global user.name "YourGitHubUsername"
git config --global user.email "your-email@example.com"
```

### 2. Verify Entered Data
```bash
git config --global user.name
git config --global user.email
```

### 3. Connect GitHub with Your Machine Using SSH (Optional but Important)

Create a new SSH key:
```bash
ssh-keygen -t rsa -b 4096 -C "your-email@example.com"
```

Start the SSH Agent service:
```bash
eval "$(ssh-agent -s)"
```

Add the new key:
```bash
ssh-add ~/.ssh/id_rsa
```

Copy the key (to add it in GitHub → Settings → SSH Keys):
```bash
cat ~/.ssh/id_rsa.pub
```

### 4. Verify Connection with GitHub
```bash
ssh -T git@github.com
```
If the message appears: **Hi username! You've successfully authenticated**, the connection is working.

---

## Live Site

[Click here to view the commands directly without explanation](https://example.com)