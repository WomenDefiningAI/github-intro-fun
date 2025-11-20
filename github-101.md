# GitHub 101

A beginner-friendly guide to understanding and using GitHub.

## What is GitHub?

GitHub is an online workspace where people store projects, track changes, and collaborate. Think of it as Google Drive for projects — but with powerful version history and teamwork features.

## Core Concepts

**Repository (Repo)**: A project folder stored on GitHub.

**Commit**: A saved change with a short note describing what you did.

**Branch**: A parallel workspace to safely make edits without affecting the main project.

**Pull Request (PR)**: A request to merge your changes into the main project after review.

**Issues**: The project's to-do list where tasks, bugs, and ideas are tracked.

**README**: The homepage of the project that tells you what it does and how to use it.

**Fork**: Creating your own copy of someone else's repository that you can modify independently.

**Clone**: Downloading a repository from GitHub to your local computer.

**Remote**: The version of your repository that lives on GitHub (as opposed to your local copy).

**Merge**: Combining changes from one branch into another.

## Why It Matters (Even If You're Not Technical)

* Tracks every version of your work
* Makes collaborating easy with comments and approvals
* Keeps everything backed up and transparent
* Great for documenting and sharing projects
* Can be used for writing, research, workflows, or even simple websites

## Simple Mental Model

* **Repo** = Folder
* **Files** = Your content
* **Commit** = Save with a note
* **Branch** = Safe workspace
* **Pull Request** = Review + merge
* **Issues** = To-do list
* **GitHub** = Google Drive + Version History + Teamwork + Automation

## Common Git Commands

### Basic Workflow Commands

```bash
git status          # See what files have changed
git add .           # Stage all changes for commit
git add <file>      # Stage a specific file
git commit -m " "   # Save changes with a message
git push            # Upload changes to GitHub
git pull            # Download changes from GitHub
```

### Repository Setup Commands

```bash
git init            # Initialize a new repository
git clone <url>     # Copy a repository from GitHub to your computer
```

### Branch Commands

```bash
git checkout -b <branch name>    # Create and switch to a new branch
git branch                        # List all branches
git checkout <branch name>       # Switch to an existing branch
git branch -d <branch name>      # Delete a branch
```

### Additional Useful Commands

```bash
git log            # View commit history
git diff           # See what changed in your files
git remote -v      # View remote repository URLs
git fetch          # Download changes without merging
git merge          # Combine branches
```

## Getting Started Workflow

1. **Create or Clone a Repository**
   ```bash
   git clone <repository-url>
   # or
   git init
   ```

2. **Make Changes**
   - Edit files in your project
   - Create new files
   - Delete files

3. **Stage Your Changes**
   ```bash
   git add .
   # or
   git add <specific-file>
   ```

4. **Commit Your Changes**
   ```bash
   git commit -m "Describe what you changed"
   ```

5. **Push to GitHub**
   ```bash
   git push
   ```

## Best Practices

* **Write clear commit messages**: Describe what and why you changed something
* **Commit often**: Small, frequent commits are easier to understand and review
* **Use branches**: Keep your main branch stable by working on feature branches
* **Pull before push**: Always pull the latest changes before pushing your own
* **Review before merging**: Check your changes in a pull request before merging

## Public vs Private Repositories

* **Public**: Anyone can view your code (great for open source projects)
* **Private**: Only you and people you invite can see your code (great for personal projects)

## Common Scenarios

### Scenario 1: Starting Fresh
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <your-repo-url>
git push -u origin main
```

### Scenario 2: Working on a Feature
```bash
git checkout -b feature-name
# Make your changes
git add .
git commit -m "Add new feature"
git push origin feature-name
# Then create a pull request on GitHub
```

### Scenario 3: Updating Your Local Copy
```bash
git pull
```

### Scenario 4: Checking What Changed
```bash
git status
git diff
```

## Troubleshooting

**"Your branch is behind"**: Run `git pull` to get the latest changes

**"Merge conflict"**: GitHub will mark conflicts in files. Edit them manually, then commit

**"Nothing to commit"**: Either you haven't made changes, or you need to `git add` your changes first

**"Permission denied"**: Make sure you're authenticated with GitHub (check your SSH keys or personal access token)

## Next Steps

* Practice by making small changes to this repository
* Explore other open source projects on GitHub
* Create your own repository and experiment
* Join our [GitHub Office Hours](https://luma.com/z56kmlpi) to ask questions!

---

Happy coding! 🚀

