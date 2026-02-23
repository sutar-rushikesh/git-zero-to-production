# 🎯 Git Interview Guide -- Detailed Answers with Diagrams

Comprehensive Git Interview Preparation Guide\
With Explanations, Real-World Examples & Visual Diagrams

------------------------------------------------------------------------

# 🧠 1. What is Git?

Git is a distributed version control system that tracks changes in
source code during software development.

It allows: - Version tracking - Collaboration - Branching & merging -
Rollback capability

------------------------------------------------------------------------

# 🧠 2. What is a Commit?

A commit is a snapshot of your project at a specific point in time.

Each commit has: - 40-character SHA-1 ID - Author - Timestamp - Message

``` mermaid
flowchart LR
    A[Working Directory] --> B[Staging Area]
    B --> C[Commit - Local Repository]
```

------------------------------------------------------------------------

# 🧠 3. What is Branching?

Branching allows developers to work independently without affecting main
code.

``` mermaid
gitGraph
   commit id: "Initial"
   branch feature
   checkout feature
   commit id: "Feature Work"
   checkout main
   merge feature
```

------------------------------------------------------------------------

# 🧠 4. What is Merge?

Merge combines changes from one branch into another.

Creates a merge commit.

Used in: - Pull Requests - Feature integration

------------------------------------------------------------------------

# 🧠 5. What is Rebase?

Rebase reapplies commits on top of another base commit to create linear
history.

``` mermaid
gitGraph
   commit id: "Initial"
   branch feature
   checkout feature
   commit id: "Feature Work"
   checkout main
   commit id: "Main Update"
   checkout feature
   commit id: "Feature Work (Reapplied)"
```

Difference: - Merge → Preserves history - Rebase → Cleaner linear
history

------------------------------------------------------------------------

# 🧠 6. What is Cherry Pick?

Cherry-pick applies a specific commit from one branch to another.

Used when: - Urgent hotfix required - Wrong branch commit

Command: git cherry-pick `<commitID>`{=html}

------------------------------------------------------------------------

# 🧠 7. Difference Between Reset and Revert

Reset modifies history (local only recommended). Revert creates new
commit to undo changes (safe for shared branches).

## Reset Types

-   --soft → Uncommit keep staged
-   --mixed → Uncommit + unstage
-   --hard → Delete everything

``` mermaid
flowchart LR
    A[Commit History] -->|Soft| B[Keep Staged]
    A -->|Mixed| C[Unstage]
    A -->|Hard| D[Delete Changes]
```

------------------------------------------------------------------------

# 🧠 8. What is Git Stash?

Temporarily saves changes without committing.

Commands: git stash git stash list git stash apply

Used when switching branches quickly.

------------------------------------------------------------------------

# 🧠 9. What is Merge Conflict?

Occurs when two branches modify same line of code.

Conflict markers:

# \<\<\<\<\<\<\< HEAD

> > > > > > > branch

Resolution: - Edit file - git add - git commit

------------------------------------------------------------------------

# 🧠 10. What is Pull Request?

A request to merge changes into main branch.

Enterprise Flow:

``` mermaid
flowchart LR
    A[Feature Branch] --> B[Pull Request]
    B --> C[Code Review]
    C --> D[Approval]
    D --> E[Merge to Main]
```

------------------------------------------------------------------------

# 🧠 11. Explain Enterprise Branching Strategy

Rules followed in companies:

1.  No direct push to main
2.  Feature branches only
3.  PR mandatory
4.  4-eye approval
5.  Ticket ID in branch name

``` mermaid
gitGraph
   commit id: "Initial"
   branch feature/INC0902324
   checkout feature/INC0902324
   commit id: "Development"
   checkout main
   merge feature/INC0902324
```

------------------------------------------------------------------------

# 🧠 12. What is Hotfix Workflow?

Used when production bug occurs.

Steps: 1. Create hotfix branch from main 2. Fix issue 3. PR & approval
4. Tag release

``` mermaid
flowchart LR
    A[Production Issue] --> B[Hotfix Branch]
    B --> C[Fix & Test]
    C --> D[PR Approval]
    D --> E[Merge]
    E --> F[Tag v1.0.1]
```

------------------------------------------------------------------------

# 🧠 13. What is Detached HEAD?

Occurs when HEAD points to specific commit instead of branch.

Usually happens when checking out a commit ID.

------------------------------------------------------------------------

# 🧠 14. What Happens Internally During Commit?

1.  Files hashed
2.  Blob objects created
3.  Tree object created
4.  Commit object created
5.  HEAD updated

------------------------------------------------------------------------

# 🧠 15. How to Recover Deleted Branch?

Use:

git reflog

Find commit ID and recreate branch:

git checkout -b branch_name commitID

------------------------------------------------------------------------

# 🧠 16. When Should You Avoid Rebase?

Avoid when: - Branch already pushed publicly - Multiple developers using
branch

Because it rewrites history.

------------------------------------------------------------------------

# 🧠 17. How to Revert Pushed Commit?

git revert `<commitID>`{=html}

Creates new commit safely.

------------------------------------------------------------------------

# 🧠 18. Git Tags Explained

Tags are immutable references to commits.

Used for releases:

git tag v1.0.0 git push origin v1.0.0

------------------------------------------------------------------------

# 🧠 19. Git Hooks

Stored in:

.git/hooks

Examples: - pre-commit - pre-push

Used for: - Linting - Secret scanning - Policy enforcement

------------------------------------------------------------------------

# 🧠 20. Difference Between Fetch and Pull

Fetch → Downloads changes only\
Pull → Fetch + Merge

------------------------------------------------------------------------

# 🚀 Conclusion

This guide covers:

✔ Basic Git\
✔ Intermediate Git\
✔ Advanced Git\
✔ Enterprise Workflow\
✔ Production Scenarios

Perfect for DevOps & Developer Interviews.

------------------------------------------------------------------------

👨‍💻 Author\
Rushikesh Sutar\
DevOps Engineer
