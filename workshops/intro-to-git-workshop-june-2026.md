# Intro to Git — Hands-On Workshop
### June 2026 | Women Defining AI

Welcome! This is a beginner-friendly, hands-on session. By the end of today, you will have Git set up, a real repo on GitHub, and your first commit.

You do not need any prior experience. You just need your laptop and your curiosity.

---

## What We're Doing Today

By the end of this session, you will:

- Have a GitHub account set up and ready to use
- Understand what a repo, commit, push, and pull are
- Have created your own GitHub repo
- Have made and pushed your first commit
- Understand how Git fits into working with AI tools like Claude Code and Lovable

Today is not about becoming a Git expert. Today is about becoming Git-comfortable.

---

## A Note on How We're Learning

We're going to walk through this manually first — the "hard way."

That means typing commands, creating files ourselves, and committing step by step. This might feel slower than just asking Claude Code to do it.

But here's why it matters: **Claude Code, Lovable, and every other AI tool does these exact same steps under the hood.** When you know what the steps are, you can:

- Recognize what happened when something breaks
- Give better instructions to AI tools ("create a branch before making changes")
- Review AI-generated changes with confidence instead of just hoping they're right

The manual way teaches you the concepts. The AI tools handle the mechanics once you understand them.

---

## Part 1: What Is Git and Why Does It Matter?

### The simple version

**Git** is a version control system. It tracks changes to your files over time.

**GitHub** is the online home where your project lives — and where others can see and collaborate on it.

> Git is the memory. GitHub is the home.

You don't need to fully understand the difference today. Together, they help you save, share, review, and recover your work.

### Why does this matter if you're building with AI?

When you work with AI tools like Claude Code or Lovable, changes can happen very quickly. The AI might rewrite a file, add new files, or delete things — sometimes all at once.

GitHub gives you:

- **Checkpoints** — saved versions you can go back to
- **History** — a record of what changed, when, and why
- **Control** — the ability to review changes before they become permanent
- **Recovery** — a way to undo mistakes
- **Consistency** — you can instruct Claude Code on *how* to commit, what to name branches, and when to push, so your project stays organized as AI tools make changes

> The AI is a fast, capable collaborator. GitHub is where you review its work.

### Git is not just for code

You can use GitHub for:

- Websites and apps
- Workshop guides (like this one!)
- Documentation and notes
- Research
- Product ideas
- Automation workflows
- Community projects

---

## Part 2: Core Concepts

You only need a handful of concepts today. Here's the whole vocabulary:

| Term | What it means |
|------|--------------|
| **Repository (repo)** | Your project folder — tracked by GitHub |
| **README** | The front door of your project — describes what it is |
| **Clone** | Download a copy of a GitHub repo to your computer |
| **Commit** | A saved checkpoint with a note describing what changed |
| **Push** | Send your local commits up to GitHub |
| **Pull** | Download the latest changes from GitHub to your computer |
| **Branch** | A separate version of your project for safe experimentation |
| **Pull Request** | A proposal to bring branch changes into the main version |
| **Fork** | Your own copy of someone else's repo on GitHub |

The core beginner workflow — and all you need for today:

```
clone → edit → commit → push
```

---

## Part 3: Setup

Let's get everything in place. Helpers will come around — raise your hand if you get stuck.

### Step 1: Create a GitHub Account

1. Go to [github.com](https://github.com)
2. Click **Sign up**
3. Enter your email, create a password, and choose a username
4. Verify your email address

Your account is ready.

**Tips for choosing a username:**
- It will be public and appear in your repo URLs
- Keep it professional and recognizable (your name or a variation)
- You can change it later, but it's easier to get it right now

### Step 2: Install GitHub Desktop

GitHub Desktop is a visual app that makes Git easier to use — no command line required.

1. Go to [desktop.github.com](https://desktop.github.com)
2. Download and install it
3. Open GitHub Desktop
4. Sign in with your GitHub account

> **Prefer the terminal?** That's great too. The terminal commands are included throughout this guide alongside the GitHub Desktop steps.

**To verify Git is installed via terminal:**
```bash
git --version
```

If it's not installed:
- **Mac**: macOS will prompt you, or run `brew install git`
- **Windows**: Download from git-scm.com
- **Linux**: `sudo apt install git`

---

## Part 4: Tour of a GitHub Repo

Before we create our own, let's walk through what a repo looks like.

Open this repo: `https://github.com/WomenDefiningAI/github-intro-fun`

### Repo name and description

The repo name appears at the top and in the URL. The URL structure tells you a lot:

```
github.com / WomenDefiningAI / github-intro-fun
             ↑ organization    ↑ repo name
```

When you create your own repo, your username will appear where the organization name is.

### README

The README is the front door of a project — the first thing anyone sees when they visit. It explains what the project is, how to use it, and any important notes.

> **README is primarily written for humans.** It's a landing page for anyone who visits your repo. AI tools can read it too and use it as context, but write it for people first.

Every good repo has a README. Always add one when you create a new repo.

### File list

The file list shows everything inside the project — code, notes, images, config files, documentation. A repo isn't just for code. It's a home for your project.

### The green Code button

This is how you copy the project to your computer. Click it and you'll see several options.

| | Download ZIP | Clone | Fork |
|---|---|---|---|
| **What you get** | Files only | Files + full history | Your own copy on GitHub |
| **Connected to GitHub?** | No | Yes | Yes (via your account) |
| **Can you push changes?** | No | Yes (if you have write access) | Yes (always, to your fork) |
| **Use for** | Quick read | Actual work on repos you own or have access to | Contributing to a repo you don't have write access to |

**Always clone, not download ZIP**, when you're going to work on something.

> **When would you fork?** Fork when you want to contribute to someone else's repo and you don't have write access — for example, an open source library, a public template you want to customize, or a community project. You fork it, make changes on your copy, and then open a pull request to propose those changes back to the original. For this workshop and most day-to-day building, you'll clone, not fork.

### Commit history

Click the **commits** link (you'll see something like "12 commits" near the top of the file list). This is your project's timeline.

Every commit shows:
- What changed
- Who changed it
- When it changed
- A message describing the change

**Click on any commit** to see the diff — a color-coded view of exactly what was added or removed.

- **Green** = added
- **Red** = removed

> This is the most important view in all of GitHub. After an AI tool makes changes, this is where you come to review exactly what happened. Every commit in history is a checkpoint you can return to. Nothing in Git is permanent — everything is recoverable.

---

## Part 5: Create Your Own Repo

Now it's your turn. Let's create a repo that's yours.

**On GitHub:**

1. Click the **+** icon in the top right → **New repository**
2. Name your repo. Some ideas:
   ```
   my-first-repo
   ai-builder-playground
   github-practice
   ```
3. Add a short description (optional but good habit)
4. Check **Add a README file**
5. Click **Create repository**

Your repo is now live on GitHub.

### Public vs. Private

When creating a repo, you'll choose visibility:

**Public** — anyone on the internet can view your repo. Good for:
- Portfolio work
- Learning in public
- Workshop examples and community projects

**Private** — only you and invited collaborators can see it. Good for:
- Personal experiments
- Client work
- Early-stage ideas
- Anything with sensitive information

> **Beginner rule:** When in doubt, start private. You can always make a repo public later — but you can't un-publish something that's already been seen.

---

## Part 6: Clone Your Repo

Now let's get a local copy on your computer.

**Option A: GitHub Desktop**

1. In GitHub Desktop: **File → Clone Repository**
2. Click the **GitHub.com** tab and find your new repo
3. Choose where to save it on your computer
4. Click **Clone**

GitHub Desktop will create a folder on your computer with your repo inside.

**Option B: Terminal**

1. On your repo page, click the green **Code** button → copy the HTTPS URL
2. Run:
   ```bash
   git clone <your-repo-url>
   cd <your-repo-name>
   git status
   ```

You should see:
```
On branch main
nothing to commit, working tree clean
```

That means your local copy is ready and synced with GitHub.

> **Where does the folder go?** When you clone, Git creates a new folder with your repo's name inside whatever location you chose. You don't need to create a folder first — Git creates it for you. On Mac, Documents is a good place. On Windows, your user folder works.

### Is it safe to clone a public repo?

Yes — cloning is just copying files. The risk only comes if you explicitly *run* executable files from an unknown source.

If you're evaluating whether a public repo is trustworthy:
- Check the star count and fork count — more is generally better
- Look for an MIT or Apache license
- Check when it was last updated
- When in doubt, you can paste the GitHub URL into Claude and ask: *"Can you review this repo and tell me if anything looks suspicious?"*

---

## Part 7: Make a Change

Let's add something to your repo.

### Open your repo folder

Open the folder you just cloned. You can use:
- **VS Code** or **Cursor** (recommended)
- **TextEdit** on Mac (built-in, works fine)
- **Notepad** on Windows (built-in, works fine)

> **Do NOT use Microsoft Word or Google Docs.** They add invisible formatting that breaks plain text files. Use a plain text editor only.

> **Do NOT edit files directly on the GitHub website.** You can do it, but it skips the local workflow and defeats the purpose of Git. Always edit locally.

### Create a new file

Create a new file called:
```
<your-name>-notes.md
```

Add this content (customize it however you like):

```markdown
# My GitHub Notes

Today I created my first GitHub repo and made my first commit.

## What I learned

- A repo is a project folder tracked by GitHub
- A commit is a saved checkpoint with a note
- Git helps me track what changed, when, and why

## What I want to use GitHub for

(Write something here — your project, your use case, anything)
```

Save the file (Cmd+S on Mac, Ctrl+S on Windows).

---

## Part 8: Check What Changed

Before we commit, let's look at what Git noticed.

**Option A: GitHub Desktop**

You'll see the new file listed in the left panel under **Changes**. Click it to see the content — green means it was added.

**Option B: Terminal**

```bash
git status
```

You'll see your new file listed as untracked. That means Git sees it exists but hasn't saved it as a checkpoint yet.

---

## Part 9: Make Your First Commit

A commit is a checkpoint. You're saying: "Save this moment, with this note."

**Option A: GitHub Desktop**

1. In the bottom left, you'll see a **Summary** field
2. Type your commit message:
   ```
   Add personal notes file
   ```
3. Click **Commit to main**

**Option B: Terminal**

```bash
git add <your-name>-notes.md
git commit -m "Add personal notes file"
```

You've made your first commit. It lives on your computer for now.

### What makes a good commit message?

A commit message answers: **What changed?**

Simple formula: `Verb + what changed`

Good examples:
```
Add personal notes file
Update README with project description
Fix typo in setup instructions
Remove placeholder content
```

Less helpful examples:
```
changes
stuff
fix
final v2
asdf
Claude did things
please work
```

Emotionally understandable. Not useful to future-you.

---

## Part 10: Push to GitHub

Your commit is saved locally. Now let's send it to GitHub so it's backed up and visible online.

**Option A: GitHub Desktop**

Click **Push origin** at the top of the window.

**Option B: Terminal**

```bash
git push
```

Now go to your repo on GitHub.com and refresh the page. You should see your new file and your commit message in the history.

---

## Part 11: View Your Commit History

**Option A: GitHub Desktop**

Click the **History** tab on the left. You'll see your commit with the message and timestamp.

**Option B: Terminal**

```bash
git log --oneline
```

You'll see something like:
```
a3f92c1 Add personal notes file
b1e4d8a Initial commit
```

Every line is a checkpoint. Every checkpoint is recoverable.

---

## Part 12: What Just Happened?

Let's take a breath and recap what we just did:

1. Created a GitHub account and installed GitHub Desktop
2. Created a repo on GitHub
3. Cloned it to our computer
4. Created a new file
5. Made a commit — a saved checkpoint
6. Pushed it to GitHub
7. Viewed the commit history

This is the core Git workflow:

```
clone → edit → commit → push
```

This is also exactly what AI tools like Claude Code are doing under the hood when they make changes to your projects.

---

## Part 13: Commit Messages and Best Practices

### When should you commit?

- When you finish one focused, working thing
- Before you try something risky or experimental
- After an AI tool makes a change you've reviewed and approved
- At the end of a work session, so you don't lose progress
- Whenever you'd want a checkpoint to return to

**Commit working code.** Don't commit half-finished work to main — if something is broken mid-build, use a branch (more on that below). The goal is that every commit on main represents a working state you could return to.

**Don't batch everything into one giant commit.** Small, focused commits are easier to review, easier to revert, and more useful as checkpoints.

### Branch naming best practices

When you create a branch, give it a name that describes what you're working on:

- Use hyphens, not spaces: `update-homepage` not `update homepage`
- Be short but specific: `fix-login-bug` not `fix`
- Common prefixes: `feature/`, `fix/`, `experiment/`, `update/`
  - `feature/add-rsvp-form`
  - `fix/mobile-layout`
  - `experiment/new-color-scheme`

Avoid: `branch1`, `test`, `new`, `my-branch`, `untitled`

If you're working with others (or with Claude Code on a team project), including your name and date helps track ownership:
```
anennya-2026-06-27-update-homepage
```

---

## Part 14: What Never Goes in a Repo

One important rule before you start pushing code:

**Never commit:**
```
API keys
Passwords
Private tokens
.env files
Customer data
Personal data
Financial information
Private documents
```

This is especially critical for public repos. GitHub stores full history — even if you delete a file later, old commits may still contain the secret. If you accidentally commit a secret, change/rotate the key immediately. Deleting the file is not enough.

### How to keep secrets out: `.env` and `.gitignore`

**The `.env` file** is where you store API keys and secrets locally. It looks like this:

```
OPENAI_API_KEY=sk-abc123
DATABASE_URL=postgres://...
```

Claude and your app can read this file to access those keys — but you don't want it going to GitHub.

**The `.gitignore` file** is a list of files you tell Git to never upload. You add `.env` to it:

```
.env
.env.local
*.log
node_modules/
```

Once a file is in `.gitignore`, Git ignores it completely — it won't show up in your changes and won't be committed.

> **You can ask Claude to set this up:** "Add a `.gitignore` file to this project and make sure `.env` is listed." It knows exactly what to do.

---

## Part 15: GitHub and AI Tools

### Claude Code

Claude Code makes changes directly inside your project files. That's powerful. Here's a safe workflow:

```
1. Start from a version that works
2. Ask Claude Code for one focused change
3. Review what changed (look at the diff!)
4. Test that everything still works
5. Commit if it looks good
```

Before committing any AI-generated change, ask yourself:
- Did it only change what I asked for?
- Did it touch unrelated files?
- Do I understand the change?
- Does the project still run?

**A useful prompt to give Claude Code before it makes changes:**
```
Before making changes, explain your plan. Make one focused change only.
Do not modify unrelated files. After making changes, summarize what changed
and which files you touched.
```

### Instructing Claude on how to use Git

One of the most powerful things you can do: tell Claude Code *how* you want it to work with Git. You can put these instructions in a file called `CLAUDE.md` in your repo, and Claude will follow them automatically every session.

Example `CLAUDE.md` with Git instructions:

```markdown
# Project Instructions for Claude

## Git Workflow
- Always create a branch before making changes. Name branches like: feature/description or fix/description
- Write commit messages in the format: Verb + what changed (e.g. "Add RSVP form")
- Commit after each focused change, not in bulk
- Never commit .env files or API keys
- After making changes, summarize what files you touched and why

## General Rules
- Keep changes small and easy to review
- Do not rewrite unrelated files
- Ask before changing anything related to payments, auth, or database schema
- Prefer simple, readable solutions over clever ones
```

This is how you stay in control even as AI tools make fast changes: you set the rules once, and Claude follows them every time.

### How to revert a commit

Made a commit that broke something? You can undo it.

**Option A: GitHub Desktop**
1. Click the **History** tab
2. Right-click the commit you want to undo
3. Select **Revert changes in this commit**

This creates a new commit that undoes the previous one — your history stays intact.

**Option B: Terminal (safe)**
```bash
git revert HEAD
```
Creates a new "undo" commit. Safe to use anytime.

**Option B: Terminal (destructive — use with caution)**
```bash
git reset --hard HEAD~1
```
Erases the last commit entirely. Only use this if you haven't pushed yet and are sure you want to wipe it.

> When in doubt, use `git revert` — it's always safe. You can also just ask Claude: "The last change you made isn't working. Can you revert it?"

### Lovable

When Lovable is connected to GitHub:
- Your project has a home outside of Lovable
- You can see what changed in each update
- You can roll back to a previous version if something breaks
- You can share your project or connect it to deployment tools

Lovable commits automatically with almost every change. That's great for checkpointing, but it means your commit history can get noisy. Look at the diffs regularly to stay aware of what's changed.

**The key habit:** after any AI-generated change, open GitHub and look at the diff. Ask: *Do I understand what changed? Does it look right?*

---

## Part 16: Branches

You don't need branches today. But here's the idea for when you're ready — and it's important context for how AI tools work.

### The mental model

Think of your project as a tree. **Main** is the trunk — the stable, official version. A **branch** is a new limb you grow off the trunk.

```
main (trunk — stable, official)
  └── feature/add-contact-form  ← your branch
  └── experiment/new-homepage   ← another branch
```

You work on a branch, and when you're happy, you merge it back into main. The trunk never changes until you decide it should.

### When would you use a branch?

- You want to try something experimental without risking the working version
- You're adding a feature that will take multiple sessions to finish
- You're asking Claude Code to make a bigger change and want to review it before it goes to main
- You're collaborating with others and don't want to overwrite each other's work

### How to create a branch

**GitHub Desktop:**
1. Click the **Current Branch** dropdown at the top
2. Click **New Branch**
3. Name it (e.g., `experiment-new-layout`)
4. Click **Create Branch**

You're now on that branch. Any commits you make stay there, not on main.

**Terminal:**
```bash
git checkout -b feature/add-contact-form
```

To switch back to main:
```bash
git checkout main
```

To see all your branches:
```bash
git branch
```

### The AI connection

When Claude Code makes a bigger change to your project, it typically creates a branch automatically, commits there, and opens a pull request for you to review. That's exactly this workflow — you just watched it happen manually.

For a deeper explanation, see the [Branches section in the GitHub 101 Guide](./github-101-final.md#branches).

---

## Part 17: Pull Requests

A pull request (PR) is a proposal to bring changes from a branch into main. It includes a built-in review step — before anything is finalized, you get to look at exactly what changed.

### What you see in a PR

- **The diff** — green = added, red = removed. This is the most important view.
- **A list of commits** included in the branch
- **Comments** — you or reviewers can leave notes on specific lines
- **The merge button** — when you're ready to make it official

### How to open a pull request

1. Commit and push your changes on a branch (not main)
2. Go to your repo on GitHub.com
3. You'll see a yellow banner: **"Compare & pull request"** — click it
4. Add a title and description
5. Click **Create pull request**
6. Review the diff — does everything look right?
7. Click **Merge pull request** when you're ready

### Why PRs matter even when you're working alone

A pull request forces a review step before anything goes to main. It's a moment to slow down and ask:
- What changed?
- Do I understand it?
- Do I approve it?

> **The AI can draft the change. You review and approve it. That's the whole pattern.**

For a deeper explanation, see the [Pull Requests section in the GitHub 101 Guide](./github-101-final.md#pull-requests).

---

## Keep Practicing

After today, try this on your own:

1. Open your repo and make another small change
2. Commit it with a clear message
3. Push it and verify it shows up on GitHub
4. Look at your commit history — see your timeline growing

When you're ready to go further:
- Try creating a branch
- Open a pull request
- Add a `CLAUDE.md` to one of your projects and give Claude git instructions
- Connect a project to Claude Code or Lovable and review the changes in GitHub

---

## Your Core Mantra

```
Clone the project.
Make a small change.
Commit a checkpoint.
Build safely.
```

GitHub is not the goal. Building safely, with confidence and control, is the goal.

---

*This guide lives in the [WomenDefiningAI/github-intro-fun](https://github.com/WomenDefiningAI/github-intro-fun) repo.*
*For a deeper reference on any of these topics, see the [GitHub 101 Guide](./github-101-final.md).*
