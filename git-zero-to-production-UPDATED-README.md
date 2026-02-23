# 🚀 Git Zero to Production

Enterprise Git Workflow \| DevOps Engineering \| Real‑World Scenarios

------------------------------------------------------------------------

## 📌 Overview

This repository demonstrates a complete Enterprise‑Level Git Workflow
from basics to production readiness.

Covered Topics:

-   Git Basics
-   Branching Strategy (Corporate Standard)
-   Pull Request Workflow
-   Merge Conflicts
-   Rebase vs Merge
-   Cherry Pick
-   Git Reset (Soft / Mixed / Hard)
-   Git Revert
-   Git Stash
-   Git Hooks
-   Git Tags
-   Production Hotfix Strategy
-   Interview Questions
-   Real‑World Scenarios

------------------------------------------------------------------------

## 🧠 Git Architecture Flow

``` mermaid
flowchart TD
    A[Working Directory] --> B[Staging Area]
    B --> C[Local Repository]
    C --> D[Remote Repository]
```

------------------------------------------------------------------------

## 🌳 Enterprise Branching Strategy

``` mermaid
gitGraph
   commit id: "Initial Commit"
   branch feature/INC0902324
   checkout feature/INC0902324
   commit id: "Feature Development"
   checkout main
   merge feature/INC0902324 tag: "v1.0.0"
```

------------------------------------------------------------------------

## 🔁 Rebase vs Merge Visual

### Merge -- Non Linear History

``` mermaid
gitGraph
   commit id: "Initial"
   branch feature
   checkout feature
   commit id: "Feature Work"
   checkout main
   commit id: "Main Update"
   merge feature tag: "Merge Commit"
```

### Rebase -- Linear History

``` mermaid
gitGraph
   commit id: "Initial"
   branch feature
   checkout feature
   commit id: "Feature Work"
   checkout main
   commit id: "Main Update"
   checkout feature
   commit id: "Feature Work (Rebased)"
```

------------------------------------------------------------------------

## 🚨 Production Hotfix Flow

``` mermaid
flowchart LR
    A[Production Issue] --> B[Create Hotfix Branch]
    B --> C[Fix & Test]
    C --> D[Pull Request]
    D --> E[Approval]
    E --> F[Merge]
    F --> G[Tag v1.0.1]
```

------------------------------------------------------------------------

## 🔹 Git Reset Modes

-   git reset --soft → Uncommit (keep staged)
-   git reset --mixed → Uncommit + Unstage
-   git reset --hard → Remove everything

------------------------------------------------------------------------

## 🔹 Git Revert

Creates new commit to undo changes safely.

------------------------------------------------------------------------

## 🔹 Git Cherry Pick

Apply specific commit to another branch.

------------------------------------------------------------------------

## 🔹 Git Hooks

Stored in: .git/hooks

Examples: - pre-commit - pre-push - post-merge

------------------------------------------------------------------------

## 🔹 Git Tags

Used for versioning.

Example: git tag v1.0.0 git push origin v1.0.0

------------------------------------------------------------------------

## 🎯 Real‑World Scenarios Covered

-   Production hotfix handling
-   Merge conflict resolution
-   Rebase before PR
-   Cherry-pick for urgent fix
-   Reset vs Revert decision

------------------------------------------------------------------------

## 👨‍💻 Author

Rushikesh Sutar\
DevOps Engineer

------------------------------------------------------------------------

⭐ If you find this helpful, give it a star.
