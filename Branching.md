Git Branching (Detailed Notes)
1. What is a Branch in Git?

A branch is a pointer to a commit in Git.

By default, a new repo starts with the main (or master) branch.

Branching allows parallel development without disturbing the main codebase.

Think of a branch as a workspace where you can make changes safely.

2. Why Use Branches?

Work on new features without breaking production code.

Experiment with ideas safely.

Fix bugs independently.

Collaborate in teams (each feature in its own branch).

3. Common Branch Types

Main (or Master) → Production-ready code.

Feature Branch → For new features (feature/login-ui).

Bugfix Branch → For fixing issues (bugfix/user-auth).

Hotfix Branch → Urgent fixes in production (hotfix/payment-error).

Release Branch → Prepares for deployment (release/v2.0).

4. Basic Branch Commands
🔹 Create a New Branch
git branch feature1

🔹 Switch to a Branch
git checkout feature1


(or modern way:)

git switch feature1

🔹 Create & Switch in One Step
git checkout -b feature1

🔹 See All Branches
git branch

🔹 Merge Branch into Main
git checkout main
git merge feature1

🔹 Delete a Branch
git branch -d feature1

5. Branching Workflow Example

Start in main branch:

git checkout main


Create a new feature branch:

git checkout -b feature-login


Make changes → git add → git commit.

Merge back into main:

git checkout main
git merge feature-login


Push branch to remote:

git push origin feature-login

6. Branching Visual Flow
main:  A──B──C──D
               \
feature:        E──F──G


A, B, C, D → commits in main.

E, F, G → commits in feature branch.

Later, you merge feature back into main.

7. Merging vs. Rebasing

Merge: Combines changes, creates a new merge commit. (Preserves history)

Rebase: Moves branch commits on top of another branch. (Cleaner history)
