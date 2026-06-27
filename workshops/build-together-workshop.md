# GitHub for Builders: Follow-Along Workshop Guide

Welcome to **GitHub for Builders**.

This is a follow-along guide for our Build TogetHER session. Use it during the workshop, and come back to it later when you are building with GitHub, Claude Code, Lovable, Cursor, or other AI tools.

## What We Are Doing Today

By the end of this session, you will:

* Understand what GitHub is for
* Know the most important parts of a GitHub repo
* Clone a repo
* Make a small change
* Create a commit
* Understand how GitHub helps when building with Claude Code and Lovable

Today is not about becoming a Git expert.

Today is about becoming Git-comfortable.

## Before You Start

Please set up the following before the workshop if you can. We will also help at the start of the session.

**1. Create a GitHub Account**

1. Go to github.com.
2. Click **Sign up**.
3. Enter your email, create a password, and choose a username.
4. Verify your email address.

Your account is ready.

**2. Install GitHub Desktop (Recommended)**

GitHub Desktop is a visual app that includes Git. No command line required.

1. Download from desktop.github.com.
2. Install and open it.
3. Sign in with your GitHub account.

**If you prefer the command line instead:**

* **Mac**: Run `git --version` in Terminal. If Git is not installed, macOS will prompt you. Or run `brew install git` if you have Homebrew.
* **Windows**: Download from git-scm.com and run the installer.
* **Linux**: Run `sudo apt install git` (Ubuntu/Debian) or `sudo yum install git` (Fedora/RHEL).

To verify Git is installed: `git --version`

**What you will need on the day:**

* A laptop
* A GitHub account
* GitHub Desktop installed, or Git installed for terminal use

## Workshop Agenda

1. Why GitHub matters for AI builders
2. Core mental model
3. GitHub survival tour
4. Hands-on: create your own repo, make a commit, and push it
5. GitHub with Claude Code and Lovable
6. Commit message examples
7. Optional: intro to branches & pull requests

## Part 1: What is GitHub?

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

## Part 2: Why GitHub Matters, Even If You Are Not Technical

GitHub helps you:

* Save versions of your work
* Recover from mistakes
* See what changed over time
* Collaborate with others
* Share your project
* Keep your work organized
* Connect your project to tools like Claude Code, Lovable, Cursor, Netlify, and Vercel

When you are building with AI tools, changes can happen very quickly. GitHub gives you checkpoints, history, and a safer way to experiment.

## Part 3: Git vs GitHub

You may hear both terms: **Git** and **GitHub**.

For today, you can think of them together. But here is the simple distinction:

* **Git** is the version-control system. It tracks changes.
* **GitHub** is the online place where your project lives and where people collaborate.

Beginner mental model:

> Git is the memory.
> GitHub is the home.

You do not need to fully understand the difference on day one. Together, they help you save, share, review, and recover your project.

## Part 4: The Builder Mental Model

You only need a few concepts to get started.

| Term         | Simple Explanation                   |
| ------------ | ------------------------------------ |
| Repo         | Your project folder/home             |
| README       | The front door of your project       |
| Clone        | Copy a GitHub repo to your computer  |
| Commit       | A saved checkpoint with a note       |
| Push         | Send local commits to GitHub         |
| Pull         | Bring latest changes from GitHub     |
| Issue        | A project to-do item                 |
| Pull Request | Review changes before merging        |
| Branch       | A safe experiment area, useful later |

The most important beginner workflow:

```txt
clone → edit → status → add → commit
```

That is enough for today.

## Part 5: GitHub Tour

Open the workshop repo:

```txt
https://github.com/WomenDefiningAI/github-intro-fun
```

During the tour, we will look at:

* Repo name
* Public/private visibility
* README
* File list
* Green Code button
* Commit history
* Issues tab
* Pull Requests tab
* Settings tab, briefly

### README

The README is the front door of the project.

It usually explains:

* What the project is
* How to use it
* How to set it up
* Any important notes

### File List

The file list shows what is inside the project.

This repo includes:

```txt
README.md
github-101.md
```

There may also be practice files or workshop files added over time.

### Green Code Button

The green **Code** button is how you copy the project.

You may see:

* HTTPS
* GitHub Desktop
* Download ZIP

Important:

```txt
Download ZIP = files only
Clone = files + project history
```

For this workshop, we want to **clone**, not download ZIP.

### Commit History

Commit history is the project timeline.

Every commit is a checkpoint that says:

* What changed
* Who changed it
* When it changed
* A short note about the change

## Part 6: Create Your Own Repo and Clone It

Now we will create your own GitHub repo and clone it to your computer. This is the repo you will use for the rest of the hands-on section.

**Step 1: Create your repo on GitHub**

1. Go to github.com and sign in.
2. Click the **+** icon in the top right and choose **New repository**.
3. Name your repo. Some ideas:

```txt
my-first-builder-repo
ai-builder-playground
github-practice
```

4. Set visibility to **Public** or **Private** — your choice.
5. Check **Add a README file**.
6. Click **Create repository**.

Your repo is now live on GitHub.

**Step 2: Clone it to your computer**

## Option A: Clone with GitHub Desktop

1. In GitHub Desktop, go to **File → Clone Repository**.
2. Click the **GitHub.com** tab and find your new repo.
3. Choose where to save it on your computer.
4. Click **Clone**.

Once cloned, you should have a local copy on your computer.

## Option B: Clone with Terminal

Copy your repo URL from GitHub (green **Code** button → HTTPS), then run:

```bash
git clone <your-repo-url>
cd <your-repo-name>
git status
```

You should see:

```txt
On branch main
nothing to commit, working tree clean
```

That means your local copy is ready.

## Part 7: Make a Small Change

Now we will make a small change to a file.

Open the repo folder on your computer.

You can use:

* VS Code
* Cursor
* Any text editor
* GitHub Desktop’s “Open in editor” option

Create a new file called:

```txt
<your-name>-practice.md
```

Add this content:

```md
# My GitHub Practice File

Today I cloned a GitHub repo and made my first local change.

## What I learned

- A repo is a project folder.
- A commit is a checkpoint with a note.
- GitHub helps builders save and review their work.
```

Save the file.

## Part 8: Check What Changed

Before committing, check what changed.

## Option A: GitHub Desktop

In GitHub Desktop, you should see the new file listed under changes.

You can click the file to see what was added.

## Option B: Terminal

Run:

```bash
git status
```

You should see that Git noticed the new file.

You can also run:

```bash
git diff
```

For a brand-new file, `git diff` may not show much until the file is staged. That is okay.

## Part 9: Create a Commit

A commit is a saved checkpoint with a note.

## Option A: GitHub Desktop

In GitHub Desktop:

1. Look at the changed file.
2. Add a commit message.
3. Click **Commit to main**.

Use this commit message:

```txt
Add GitHub practice file
```

## Option B: Terminal

Stage the change:

```bash
git add workshop-practice.md
```

Commit the change:

```bash
git commit -m "Add GitHub practice file"
```

Now you created a local checkpoint.

## Part 10: Push to GitHub

Now that you have a local commit, send it to GitHub.

Because this is your own repo, you have permission to push.

## Option A: GitHub Desktop

Click the **Push origin** button at the top of the GitHub Desktop window.

That is it. Your commit is now on GitHub.

## Option B: Terminal

```bash
git push
```

After pushing, visit your repo on github.com to confirm the commit is there.

## Part 11: View Commit History

## Option A: GitHub Desktop

In GitHub Desktop, look at the **History** tab.

You should see your new commit.

## Option B: Terminal

Run:

```bash
git log --oneline
```

You should see your commit message near the top:

```txt
Add GitHub practice file
```

## Part 12: What Did We Just Do?

We:

1. Created our own GitHub repo
2. Cloned it to our computer
3. Created a new file
4. Checked what changed
5. Created a commit
6. Pushed to GitHub
7. Viewed the commit history

That is the core Git workflow.

The big idea:

> A commit is a checkpoint for future-you.

## Part 13: Commit Messages

A commit message is the note attached to your checkpoint.

Good commit messages answer:

> What changed?

Use this simple formula:

```txt
Verb + thing changed
```

Good verbs:

```txt
Add
Fix
Update
Remove
Refactor
Rename
Document
Connect
Style
Simplify
```

Good commit messages:

```txt
Add GitHub practice file
Update README
Fix typo in setup instructions
Add workshop notes
Remove placeholder text
Document local setup steps
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

Emotionally understandable. Not useful to future-you.

For bigger changes, you can add more detail:

```txt
Add RSVP form

- Adds name, attendance, headcount, and dietary restriction fields
- Keeps existing page styling
- Not yet connected to Google Sheets
```

## Part 14: GitHub with Claude Code

Claude Code can make changes directly inside your project files.

That is powerful. It also means you need a safe workflow.

A beginner-friendly Claude Code workflow:

```txt
1. Start from a version that works.
2. Ask Claude Code for one focused change.
3. Review what changed.
4. Test the project.
5. Commit the change if it works.
```

Example Claude Code prompt:

```txt
Add an RSVP form with fields for name, attendance, headcount, dietary restrictions, and message. Keep the existing design style. Do not change unrelated files. After making changes, summarize what files you changed.
```

Before committing Claude Code changes, ask:

* Did Claude only change what I asked?
* Does the project still run?
* Did Claude touch unrelated files?
* Did Claude change auth, database, payments, or secrets?
* Do I understand the change enough to keep it?

Helpful Claude Code instruction:

```txt
Before making changes, inspect the project structure and explain your plan. Make one focused change only. Do not modify unrelated files. After making changes, summarize what changed and any files you touched.
```

## Part 15: GitHub with Lovable

Lovable can generate and update apps quickly.

When connected to GitHub, Lovable gives your app a project home and version history.

A beginner-friendly Lovable workflow:

```txt
1. Build or edit in Lovable.
2. Connect the project to GitHub.
3. Review changes in GitHub.
4. Commit meaningful checkpoints.
5. Keep private information and API keys out of the repo.
```

Why GitHub helps with Lovable:

* Your project has a home outside Lovable.
* You can see what changed.
* You can connect to deployment tools.
* You can collaborate with others.
* You can recover from mistakes more easily.

## Part 16: What Never Goes in GitHub

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

This is especially important for public repositories.

If you accidentally commit a secret, deleting the file later may not be enough because GitHub stores history. You may need to rotate the key or token.

## Part 16: Optional Stretch — What Are Branches?

Branches are useful later, but they are not required for your first Git session.

A branch is a safe place to experiment without changing the main version of a project.

Think of it like this:

```txt
main = stable version
branch = experiment version
```

Example:

```txt
main
  └── try-new-homepage
```

Branches are helpful when:

* You want to try a risky change
* You are collaborating with others
* You want to review work before adding it to the main version
* You are using AI tools to make bigger changes

For today, the main thing to remember is:

> Branches are for safe experiments.
> You do not need them to make your first commit.
## Part 17: Optional Stretch — What Is a Pull Request?

A pull request, often called a PR, is a way to review changes before bringing them into the main version of a project.

You do not need to use pull requests for your very first Git session.

But you will see PRs often when:

You collaborate with other people
You use branches
You want someone to review your work
An AI tool like Claude Code makes a bigger change
You want to carefully inspect changes before accepting them

Think of it like this:

Repo = project home
Commit = checkpoint
Branch = safe experiment
Pull Request = review before accepting the experiment
Merge = bring it into the main version
Commit vs Pull Request

A commit is one saved checkpoint.

A pull request is a review packet that may contain one or more commits.

Commit = “I saved this change.”
Pull Request = “Here are the changes I want to bring into the main project. Can we review them?”
What You See in a Pull Request

When you open a pull request, you will usually see:

A title
A description of what changed
A list of commits
A Files changed tab
Comments or review notes
A merge button

The most useful tab for beginners is usually:

Files changed

That is where you can inspect exactly what was added, removed, or edited.

Why PRs Matter for AI Builders

AI tools can make changes quickly.

That is powerful, but it also means you need a place to slow down and review.

A pull request helps you ask:

What did the AI tool change?
Did it only change what I asked for?
Did it touch unrelated files?
Does the change look safe?
Should I accept this into the main version?

A helpful rule:

AI can draft the change. You still review and approve it.

Simple PR Description Template

When creating a pull request, you can use this structure:

-  What changed?

- Why did it change?

- How can someone test it?

- Anything risky or worth reviewing carefully?

Example:

 What changed?

Added a basic RSVP form to the event page.

 Why did it change?

We want guests to be able to submit their attendance and dietary restrictions.

 How can someone test it?

Open the event page and confirm the form fields appear.

 Anything risky or worth reviewing carefully?

The form is not connected to a database yet.
Beginner Rule

For today, remember:

A commit is a checkpoint.
A pull request is a review step.

You do not need to practice PRs right away. First get comfortable with:

clone → edit → status → add → commit → log

Pull requests will make more sense once commits feel familiar.

## Part 18: After-Workshop Practice

After the workshop, practice this flow again:

```txt
clone → edit → status → add → commit → log
```

Then try:

1. Create your own repo
2. Add a README
3. Clone it locally
4. Make a small change
5. Commit the change
6. Push it back to GitHub

## Final Mantra

```txt
Clone the project.
Make a small change.
Commit a checkpoint.
Build safely.
```

GitHub is not the goal.

Building safely is the goal.

Happy building 🚀
