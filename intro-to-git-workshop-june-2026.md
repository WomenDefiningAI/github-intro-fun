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

We'll look at:

- **Repo name and description** — what the project is
- **README** — the front page; every good repo has one
- **File list** — what's inside the project
- **The green Code button** — this is how you clone
- **Commit history** — the project's timeline of changes
- **Branches** — we'll cover these more later

### Clone vs. Download ZIP

When you click the green Code button, you'll see options including **Download ZIP** and **Open with GitHub Desktop**.

| | Download ZIP | Clone |
|---|---|---|
| What you get | Just the files | Files + full history |
| Connected to GitHub? | No | Yes |
| Can you push changes? | No | Yes |
| Use for | Quick read | Actual work |

**Always clone, not download ZIP**, when you're going to work on something.

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
4. Set visibility to **Public** or **Private** — your choice
5. Check **Add a README file**
6. Click **Create repository**

Your repo is now live on GitHub.

---

## Part 6: Clone Your Repo

Now let's get a local copy on your computer.

**Option A: GitHub Desktop**

1. In GitHub Desktop: **File → Clone Repository**
2. Click the **GitHub.com** tab and find your new repo
3. Choose where to save it on your computer
4. Click **Clone**

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

---

## Part 7: Make a Change

Let's add something to your repo.

Open your repo folder. You can use VS Code, Cursor, any text editor, or GitHub Desktop's "Open in editor" option.

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

Save the file.

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

## Part 13: What Never Goes in a Repo

Before we go further, one important rule:

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

This is especially critical for public repos. GitHub stores history — even if you delete a file later, old commits may still contain the secret.

If you accidentally commit a secret, change/rotate the key immediately. Deleting the file is not enough.

---

## Part 14: GitHub and AI Tools

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

A useful prompt to give Claude Code before it makes changes:
```
Before making changes, explain your plan. Make one focused change only.
Do not modify unrelated files. After making changes, summarize what changed
and which files you touched.
```

### Lovable

When Lovable is connected to GitHub:
- Your project has a home outside of Lovable
- You can see what changed in each update
- You can roll back to a previous version if something breaks
- You can share your project or connect it to deployment tools

**The key habit:** after any AI-generated change, open GitHub and look at the diff. Ask: *Do I understand what changed? Does it look right?*

---

## Part 15: Branches — A Preview

You don't need branches today. But here's the idea for when you're ready.

A branch is a parallel version of your project where you can experiment safely.

```
main = the official, stable version
branch = your scratchpad
```

You work on the branch, and when you're happy with the result, you merge it into main.

This is how Claude Code works when it makes bigger changes — it creates a branch, commits the changes there, and opens a pull request for you to review before anything goes into main.

For now, remember:
> Branches are for safe experiments. You don't need them for your first commit.

---

## Part 16: Pull Requests — A Preview

A pull request (PR) is a proposal to bring changes from a branch into main. It includes a review step before anything is finalized.

You'll encounter PRs when:
- You use branches
- You collaborate with others
- Claude Code or another AI tool makes a bigger change

The most important thing to look at in a PR:

**The diff** — a view that shows exactly what changed. Green = added. Red = removed.

For today:
> A commit is a checkpoint. A pull request is a review step. Both exist to help you understand and control what happens to your project.

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
