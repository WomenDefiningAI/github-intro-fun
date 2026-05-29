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

## The Big Idea

AI tools can help you build faster.

GitHub helps you build safely.

GitHub gives you:

* Checkpoints
* Version history
* A place to review changes
* A way to recover from mistakes
* A project home
* A collaboration space

Think of GitHub as a safety net for builders.

## What You Need

Before we begin, make sure you have:

* A laptop
* A GitHub account
* GitHub Desktop installed, or Git installed for terminal use
* Access to this workshop repo

Workshop repo:

```txt
https://github.com/WomenDefiningAI/github-intro-fun
```

## Workshop Agenda

|      Time | Section                                                   |
| --------: | ------------------------------------------------------    |
|   0–5 min | Why GitHub matters for AI builders                        |
|  5–12 min | Core mental model                                         |
| 12–20 min | GitHub survival tour                                      |
| 20–40 min | Hands-on: clone this repo and create a commit             |
| 40–50 min | GitHub with Claude Code and Lovable                       |
| 50–55 min | Commit message examples                                   |
| 55–60 min | Optional: creating your own repo and intro to branches & PR |

## Part 1: The Builder Mental Model

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

## Part 2: GitHub Tour

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

## Part 3: Clone This Repo

We will clone the workshop repo to our computers.

Repo URL:

```txt
https://github.com/WomenDefiningAI/github-intro-fun
```

## Option A: Clone with GitHub Desktop

This is the beginner-friendly option.

1. Open the repo in your browser.
2. Click the green **Code** button.
3. Choose **Open with GitHub Desktop**.
4. Choose where to save it on your computer.
5. Click **Clone**.

Once cloned, you should have a local copy of the repo on your computer.

## Option B: Clone with Terminal

Open your terminal and run:

```bash
git clone https://github.com/WomenDefiningAI/github-intro-fun.git
```

Move into the project folder:

```bash
cd github-intro-fun
```

Check that Git sees the project:

```bash
git status
```

You should see something like:

```txt
On branch main
nothing to commit, working tree clean
```

That means your local copy is ready.

## Part 4: Make a Small Change

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

## Part 5: Check What Changed

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

## Part 6: Create a Commit

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
git add <your-name>-practice.md
```

Commit the change:

```bash
git commit -m "Add GitHub practice file"
```

Now you created a local checkpoint.

## Part 7: View Commit History

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

## Important Note About Pushing

Because this is a shared workshop repo, you may not have permission to push your commit back to the original repo.

That is okay.

Today’s main goal is to learn how to:

```txt
clone → edit → commit → view history
```

Pushing to GitHub is a next step, usually done in a repo you own or have permission to edit.

## Part 8: What Did We Just Do?

We:

1. Found a GitHub repo
2. Cloned it to our computer
3. Created a new file
4. Checked what changed
5. Created a commit
6. Viewed the commit history

That is the core Git workflow.

The big idea:

> A commit is a checkpoint for future-you.

## Part 9: Commit Messages

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

## Part 10: GitHub with Claude Code

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

## Part 11: GitHub with Lovable

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

## Part 12: What Never Goes in GitHub

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

## Part 13: Optional Stretch — Create Your Own Repo

If there is time, we may create a new repo.

Suggested repo names:

```txt
my-first-builder-repo
ai-builder-playground
daily-os-experiment
lovable-test-project
claude-code-practice
```

A simple README starter:

```md
# My First Builder Repo

## What I want to build

I want to build...

## Who it is for

This is for...

## Tools I might use

- GitHub
- Claude Code
- Lovable
- ChatGPT

## Notes from Git 101

GitHub helps me...
```

Possible first commit message:

```txt
Add first README
```

## Part 14: Optional Stretch — What Are Branches?

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

## Part 15: After-Workshop Practice

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
