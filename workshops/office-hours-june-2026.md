# GitHub for Builders — Office Hours Follow-Along Guide
### June 2026 | Women Defining AI

Welcome back! This is a casual, beginner-friendly session. There are no dumb questions here, and you do not need to have everything perfectly set up.

This guide is yours to follow along with, refer back to, and share.

---

## What We're Covering Today

- A quick recap of the basics from last time
- Forking vs. Cloning — what's actually the difference?
- What branches are and when you'd actually use one
- What pull requests are and how to open one
- A walkthrough from Patty on how she uses Claude Code + Git for a non-coding project
- Open Q&A — bring your "wait, what just happened?" moments

---

## Part 1: Quick Recap

Last time we covered the foundations. Here's a one-line refresher on each concept:

| Term | What it means |
|------|---------------|
| **Repository (repo)** | A folder for your project that GitHub tracks |
| **Clone** | Downloading a copy of a repo to your computer |
| **Commit** | Saving a snapshot of your changes with a message |
| **Push** | Sending your local commits up to GitHub |
| **Pull** | Downloading the latest changes from GitHub to your computer |

If any of these feel fuzzy, that's okay — they'll make more sense as we use them today.

---

## Part 2: Forking vs. Cloning — What's the Difference?

This came up last time, and it's a really good question: **Is forking safer than cloning?**

Short answer: neither is safer — they do different things.

| | Clone | Fork |
|---|---|---|
| **What it is** | A local copy of a repo on your computer | Your own copy of a repo on GitHub |
| **Where it lives** | Your machine | Your GitHub account |
| **Connected to the original?** | Yes, directly | Yes, but through GitHub |
| **Can you push changes back?** | Only if you have permission to the original | Always — to your fork |
| **When to use it** | Working on a repo you own or have been given access to | Contributing to someone else's repo you don't have write access to |

### The mental model

- **Clone** = "I want to work on this project on my computer"
- **Fork** = "I want my own copy of this project on GitHub, separate from the original"

Most of the time, if you're working on your own project or a project where you've been added as a collaborator, **you just clone it**.

Forking is most useful when you want to contribute to a public repo you don't own — like a library or open source project. You fork it, make your changes, and then propose those changes back to the original via a pull request.

> **For our workshop repos:** you'll clone, not fork. You have access as collaborators.

---

## Part 3: What Are Branches?

Think of your project as a tree. The **main** branch is the trunk — the stable, "official" version of your project.

A **branch** is like a new limb you grow off the trunk. You can experiment on that branch — add things, change things, break things — without touching the trunk. When you're happy with what's on the branch, you can merge it back into main.

### Why does this matter?

Branches let you:
- Experiment without breaking the main version
- Work on one thing while main stays stable
- Try out an AI-suggested change before committing it permanently
- Collaborate with others without overwriting each other's work

### When would you actually use a branch?

- "I want to try a new homepage layout without breaking the current one"
- "I'm adding a new feature and I'm not sure it'll work yet"
- "Claude Code is about to make a bunch of changes — I want those on a branch so I can review them"

### How to create a branch

**In GitHub Desktop:**
1. Open your repo in GitHub Desktop
2. Click **Current Branch** at the top
3. Click **New Branch**
4. Name it something descriptive (e.g., `update-homepage` or `experiment-new-layout`)
5. Click **Create Branch**

You're now on that branch. Any commits you make will go there, not to main.

**In the GitHub website:**
1. Go to your repo
2. Click the branch dropdown (it says `main` by default)
3. Type a new branch name
4. Click **Create branch**

---

## Part 4: What Are Pull Requests?

A **pull request** (PR) is a way to say: "Hey, I made some changes on this branch — can we review them and bring them into main?"

Even if you're working alone, PRs are useful because they give you a built-in review step. Before anything merges into main, you get to see exactly what changed.

### What you'll see in a PR

- **The diff** — a side-by-side view of what was there before vs. what you're proposing. Green = added. Red = removed.
- **Comments** — you or others can leave feedback on specific lines
- **Merge button** — when you're ready, you merge the branch into main

### How to open a pull request

1. Make sure you've committed and pushed your changes on a branch (not main)
2. Go to your repo on GitHub
3. You'll see a yellow banner: **"Compare & pull request"** — click it
4. Add a title describing what changed
5. Add a description if it's helpful
6. Click **Create pull request**
7. Review the diff — do the changes look right?
8. Click **Merge pull request** when you're ready

> **The key mindset shift:** a PR is not just a technical step. It's a moment to slow down and ask: "What changed? Do I understand it? Do I approve it?"

---

## Part 5: Patty's Walkthrough — Claude Code + Git for a Non-Coding Project

You don't have to be a software engineer to benefit from version control. Patty is going to show us how she uses Claude Code and Git together for her own non-coding work.

### What to watch for

As Patty walks through her workflow, notice:

- How she uses Claude Code to make changes
- How those changes show up in GitHub — as a branch, a commit, a PR
- What the diff looks like (even for non-code files like text or markdown)
- How she reviews and approves the changes before they become "official"

### Why this matters for builders

Most AI tools — Claude Code, Lovable, Cursor — follow the same pattern when they make changes:

```
branch → commit → push → pull request
```

The AI handles the mechanics. But *you* are the one who reviews the PR, looks at the diff, and decides whether to merge.

That's the moment of control. That's where your judgment lives.

GitHub isn't just for developers. It's a safety net for anyone building with AI tools.

---

## Part 6: The AI Connection — Why This Still Matters

One of the most common questions from last time was: **"Do we really need to learn this if AI tools handle it for us?"**

Here's the honest answer: AI tools *do* handle a lot of the mechanics. But they're still working with repos, branches, commits, and pull requests under the hood.

When you understand those concepts, you can:

- **Know what happened** — not just that Claude Code "made changes," but *what* changed and *where*
- **Review before you accept** — open the PR, look at the diff, decide if it looks right
- **Recover if something breaks** — every commit is a checkpoint; you can roll back
- **Ask better questions** — "Claude, can you put these changes on a branch first?" is a much more powerful prompt than "Claude, make some changes"

> **The AI is your collaborator. GitHub is where you review its work.**

The goal isn't to become a Git expert. The goal is to understand what's happening to your project so you can build with confidence and control.

---

## Q&A

Now it's your turn. Bring your:

- "Wait, I tried this and it didn't work"
- "I'm confused about \_\_\_"
- "What happens if \_\_\_?"
- "Can you show me \_\_\_ again?"

No question is too basic. We're all building this understanding together.

---

## Want to keep practicing?

- Try creating a branch in one of your own repos
- Make a small change, commit it, and open a PR — even if you're the only one reviewing it
- Look at the diff before you merge — get used to that habit
- If you haven't set up Git locally yet, that's what we're doing tomorrow at the in-person workshop!

---

*This guide lives in the [WomenDefiningAI/github-intro-fun](https://github.com/WomenDefiningAI/github-intro-fun) repo.*
*You can also reference the full [GitHub 101 Guide](./github-101-final.md) for a deeper dive on any of these topics.*
