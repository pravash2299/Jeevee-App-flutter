# Git Collaboration Guide

A comprehensive guide for beginners on how to use Git for project collaboration, including branch management and common workflows.

## Table of Contents
- [Initial Setup](#initial-setup)
- [Basic Workflow](#basic-workflow)
- [Push and Pull Operations](#push-and-pull-operations)
- [Branch Management](#branch-management)
- [Handling Conflicts](#handling-conflicts)
- [Common Commands](#common-commands)
- [Best Practices](#best-practices)

## Initial Setup

One-time configuration steps for Git:

```bash
# Configure Git with your identity
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Basic Workflow

### 1. Clone the Repository
```bash
# Clone the repository
git clone <repository_url>
git clone https://github.com/pravash2299/Jeevee-App-flutter.git

# Navigate to project directory
cd <repository_name>
cd Jeevee-App-flutter
```

### 2. Create and Switch to New Branch
```bash
# Create and switch to new branch 'pravash'
git checkout -b <your-branch-name>

# Verify current branch. The current branch will be highlighted with an asterisk (*).
git branch
```

### 3. Make and Commit Changes
```bash
# Check status of changes
git status

# Add changes to staging area
git add .                  # Add all changes
# OR
git add <filename>         # Add specific files

# Commit changes
git commit -m "Your descriptive commit message"
```

### 4. First-time Push
```bash
# Push and set upstream branch
git push -u origin <your-branch-name>
```

## Push and Pull Operations

### Pushing Changes
```bash
# Regular push after first-time setup
git push

# Force push (use carefully!)
git push -f origin <your-branch-name>
```

### Pulling Changes
```bash
# Method 1: Pull changes (fetch + merge combined)
git pull origin <your-branch-name>

# Method 2: Separate fetch and merge
git fetch origin
git merge origin/<your-branch-name>
```

### Syncing with Main Branch
```bash
# Switch to your branch
git checkout <your-branch-name>

# Pull latest changes from main
git pull origin main
```

## Branch Management

```bash
# List all branches
git branch -a

# Switch branches
git checkout <your-branch-name>

# Delete local branch
git branch -d <your-branch-name>

# Delete remote branch
git push origin --delete <your-branch-name>
```

## Handling Conflicts

When conflicts occur during merge/pull:

1. Identify conflicted files:
```bash
git status
```

2. Open the files and resolve conflicts
3. After resolving:
```bash
git add .
git commit -m "Resolved merge conflicts"
git push
```

## Common Commands

### Repository Status
```bash
# Check working directory status
git status

# View commit history
git log

# View remote repository info
git remote -v
```

## Best Practices

1. **Branch Management**
   - Create new branches for new features/changes
   - Use descriptive branch names
   - Delete merged branches to keep repository clean

2. **Commits**
   - Write clear, descriptive commit messages
   - Make small, focused commits
   - Commit frequently

3. **Synchronization**
   - Pull changes from main branch frequently
   - Resolve conflicts promptly
   - Test changes before pushing

4. **Safety**
   - Don't commit sensitive information
   - Back up important changes
   - Be careful with force push

5. **Workflow**
   - Pull before starting new work
   - Test changes before committing
   - Review changes before pushing

## Additional Resources

- [Git Download to your System](https://git-scm.com/downloads)
- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com)
- [Git Cheat Sheet](https://training.github.com/downloads/github-git-cheat-sheet.pdf)


## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
