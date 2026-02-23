# 🚀 Git Zero to Production

Enterprise Git Workflow \| DevOps Engineering \| Interview Preparation
\| Real-World Scenarios

------------------------------------------------------------------------

## 📌 Overview

This repository covers Git from basic concepts to production-level
enterprise workflows including:

-   Git Basics
-   Branching Strategy
-   Pull Requests
-   Merge Conflicts
-   Rebase vs Merge
-   Cherry Pick
-   Reset vs Revert
-   Git Hooks
-   Git Tags
-   Production Hotfix Strategy
-   Interview Preparation (30 Questions)
-   Real-World Scenarios (10 Cases)

------------------------------------------------------------------------

# 🧠 Git Architecture Flow

``` mermaid
flowchart TD
    A[Working Directory] --> B[Staging Area]
    B --> C[Local Repository]
    C --> D[Remote Repository]
```

------------------------------------------------------------------------

# 🌳 Enterprise Branching Strategy

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

# 🔁 Rebase vs Merge

## Merge -- Non Linear History

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

## Rebase -- Linear History

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

# 🎯 30 Git Interview Questions

## Basic Level

1.  What is Git?
2.  Difference between Git and GitHub?
3.  What is a commit?
4.  What is staging area?
5.  What is the difference between git add and git commit?
6.  What is a branch?
7.  What is HEAD in Git?
8.  What is origin?
9.  Difference between clone and fork?
10. What is the purpose of .git folder?

## Intermediate Level

11. What is Git branching strategy?
12. What is the 4-eye principle in Git workflow?
13. Difference between merge and rebase?
14. What is cherry-pick?
15. What is Git stash?
16. What is merge conflict and how do you resolve it?
17. What is pull request?
18. Difference between fetch and pull?
19. What are Git hooks?
20. What are Git tags?

## Advanced Level

21. Difference between reset and revert?
22. Explain git reset --soft, --mixed, --hard.
23. When should you avoid rebase?
24. What happens internally during commit?
25. How do you recover deleted branch?
26. How to revert a pushed commit?
27. What is detached HEAD?
28. How do you handle large binary files?
29. How do you enforce branch protection?
30. Explain hotfix workflow in production.

------------------------------------------------------------------------

# 🚀 10 Real-World Git Scenarios

1.  Production bug found -- how do you create hotfix branch?
2.  Two developers changed same file -- how to resolve conflict?
3.  Committed to wrong branch -- what will you do?
4.  Need specific commit from another branch -- solution?
5.  Accidentally deleted code -- how to recover?
6.  Want to undo last commit but keep code -- solution?
7.  Want clean history before PR -- what command?
8.  Developer pushed directly to main -- how to fix?
9.  Multiple stashes exist -- how to manage?
10. Release versioning strategy in enterprise?

------------------------------------------------------------------------

# 🔹 Git Reset Summary

-   Soft → Uncommit (keep staged)
-   Mixed → Uncommit + Unstage
-   Hard → Remove everything

------------------------------------------------------------------------

# 🔹 Git Revert

Creates new commit to undo previous changes safely.

------------------------------------------------------------------------

# 🔹 Git Cherry Pick

Apply specific commit into another branch.

------------------------------------------------------------------------

# 🔹 Git Hooks

Location: .git/hooks

Examples: - pre-commit - pre-push - post-merge

------------------------------------------------------------------------

# 🔹 Git Tags

Used for version control:

git tag v1.0.0\
git push origin v1.0.0

------------------------------------------------------------------------

# 👨‍💻 Author

Rushikesh Sutar\
DevOps Engineer

------------------------------------------------------------------------

If this repository helps you in learning or interview preparation,
consider giving it a star.
