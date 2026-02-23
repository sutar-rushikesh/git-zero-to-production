# 🚀 Enterprise Git Workflow for DevOps Engineers

![Git](https://img.shields.io/badge/Git-Advanced-red?style=for-the-badge&logo=git)
![DevOps](https://img.shields.io/badge/DevOps-Production%20Ready-blue?style=for-the-badge&logo=dev.to)
![Branching](https://img.shields.io/badge/Branching-Strategy-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

------------------------------------------------------------------------

## 🌟 Project Overview

This repository demonstrates **Enterprise-Level Git Workflow** used in
real-world DevOps environments.

It covers:

-   Branching Strategy (Corporate Model)
-   Pull Requests & 4-Eye Principle
-   Merge Conflict Resolution
-   Git Rebase & Cherry Pick
-   Git Reset vs Git Revert
-   Git Stash
-   Git Hooks
-   Git Tags (Release Versioning)
-   Production Hotfix Scenarios

------------------------------------------------------------------------

## 🧠 Git Architecture

Working Directory\
↓\
Staging Area (git add)\
↓\
Local Repository (git commit)\
↓\
Remote Repository (git push)

------------------------------------------------------------------------

## 🌳 Enterprise Branching Strategy

✔ No direct push to `main/master`\
✔ Feature branch mandatory\
✔ INC/REQ/CHG/STORY naming convention\
✔ Pull Request required\
✔ Minimum 2 approvals (4-Eye Principle)

Example:

main\
├── INC0902324\
├── REQ092348\
└── CHG009823

------------------------------------------------------------------------

## 🔥 Merge Conflict Example

\<\<\<\<\<\<\< HEAD\
echo "Adding new line"\
=======\
echo "Adding new data"\
\>\>\>\>\>\>\> branch-name

Resolution Steps:

1.  Discuss with team\
2.  Remove conflict markers\
3.  Keep correct final code\
4.  git add .\
5.  git commit -m "Resolved conflict"

------------------------------------------------------------------------

## ⚡ Rebase vs Merge

  Merge                    Rebase
  ------------------------ -----------------
  Creates merge commit     Linear history
  Safe                     Cleaner history
  Good for shared branch   Use carefully

------------------------------------------------------------------------

## 🚨 Production Hotfix Scenario

Situation:\
Application down → War room created → Immediate fix required

Workflow:

1.  Create hotfix branch from main\
2.  Fix issue\
3.  Create PR\
4.  Approval\
5.  Merge\
6.  Tag release (v1.0.1)

------------------------------------------------------------------------

## 🛠 Git Reset Modes

Soft → Uncommit (keeps staged)\
Mixed → Uncommit + unstage\
Hard → Uncommit + unstage + delete changes ⚠

------------------------------------------------------------------------

## 🔁 Git Revert

Creates a new commit that undoes previous changes.\
Safe for shared repositories.

------------------------------------------------------------------------

## 🏷 Git Tags

Used for versioning releases:

v1.0\
v2.0\
release-2026

Tags point to a specific commit and do not change.

------------------------------------------------------------------------

## 🪝 Git Hooks

Location: `.git/hooks`

Examples:

-   pre-commit
-   pre-push
-   post-push

Used for:

-   Code validation
-   Security scanning
-   Automated testing

------------------------------------------------------------------------

## 📚 Command Reference

git clone\
git add .\
git commit -m "message"\
git push\
git pull\
git fetch\
git rebase\
git cherry-pick\
git stash\
git reset --soft\
git reset --hard\
git revert\
git tag

------------------------------------------------------------------------

## 🎓 Interview & Scenario Coverage

✔ 30+ Interview Questions\
✔ 10 Real-World Production Scenarios\
✔ Enterprise DevOps Workflow

------------------------------------------------------------------------

## 👨‍💻 Author

DevOps Engineer\
Enterprise Workflow Practitioner\
Focused on Production-Ready Practices

------------------------------------------------------------------------

⭐ If you found this helpful, consider giving this repository a star!
