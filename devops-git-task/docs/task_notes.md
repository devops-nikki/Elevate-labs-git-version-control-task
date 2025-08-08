# Task Notes

## Git Best Practices Used:
- Created separate branches: main, dev, feature.
- Used pull requests to merge branches.
- Tagged initial version as `v1.0`.
- Implemented `.gitignore` to avoid unnecessary files.
- Created CI workflow using GitHub Actions.

## Project Setup:
- Used shell script to simulate setup.
- HTML file added in `src/` to simulate front-end source.
# Basic Git Commands

# Initialize a new Git repository
git init

# Check the status of your working directory and staging area
git status

# Add changes to staging area (add all files)
git add .

# Commit staged changes with a descriptive message
git commit -m "Your commit message here"

# View commit history
git log

# View a simplified one-line commit history graph
git log --oneline --graph --all

# Create a new branch and switch to it
git checkout -b feature-branch

# Switch to an existing branch
git checkout main

# Merge another branch into your current branch
git merge feature-branch

# Fetch latest changes from remote without merging
git fetch origin

# Pull latest changes from remote and merge automatically
git pull origin main

# Push your local branch to the remote repository
git push origin main

# View remote repositories
git remote -v

# Create a lightweight tag
git tag v1.0.0

# Push tags to remote
git push origin --tags

# Stash your current changes (save them temporarily)
git stash

# Apply stashed changes and remove from stash list
git stash pop

# Delete a local branch
git branch -d feature-branch

# Delete a remote branch
git push origin --delete feature-branch


# Git Workflows
This document explains popular Git workflows used in software development projects, especially in DevOps environments.

1. Feature Branch Workflow
Each new feature or bug fix is developed in a dedicated branch created from the main branch (main or dev).
Developers work independently on their feature branches.
Once complete, the feature branch is merged back into dev or main via a Pull Request (PR).
Helps isolate work, allows code review, and facilitates parallel development.

2. Git Flow Workflow
A well-defined branching model designed for release management.
Main branches:
main (or master): production-ready code
develop: integration branch for features
Supporting branches:
Feature branches (from develop)
Release branches (from develop for preparing releases)
Hotfix branches (from main for urgent fixes)
Ensures structured release cycles and better version control.

3. Trunk-Based Development
Developers commit small, frequent changes directly to the main branch (often main or trunk).
Feature flags or toggles may be used to hide incomplete features.
Emphasizes continuous integration and rapid delivery.
Avoids long-lived branches to reduce merge conflicts.

4. Forking Workflow
Commonly used in open-source projects.
Developers fork the main repository to create their own copy.
They make changes in their fork, then submit a Pull Request back to the main repository.
Maintainers review and merge the PRs.
Provides a clear separation between contributors and maintainers.
Best Practices for Git Workflows
Commit frequently with clear, descriptive messages.
Keep branches focused on a single task or feature.
Regularly sync your branch with the base branch to avoid conflicts.
Use Pull Requests for code review and collaboration.
Use .gitignore to avoid committing unnecessary files.
Tag releases for easy rollback and version tracking.
References
Git Branching Model
GitHub Flow
Atlassian Git Workflows
Last updated: 2025-08-08