# 🧬 DRD_2025_Project – Collaborator Guide (Bioinformatics @ UNIBO)

Welcome to the **DRD 2025 Project**! This guide will help you get started with Git, GitHub, and our R project structure — even if you've never used Git before.

---

## ✅ 1. Clone the Repository (One-Time Setup)

First, get a local copy of the project:

```bash
git clone https://github.com/kianinsilico/DRD_2025_Project.git
cd DRD_2025_Project
```
Configure your identity (global if it’s your machine, otherwise repo-level):
```bash
git config --global user.name "Your Full Name"
git config --global user.email "your_email@example.com"
```
## 🧱 2. Set Up the Project Structure in R
Once inside the project folder, open R or RStudio and run:
```R
source("00_setup_project_structure.R")
```
This creates necessary folders like scripts/, data/, results/, etc.

    🔒 Only do this once — at the very beginning!

##🌿 3. Branching Strategy & Naming Rules
❗ Never work directly on main, dev, or doc.

Instead, follow this naming convention:
| Task Type        | Base Branch | Example Branch Name          |
| ---------------- | ----------- | ---------------------------- |
| New feature/code | `dev`       | `feature/alignment-analysis` |
| Bug fix          | `dev`       | `fix/plot-title-error`       |
| Documentation    | `doc`       | `doc/setup-instructions`     |
| Experiment/test  | `dev`       | `test/alternative-alignment` |

##🧪 4. Start Working (Step-by-Step)
###🔄 A. Sync with the base branch
```bash
git checkout dev          # or 'doc' if you're documenting
git pull origin dev       # always pull latest changes
```
###🌿 B. Create your branch
```bash
git checkout -b feature/your-branch-name
Replace your-branch-name with something meaningful (e.g., feature/parse-uniprot-data).
```

##💾 5. Save Your Work (Commit & Push)
After editing scripts or adding files:
```bash
git add <file1> <file2> <...>
git commit -m "Describe what you did here"
```
❗Add files in batch only if they are related or similar in terms of content or are a result of a single step.
❗Don't use wild cards like "git add ." or "git add -A" to add and commit everything. It will be a nightmare if we need to debug or restore our work or revert changes/mistakes.

Then push your branch to GitHub:

```bash
git push -u origin feature/your-branch-name
```
## 📤 6. Submit Your Work via Pull Request (PR)
1. Go to the GitHub page of the repo:
👉 DRD_2025_Project on GitHub

2. Click "Compare & pull request" next to your branch.

3. Target branch should be dev (or doc for documentation).

3. Fill out the PR title and description clearly.

4. Submit the pull request. Wait for review/approval.

## 🔁 7. Keep Your Branch Up-to-Date (Important!)
To avoid conflicts with others:

``` bash
# While working on your feature branch
git checkout dev
git pull origin dev       # get latest changes from GitHub

# Go back to your branch
git checkout feature/your-branch-name
git merge dev             # optional: update your branch
```
🚫 What NOT to Do
❌ Don’t work on main, dev, or doc directly.

❌ Don’t upload raw .csv files, .pdf, or .RData without permission.

❌ Don’t forget to pull before working!

❌ Don’t panic — ask for help if you're stuck 😄

🙋 Questions?
If something is unclear or you run into issues:

Ask your team members

Contact the repo maintainer (Kian)


