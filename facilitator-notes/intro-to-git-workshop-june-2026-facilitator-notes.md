# Facilitator Notes — Intro to Git Workshop, June 2026
### PRIVATE — not for attendees

---

## Opening — Your Intro (say this verbatim or close to it)

> "Hello folks — welcome! My name is Anennya. I run the Build Together program at WDAI. I have been part of WDAI since it was created, three years ago, and I have been running the Build Together program for a year and a half.
>
> Build TogetHER is one of my favorite things we do at Women Defining AI because it's rooted in something really simple but powerful: we learn by building together. Not by waiting until we feel ready. Not by watching only polished demos. But by getting hands-on, asking questions, getting stuck, debugging, researching, trying again, and slowly turning an idea into something real.
>
> So as we go, please feel free to participate in whatever way works for you. You can follow along as I do the demo, or listen and observe, ask questions. This is a shared learning space — and most importantly, a safe space. No question is too basic. We can help you offline if it's too overwhelming to ask during the session.
>
> We have a guide we'll follow today, but I want to be clear: this session is meant to meet you where you are. If questions come up, we'll go there. If something needs more time, we'll slow down. The guide is a map, not a script.
>
> Today we are going to explore and understand Git. I thought about creating a presentation — but since we're going to be in Git, we'll just have that there."

---

## Timed Agenda (2 hours)

| Time | Section |
|------|---------|
| 0:00–0:10 | Welcome + framing |
| 0:10–0:20 | What is Git / Why it matters |
| 0:20–0:30 | Core concepts + vocab |
| 0:30–0:50 | Setup (wildcard — build in buffer) |
| 0:50–1:00 | GitHub tour |
| 1:00–1:10 | Create your own repo |
| 1:10–1:25 | Clone + make a change + commit |
| 1:25–1:35 | Push + view history |
| 1:35–1:45 | Best practices + what never goes in a repo |
| 1:45–1:55 | GitHub + AI tools (Claude Code, CLAUDE.md, revert) |
| 1:55–2:00 | Branches/PRs preview + wrap-up |

---

## "We're Doing This the Hard Way" — say this early and repeat it

- We're walking through the manual steps so you understand what AI tools do automatically
- Claude Code, Lovable, Cursor — they all do this exact same sequence under the hood
- When you know the steps, you can recognize what happened, troubleshoot, and give better instructions
- Repeat this frame whenever someone asks "can't Claude just do this?" — yes, and knowing why it works makes you better at using it

---

## What Is Git / Why It Matters

- "Glorified Google Drive — but with way more detail about what changed and who changed it, and it's much easier to go back"
- The key AI builder point: **you can instruct Claude on HOW to commit** — branch names, commit message format, when to push — put it in CLAUDE.md and it follows it every session
- Changes happen fast with AI. GitHub is the place you slow down and ask: what actually changed?

---

## Core Concepts

- Run through the vocab table quickly — one sentence each
- Emphasize: **commit** (the big idea), **push** (sends it to GitHub), **clone** (gets it to your laptop)
- Defer: branch and pull request — "we'll come back, don't worry about these yet"
- End with: "The workflow today is four steps: clone, edit, commit, push. That's it."

---

## Setup (the wildcard — expect this to take time)

- Have helpers roaming — don't let one person's issue stall the group
- At 0:45, call time and keep moving; helpers stay with anyone still stuck

**Common issues:**
- GitHub Desktop won't open on Mac → System Settings → Privacy & Security → allow it
- Git not installed on Windows → search "terminal" in the taskbar search bar, then `git --version`; if missing, recommend GitHub Desktop which bundles Git
- Work laptop can't install software → use GitHub.com in the browser for the concepts; flag for offline follow-up
- GitHub Desktop sign-in loops → Preferences → Accounts → sign in again

**Text editors — be explicit:**
- Word and Google Docs do NOT work
- Recommend: VS Code or Cursor
- Fallback: TextEdit (Mac), Notepad (Windows)
- Don't edit files on the GitHub website — skips the whole local workflow

---

## GitHub Tour

**Must mention:**
- URL structure: `github.com/org-name/repo-name` — it tells you everything
- README is for humans first — write it for people, not for AI (AI can read it too)
- Commit history: **spend a minute here** — click a commit, show the diff, explain green/red
- "This right here — this is the most important view in all of GitHub. This is how you review what Claude did."
- Every commit is a checkpoint. Everything in Git is recoverable.
- Clone vs. Download ZIP vs. Fork — cover the table; fork is when you don't have write access to someone else's repo (open source, public templates) — most of the time, you clone

---

## Create Your Own Repo

- Walk slowly — wait for people
- **Make sure they check "Add a README file"** — easiest way to have something to clone immediately
- Public vs. private: when in doubt, start private — you can always make it public later

---

## Clone + Make a Change

**Must mention:**
- Cloning creates a folder automatically — you don't need to create one first
- Navigate to it: GitHub Desktop just opens it; terminal users: `cd <repo-name>`
- Is it safe to clone a public repo? Yes — cloning is just copying files. Risk is only if you *run* executables. Check: star count, forks, MIT license. Can also ask Claude to review a repo URL.

**Making the change:**
- Open with a text editor (not Word, not the website)
- Make any change — the content doesn't matter, the habit does
- Save before committing (Cmd+S / Ctrl+S)

---

## Commit + Push

- **Go slowly — this is the moment of the session**
- Narrate every click: "I'm in the Summary field at the bottom left..."
- Commit message formula: Verb + what changed. "Add notes file." Not "stuff."
- After push: "Go to your repo on GitHub.com and refresh. Your commit is there. You just did the whole Git workflow."
- Give them a moment to see that

---

## Best Practices

**When to commit:**
- After one focused, working thing
- Before something risky
- After reviewing an AI-generated change
- Not after every single line — think in meaningful units

**Branch naming:**
- Hyphens not spaces: `update-homepage`
- Descriptive but short
- Prefixes: `feature/`, `fix/`, `experiment/`
- Avoid: `branch1`, `test`, `new`, `my-branch`

---

## What Never Goes in a Repo

**Must mention:**
- API keys, passwords, .env files, personal data — never commit these
- The mechanism: `.env` file stores secrets locally; `.gitignore` tells Git to never upload it
- Claude can still read `.env` to run your app — it just won't be pushed
- "You can ask Claude: add a .gitignore and make sure .env is in it"
- If you accidentally commit a secret: change/rotate the key immediately — deleting the file isn't enough

---

## GitHub + AI Tools

**Must mention:**
- The safe Claude Code workflow: start from working version → one focused change → review diff → test → commit
- Ask before committing: did it only touch what I asked? Do I understand it?
- **CLAUDE.md**: a file in your repo that gives Claude standing instructions — include git workflow rules (branch naming, commit format, what not to touch)
- **You can tell Claude how to commit** — this is a superpower for staying organized
- **Reverting**: GitHub Desktop → History → right-click → Revert. Terminal: `git revert HEAD` (safe). Don't use `git reset --hard` unless you really know what you're doing.
- Lovable auto-commits — great for checkpointing, but check the diffs regularly

---

## Branches + PRs (preview at the end)

**Branches — must mention:**
- Main = trunk (stable). Branch = a new limb you experiment on without touching the trunk.
- Use when: trying something risky, building a new feature, asking Claude to make bigger changes
- Create in GitHub Desktop: Current Branch dropdown → New Branch
- Terminal: `git checkout -b feature/name`
- Switch back to main: `git checkout main`
- Claude Code creates branches automatically when it makes bigger changes — same workflow you just learned

**Pull Requests — must mention:**
- A PR is a proposal: "here's what changed on my branch — should we bring it into main?"
- The diff view is the key — green added, red removed — review before merging
- Even solo, PRs build the habit of reviewing before accepting
- "The AI drafts the change. You review and approve it."

---

## If the Room Goes Quiet — Q&A Starters

- "What was the most confusing part of today?"
- "Has anyone tried GitHub before and had a bad experience? What happened?"
- "What would you use GitHub for in your own project?"
- "What's the thing you're most nervous about doing?"
- "Who here is using Claude Code or Lovable? Let's talk about how Git fits in."

---

## Common Questions

**"Can't Claude just do all of this for me?"**
> Yes — and knowing what it's doing makes you better at using it. When something breaks, you'll know where to look.

**"What if I mess something up?"**
> That's what Git is for. Every commit is recoverable. The only real danger is committing a secret to a public repo. Everything else can be undone.

**"Do I have to use terminal?"**
> No. GitHub Desktop handles 90% of what you'll need. Use whatever works for you.

**"What's the difference between saving and committing?"**
> Saving updates the file on your disk. Committing creates a named checkpoint in Git history with a message. You can save many times before committing.

**"How often should I commit?"**
> When you finish one working thing. Not every line, not once a week. Think in meaningful units — one feature, one fix, one reviewed AI change.

**"Is it safe to clone a public repo?"**
> Yes — cloning is just copying files. Only run code from sources you trust. Check star count, forks, and license to evaluate trustworthiness.

---

## Logistics Checklist (before you start)

- [ ] Helpers/volunteers know their role (roam during setup)
- [ ] Guide URL ready to share
- [ ] Screen sharing tested
- [ ] `github.com/WomenDefiningAI/github-intro-fun` open in browser
- [ ] GitHub Desktop installed and signed in on your demo machine
- [ ] Know where your demo repo is locally
- [ ] Backup plan for anyone who can't install software (browser-only)
