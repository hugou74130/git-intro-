<p align="center">
  <a href="https://github.com/hugou74130/git-intro-" rel="noopener">
 <img width=400px height=200px src="https://image.noelshack.com/fichiers/2025/45/5/1762530279-gemini-generated-image-idt9k1idt9k1idt9.png" alt="Project logo"></a>
</p>

<h3 align="center">git-intro - Git and GitHub Fundamentals</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]()
[![GitHub Issues](https://img.shields.io/github/issues/hugou74130/git-intro-.svg)](https://github.com/hugou74130/git-intro-/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/hugou74130/git-intro-.svg)](https://github.com/hugou74130/git-intro-/pulls)


</div>

---

<p align="center"> Learn and practice fundamental Git commands and GitHub workflow to master version control.
    <br>
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Git Basics](#git_basics)
- [GitHub Workflow](#github_workflow)
- [Common Commands](#common_commands)
- [Contributing](#contributing)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

This repository is dedicated to learning and practicing the fundamental commands of Git and understanding the GitHub workflow. Whether you're new to version control or looking to strengthen your Git skills, this resource will guide you through the essential concepts.

You will learn how to clone repositories, make changes, commit your work, push to remote servers, and manage branches. Understanding version control is crucial for any developer, as it allows you to collaborate with others, track changes, and maintain a complete history of your project.

## 🏁 Getting Started <a name = "getting_started"></a>

### Prerequisites

You will need:

```
- Git (version control system)
- GitHub account
- Terminal or command line
- Text editor or IDE
- Basic command line knowledge
```

### Installation

Install Git:

**On Ubuntu/Debian:**
```bash
sudo apt-get update
sudo apt-get install git
```

**On macOS:**
```bash
brew install git
```

**On Windows:**
Download from [git-scm.com](https://git-scm.com/)

### Initial Setup

Configure your Git identity:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

Verify your configuration:

```bash
git config --list
```

## 🔧 Git Basics <a name = "git_basics"></a>

### What is Git?

Git is a distributed version control system that allows you to:
- Track changes to files over time
- Revert to previous versions if needed
- Work collaboratively with other developers
- Maintain a complete history of your project

### Key Concepts

- **Repository**: A folder that contains all project files and version history
- **Commit**: A snapshot of your changes with a descriptive message
- **Branch**: An independent line of development
- **Remote**: A version of your repository hosted on a server (like GitHub)
- **Local**: Your copy of the repository on your computer

## 💻 Common Commands <a name = "common_commands"></a>

### Basic Workflow

#### Clone a Repository
Downloads a remote repository to your local machine:

```bash
git clone https://github.com/hugou74130/git-intro-.git
cd git-intro-
```

#### Check Status
See which files have changed:

```bash
git status
```

#### Add Changes
Stage files for commit:

```bash
git add filename.txt          # Add specific file
git add .                     # Add all changes
git add *.c                   # Add all .c files
```

#### Commit Changes
Save changes to your local repository with a message:

```bash
git commit -m "Add new feature"
git commit -am "Update documentation"  # Add and commit together
```

#### Push Changes
Upload commits to the remote repository:

```bash
git push origin main          # Push to main branch
git push origin branch-name   # Push to specific branch
```

#### Pull Changes
Download updates from the remote repository:

```bash
git pull origin main          # Pull from main branch
git pull                      # Pull current branch
```

### Branch Management

#### List Branches
View all branches:

```bash
git branch                    # Local branches
git branch -a                 # All branches (local and remote)
git branch -r                 # Remote branches
```

#### Create a Branch
Start a new branch for features:

```bash
git branch feature-name
git checkout -b feature-name  # Create and switch in one command
git switch -c feature-name    # Modern syntax
```

#### Switch Branches
Move between branches:

```bash
git checkout branch-name
git switch branch-name        # Modern syntax
```

#### Delete a Branch
Remove branches you no longer need:

```bash
git branch -d branch-name     # Delete local branch
git push origin --delete branch-name  # Delete remote branch
```

#### Merge Branches
Combine changes from one branch to another:

```bash
git checkout main
git merge feature-name
```

### View History

#### View Commits
See your commit history:

```bash
git log                       # Full log
git log --oneline             # Simplified view
git log --graph --all --oneline --decorate  # Visual branch history
```

#### View Changes
See what changed in recent commits:

```bash
git diff                      # Unstaged changes
git diff --staged             # Staged changes
git diff HEAD~1 HEAD          # Compare last two commits
```

## 🌐 GitHub Workflow <a name = "github_workflow"></a>

### Understanding the Workflow

1. **Fork** the repository (optional, for contributing to others' projects)
2. **Clone** to your local machine
3. **Create a branch** for your feature/fix
4. **Make changes** and test locally
5. **Commit** with clear messages
6. **Push** to your remote branch
7. **Create a Pull Request** for code review
8. **Address feedback** if needed
9. **Merge** once approved

### Pull Requests

#### Creating a Pull Request

1. Push your branch to GitHub:
```bash
git push origin feature-branch
```

2. Go to the repository on GitHub
3. Click "Compare & pull request"
4. Add a descriptive title and description
5. Click "Create Pull Request"

#### Code Review Process

- Team members review your changes
- Request modifications if needed
- Address comments with new commits
- Once approved, merge the PR

### Issues

#### Creating an Issue

Use GitHub issues to track:
- Bug reports
- Feature requests
- Tasks and improvements

#### Linking Issues and PRs

In your commit message or PR description:
```
Fixes #123
Closes #456
Resolves #789
```

## 📚 Best Practices <a name = "best_practices"></a>

### Commit Messages

Write clear, descriptive commit messages:

```bash
# Good
git commit -m "Add user authentication to login page"

# Bad
git commit -m "updates"
git commit -m "fix stuff"
```

### Branching Strategy

- Use descriptive branch names:
  ```
  feature/user-authentication
  bugfix/login-error
  docs/update-readme
  ```

- Keep branches focused on single features
- Delete branches after merging

### Before Pushing

Always check your changes:

```bash
git status
git diff
git log --oneline -5
```

### Pulling Before Pushing

Always pull before pushing to avoid conflicts:

```bash
git pull origin main
git push origin main
```

## 🚀 Advanced Topics <a name = "advanced"></a>

### Undoing Changes

#### Undo Uncommitted Changes
```bash
git checkout -- filename.txt  # Discard changes in working directory
git restore filename.txt      # Modern syntax
```

#### Undo Staged Changes
```bash
git reset HEAD filename.txt   # Unstage file
git reset                     # Unstage all files
```

#### Undo Commits
```bash
git revert HEAD               # Create new commit that undoes changes
git reset --soft HEAD~1       # Undo last commit, keep changes staged
git reset --hard HEAD~1       # Undo last commit, discard changes
```

### Stashing

Temporarily save changes:

```bash
git stash                     # Save changes
git stash list                # View stashed changes
git stash pop                 # Apply and remove from stash
git stash apply               # Apply but keep in stash
```

### Rebasing

Reorganize commits on your branch:

```bash
git rebase main               # Rebase current branch onto main
git rebase -i HEAD~3          # Interactive rebase last 3 commits
```

## 🤝 Contributing <a name = "contributing"></a>

This repository welcomes contributions! To contribute:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## ⛏️ Built Using <a name = "built_using"></a>

- [Git](https://git-scm.com/) - Version Control System
- [GitHub](https://github.com/) - Hosting Service
- [Markdown](https://www.markdownguide.org/) - Documentation Format

## ✍️ Authors <a name = "authors"></a>

- [@hugou74130](https://github.com/hugou74130) - Complete work

See also the list of [contributors](https://github.com/hugou74130/git-intro-/contributors) who participated in this project.

## 📖 Useful Resources

- [Git Documentation](https://git-scm.com/doc)
- [GitHub Guides](https://guides.github.com/)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)
- [Pro Git Book](https://git-scm.com/book/en/v2)

## 🎉 Acknowledgements <a name = "acknowledgement"></a>

- Git community for creating an amazing version control system
- GitHub for providing excellent hosting and collaboration tools
- All learners and contributors who use this resource to improve their skills
- The open-source community for inspiration and support
