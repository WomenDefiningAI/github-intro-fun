# GitHub 101

A beginner-friendly guide to understanding and using GitHub as a builder.

This guide is for people who are building projects, websites, AI tools, workflows, prototypes, or experiments — even if you do not think of yourself as "technical."

## What is GitHub?

GitHub is an online workspace where people store projects, track changes, and collaborate.

Think of it as:

> Google Drive + version history + teamwork + project memory

GitHub is commonly used for code, but it is not only for code. You can use it for:

* Websites
* AI app projects
* Documentation
* Notes
* Research
* Product ideas
* Workshop materials
* Automation workflows
* Community projects

## Why GitHub Matters, Even If You Are Not Technical

GitHub helps you:

* Save versions of your work
* Recover from mistakes
* See what changed over time
* Collaborate with others
* Share your project
* Keep your work organized
* Connect your project to tools like Claude Code, Lovable, Cursor, Netlify, and Vercel

When you are building with AI tools, changes can happen very quickly. GitHub gives you checkpoints, history, and a safer way to experiment.

## Git vs GitHub

You may hear both terms: **Git** and **GitHub**.

For today, you can think of them together. But here is the simple distinction:

* **Git** is the version-control system. It tracks changes.
* **GitHub** is the online place where your project lives and where people collaborate.

Beginner mental model:

> Git is the memory.
> GitHub is the home.

You do not need to fully understand the difference on day one. Together, they help you save, share, review, and recover your project.

## Getting Set Up

### Create a GitHub Account

1. Go to github.com.
2. Click **Sign up**.
3. Enter your email, create a password, and choose a username.
4. Verify your email address.

Your account is ready.

### Install GitHub Desktop (Recommended for Beginners)

GitHub Desktop is a visual app that includes Git. No command line required.

1. Download from desktop.github.com.
2. Install and open it.
3. Sign in with your GitHub account.

### Or Install Git for the Command Line

* **Mac**: Run `git --version` in Terminal. If Git is not installed, macOS will prompt you to install it. Or run `brew install git` if you have Homebrew.
* **Windows**: Download from git-scm.com and run the installer.
* **Linux**: Run `sudo apt install git` (Ubuntu/Debian) or `sudo yum install git` (Fedora/RHEL).

Verify the install:

```bash
git --version
```

You should see something like `git version 2.x.x`.

## GitHub Tour

When you open a GitHub repository, you will see a lot of buttons and tabs. You do **not** need to understand all of them right away.

Here are the most important parts to know.

### Repository Name

The repository name appears near the top of the page.

A repository, or repo, is your project folder on GitHub.

Examples:

```txt
my-first-builder-repo
birthday-invite-site
daily-os-app
slack-bot-practice
```

### README

The README is the front door of your project.

It usually explains:

* What the project is
* Why it exists
* How to use it
* How to set it up
* Notes for collaborators
* Notes for future-you

If someone opens your repo, the README is often the first thing they see.

### Files

The file list shows everything inside your project — code, notes, images, configuration files, documentation, data, and more. A GitHub repo is not just for code. It is a home for your project.

### Green Code Button

The green **Code** button is how you copy the project.

You may see options like:

* **HTTPS**: Used to clone the repo to your computer
* **GitHub Desktop**: A beginner-friendly way to work with GitHub locally
* **Download ZIP**: Downloads the files only

Important difference:

> Download ZIP gives you the files.
> Clone gives you the files plus the project history.

### Commit History

Commit history is your project timeline. Every commit is a checkpoint that says:

* What changed
* Who changed it
* When it changed
* A short note about the change

This is one of the main reasons GitHub is useful. You can see how a project evolved over time.

### Pull Requests

A pull request, often called a PR, is a place to review changes before bringing them into the main version of the project.

Think of a PR as:

> "Here is what changed. Should we accept it?"

You do not need to master pull requests right away. They become more useful when you are collaborating, using branches, or reviewing changes from AI tools.

### Issues

Issues are like a project to-do list. You can use them to track bugs, ideas, feature requests, questions, and tasks for yourself or collaborators.

For AI builders, a clear issue can become a clear prompt later.

Example issues:

```txt
Add RSVP form
Fix mobile layout
Update homepage copy
Add Google Sheets integration
Improve error message
```

### Settings

Settings are where repo-level options live. The most important settings to know are public vs private visibility, collaborators, and Pages/deployment settings if you are publishing a website.

## Core Concepts

**Repository (Repo)**: A project folder stored on GitHub. It contains your files and the history of changes to those files.

**Commit**: A saved checkpoint with a note. It creates a point in the project history you can return to, compare, or review later.

**Clone**: Copying a GitHub repository to your computer. When you clone, you get the project files, the project history, and a connection back to the GitHub repo — unlike a ZIP download, which is files only.

**Push**: Sending your local commits up to GitHub.

**Pull**: Bringing the latest changes from GitHub down to your computer.

**Branch**: A parallel workspace to safely make edits without affecting the main project.

**Pull Request (PR)**: A request to merge your changes into the main project after review.

**Fork**: Creating your own independent copy of someone else's repository that you can modify freely.

**Remote**: The version of your repository that lives on GitHub, as opposed to your local copy.

**Merge**: Combining changes from one branch into another.

**README**: The homepage of the project that tells you what it does and how to use it.

**Issues**: The project's to-do list where tasks, bugs, and ideas are tracked.

## Simple Mental Model

| GitHub Term  | Beginner Mental Model              |
| ------------ | ---------------------------------- |
| Repo         | Project folder                     |
| File         | Your content                       |
| README       | Project front door                 |
| Commit       | Save point with a note             |
| Clone        | Copy project to your computer      |
| Push         | Send changes to GitHub             |
| Pull         | Bring latest changes from GitHub   |
| Fork         | Your own copy of someone's repo    |
| Remote       | The GitHub-hosted version          |
| Branch       | Safe experiment area, useful later |
| Pull Request | Review before merging              |
| Issue        | Project to-do item                 |

## GitHub for AI Builders

GitHub becomes especially useful when you are building with AI tools like Claude Code, Lovable, Cursor, ChatGPT, Replit, Bolt, Vercel, or Netlify.

AI tools can generate changes very quickly. That is powerful, but it can also get messy.

GitHub helps you:

* Save checkpoints before trying something risky
* Review what an AI tool changed
* Undo or compare changes
* Keep a stable version of your project
* Collaborate with other people
* Connect your project to deployment tools

A helpful way to think about it:

> AI helps you build faster.
> GitHub helps you build safely.

## Best Practices with Claude Code

Claude Code can make changes directly inside your project files.

Before asking Claude Code to make a big change:

1. Start from a version of your project that works
2. Ask Claude Code for one focused change
3. Review what changed
4. Test the project
5. Commit the change if it works

Example prompt:

```txt
Add an RSVP form with fields for name, attendance, headcount, dietary restrictions, and message. Keep the existing design style. Do not change unrelated files.
```

After Claude Code makes changes, review before committing:

```bash
git status
git diff
git add .
git commit -m "Add RSVP form"
```

The key idea:

> AI can draft the change. You still review and approve it.

### Helpful Claude Code Prompt

```txt
Before making changes, inspect the project structure and explain your plan. Make one focused change only. Do not modify unrelated files. After making changes, summarize what changed and any files you touched.
```

### Add a CLAUDE.md File

For projects using Claude Code, you can add a `CLAUDE.md` file to your repo to give Claude project-specific instructions.

Example:

```md
# Project Instructions for Claude

This is a beginner-friendly AI builder project.

## Rules

- Keep changes small and easy to review.
- Do not rewrite unrelated files.
- Explain what changed after every task.
- Ask before changing database schema, auth, payments, or deployment settings.
- Never add API keys or secrets to the repo.
- Prefer simple readable code over clever code.
```

## Best Practices with Lovable

Lovable can generate and update web apps quickly. When you connect Lovable to GitHub, your project has a more permanent home and you can review changes, collaborate, and keep track of versions.

A safe beginner workflow:

1. Build or edit in Lovable
2. Connect the project to GitHub
3. Review changes in GitHub
4. Commit meaningful checkpoints
5. Keep private information and API keys out of the repo

## Commit Message Best Practices

A commit message is the note attached to a saved checkpoint.

A good commit message answers:

> What changed?

Use this simple formula:

```txt
Verb + thing changed
```

Good commit messages:

```txt
Add RSVP form
Fix mobile navbar
Update homepage copy
Remove placeholder image
Add setup instructions
Connect Supabase client
Style event cards
```

Less helpful commit messages:

```txt
changes
stuff
fix
final
asdf
Claude did things
please work
```

Good verbs to use:

```txt
Add, Fix, Update, Remove, Refactor, Rename, Document, Connect, Style, Simplify
```

For bigger changes, you can add a short description:

```txt
Add RSVP form

- Adds name, attendance, headcount, and dietary restriction fields
- Keeps existing page styling
- Not yet connected to Google Sheets
```

For AI-assisted changes, it can be helpful to note that you reviewed it:

```txt
Add mobile layout improvements

AI-assisted change reviewed manually.

- Adjusts spacing on small screens
- Fixes overflowing RSVP button
- Tested locally
```

> A commit is a checkpoint for future-you.

## Common Git Commands

You do not need to memorize these right away. It is enough to recognize the shape of the workflow.

### Basic Workflow

```bash
git status          # See what files have changed
git add .           # Stage all changes for commit
git add <file>      # Stage a specific file
git commit -m "Add message here"   # Save changes with a message
git push            # Upload changes to GitHub
git pull            # Download changes from GitHub
```

### Repository Setup

```bash
git clone <url>     # Copy a repository from GitHub to your computer
git init            # Initialize a new repository
```

### Branches

```bash
git checkout -b <branch-name>   # Create and switch to a new branch
git branch                       # List all branches
git checkout <branch-name>      # Switch to an existing branch
git branch -d <branch-name>     # Delete a branch
```

### Helpful Commands

```bash
git log            # View commit history
git diff           # See what changed in your files
git remote -v      # View remote repository URLs
git fetch          # Download changes without merging
git merge          # Combine branches
```

## Beginner Workflow: Clone, Edit, Commit

This is the simplest beginner workflow.

### Step 1: Clone the Repo

```bash
git clone <repository-url>
cd <repository-name>
```

### Step 2: Make a Small Change

Edit a file in the project — update a README, add a sentence to a notes file, fix a typo, or add your name to a practice file.

### Step 3: Check What Changed

```bash
git status
```

### Step 4: Stage and Commit

```bash
git add .
git commit -m "Update practice file"
```

### Step 5: View the History

```bash
git log --oneline
```

That is enough for a first Git session.

## Common Scenarios

### Starting a Brand New Repo

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin <your-repo-url>
git push -u origin main
```

### Working on a Feature

```bash
git checkout -b feature-name
# Make your changes
git add .
git commit -m "Add new feature"
git push origin feature-name
# Then create a pull request on GitHub
```

### Getting the Latest Changes

```bash
git pull
```

### Checking What Changed

```bash
git status
git diff
```

## Public vs Private Repositories

**Public**: Anyone can view your repo. Useful for open-source projects, portfolio work, workshop examples, and community learning.

**Private**: Only you and invited collaborators can view your repo. Useful for personal experiments, client work, early-stage ideas, and projects with sensitive information.

**Beginner rule**: When in doubt, start private. You can always make a repo public later.

## What Never Goes in GitHub

Do **not** commit:

```txt
API keys
Passwords
Private tokens
.env files
Customer data
Personal data
Financial information
Medical information
Private documents
```

This is especially important for public repositories. If you accidentally commit a secret, deleting the file later may not be enough because GitHub stores history. You may need to rotate the key or token.

## Troubleshooting

**"Nothing to commit"**: Git does not see any new saved changes. Check that you saved the file, are in the right folder, and haven't already committed this change. Run `git status`.

**"Your branch is behind"**: GitHub has changes your local copy doesn't have yet. Run `git pull`.

**"Merge conflict"**: Git sees two different edits to the same part of a file and needs a human to choose what stays. Edit the conflicting file manually, then commit. This is normal — annoying but not the end of the world.

**"Permission denied"**: GitHub does not know you are allowed to push. You may need to sign in, use GitHub Desktop, or set up authentication. If you do not own the repo, you may not have push access — you can still clone and commit locally.

## Questions Beginners Often Ask

**Do I need to use the command line?**
No. You can start with the GitHub website, GitHub Desktop, or Lovable's GitHub integration. The command line is useful but not the only way.

**What is the difference between save and commit?**
Saving updates a file. Committing creates a named checkpoint in the project history.

**What is the difference between clone and download ZIP?**
Download ZIP gives you the files. Clone gives you the files plus the full project history.

**How often should I commit?**
Commit when you reach a meaningful checkpoint — you added a section, fixed a bug, changed the design, or want a safe point before trying something risky.

**Should I use branches?**
Not on day one. First get comfortable with the basics: clone, edit, status, add, commit, log. Branches come next.

## Next Steps

1. Clone a repo
2. Make a small change
3. Commit the change
4. View the commit history
5. Create your own repo
6. Add a README
7. Make a few commits

Suggested practice repo names:

```txt
my-first-builder-repo
ai-project-playground
daily-os-experiment
lovable-test-project
claude-code-practice
```

## Final Mantra

> Clone the project.
> Make a small change.
> Commit a checkpoint.
> Build safely.

Happy building 🚀
