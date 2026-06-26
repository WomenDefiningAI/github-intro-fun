# Facilitator Notes — Office Hours June 2026
### PRIVATE — not for attendees

---

## Timed Agenda (60 min total)

| Time | Section | Notes |
|------|---------|-------|
| 0:00–0:05 | Welcome + tone-setting | Casual, no pressure, bring confusion |
| 0:05–0:10 | Quick recap | One-liners only, don't re-teach |
| 0:10–0:20 | Forking vs. Cloning | Address "is forking safer?" directly |
| 0:20–0:30 | Branches | Concept + live demo |
| 0:30–0:40 | Pull Requests | Concept + live demo |
| 0:40–0:50 | Patty's walkthrough | Intro her, then let her drive |
| 0:50–0:60 | Q&A | Use prompt starters if room is quiet |

Adjust freely — if Q&A is rich, let it run. The Patty section can flex shorter.

---

## Part 1: Welcome (0:00–0:05)

**Tone to set:**
- This is a follow-up, not a repeat. We're going deeper, not starting over.
- If last time felt overwhelming, that's normal. Today will be more concrete.
- You don't need to have done anything between sessions. Wherever you are is fine.

**Opening line option:**
> "Last time we set the foundation. Today we're going to build on it — and we're going to make things more concrete with some live demos. And later, Patty's going to show us how she actually uses this stuff day-to-day, which I think will be the most useful part."

---

## Part 2: Quick Recap (0:05–0:10)

Don't re-teach the whole last session. Just activate memory.

**Say something like:**
> "Before we jump into new stuff, let's just do a quick vocabulary refresh — not because you should have memorized this, but because it'll help everything click faster today."

Run through the table in the attendee guide. Ask the room: "Which of these feels the fuzziest?" and spend 30 seconds on whichever one they mention. Then move on.

---

## Part 3: Forking vs. Cloning (0:10–0:20)

**The question from last time:** "Is forking safer?"

**Your answer:**
> "Neither is safer — they do different things. Forking isn't a safety feature, it's a way to make your own copy of a project on GitHub when you don't have permission to push to the original. Cloning is just getting a local copy to work on your computer."

**Key framing to repeat:**
- For our workshop repos: you clone, not fork — you already have access
- Forking is for: open source contributions, experimenting on a public repo you don't own
- Cloning is for: anything you're a collaborator on

**Anticipated follow-up questions:**

*"Can I fork my own repo?"*
> Yes, but it's unusual. You'd normally just clone it. Forking yourself doesn't give you any extra benefit.

*"What happens if I clone someone else's repo and push to it?"*
> If you don't have write access, GitHub will reject the push. You'll get a permission error. That's why forking exists — your fork is yours, so you can always push to it.

*"I cloned the workshop repo but I'm scared to break it. Should I fork instead?"*
> You won't break the shared repo — we set it up so changes go through branches and PRs. But if it makes you feel safer to fork it, that's fine too. The main thing is to practice the workflow.

---

## Part 4: Branches (0:20–0:30)

**Concept framing (say this):**
> "Think of your main branch as the published version of your project. A branch is a drafts folder — you can try stuff in there without touching the published version. When you're happy with it, you merge the draft into the published version."

**Live demo steps (GitHub Desktop):**
1. Open the github-intro-fun repo in GitHub Desktop
2. Click **Current Branch** → **New Branch**
3. Name it `demo-branch-june-2026`
4. Open the repo in your text editor (or GitHub.com)
5. Add one line to `practice/anennya_test.md` — anything
6. Back in GitHub Desktop: you'll see the change in the left panel
7. Write a commit message: `"Add demo line for office hours"`
8. Click **Commit to demo-branch-june-2026**

**What to say while doing it:**
> "Notice I'm on the branch name at the top — not main. Everything I do here only affects this branch. Main is completely untouched."

**Anticipated questions:**

*"How do I switch back to main?"*
> In GitHub Desktop, click the branch dropdown and select `main`. Your branch is still there — you're just viewing main now.

*"What if I accidentally commit to main?"*
> It's not the end of the world. You can create a branch from that point, or just keep working on main if it's just your own project. For collaborative projects, it's a bigger deal — but for now, don't stress about it.

*"Does Claude Code create branches automatically?"*
> Yes — we'll see that in the Patty section. Claude Code will create a branch, make changes, and open a PR. That's exactly the same flow we're doing manually right now.

---

## Part 5: Pull Requests (0:30–0:40)

**Concept framing (say this):**
> "A pull request is a proposal. You're saying: here's what I changed on my branch — let's look at it together before it becomes official. Even if you're working alone, it's a powerful habit because it forces you to review your own work."

**Live demo steps (continuing from branch above):**
1. After committing on `demo-branch-june-2026`, click **Push origin** in GitHub Desktop
2. Go to the repo on GitHub.com
3. You'll see the yellow banner: **"Compare & pull request"** — click it
4. Walk through what they're seeing: title, description field, the diff below
5. Point out: green lines = added, red lines = removed
6. Click **Create pull request**
7. Show the PR page — comments, diff, merge button
8. Optionally: merge it and show the branch disappearing

**What to point at in the diff:**
> "This is the most important view in all of GitHub. This tells you exactly what changed. If Claude Code made a change and you open the PR, this is what you're reviewing. Green = new. Red = deleted. Nothing in main changed yet — this is just the proposal."

**Key point to land:**
> "Before you merge, ask yourself: Do I understand what changed? Does it look right? If yes, merge. If no, ask questions — or go back and fix it. This is your moment of control."

**Anticipated questions:**

*"What if I merge something and it breaks the project?"*
> That's what git history is for. Every commit is a checkpoint. You can revert to a previous version. This is the whole reason we use GitHub.

*"Do I have to open a PR? Can't I just merge directly to main?"*
> Yes, you can push directly to main. PRs are optional but recommended — especially when working with AI tools that might make lots of changes at once. The PR gives you a review step.

*"Can I comment on my own PR?"*
> Yes! It's actually a good habit. Leave notes for future-you explaining why you made a decision.

---

## Part 6: Patty's Walkthrough (0:40–0:50)

**How to introduce Patty:**
> "Now we're going to see how all of this works in the real world — not for a coding project, but for [Patty's use case]. I asked Patty to walk us through her actual workflow because I think seeing it in practice is more valuable than any demo I can give. Patty, take it away."

**What to ask Patty to show (coordinate with her beforehand):**
- Her project repo on GitHub
- Using Claude Code to make a change
- The branch + PR that Claude Code creates automatically
- Opening the PR and looking at the diff
- Deciding to merge (or not)

**Things to narrate/emphasize as she demos:**
- "Notice Claude Code created a branch — that's exactly what we just did manually"
- "There's the diff — same view we just looked at"
- "Patty is the one who decides to merge. The AI proposed; she approves."

**Key message to land after Patty's demo:**
> "Patty is not a software engineer. She's using GitHub as a safety net while building with AI. That's what we want everyone here to be able to do."

---

## Part 7: Q&A (0:50–0:60)

**If the room goes quiet, use these prompts:**

- "What from last time still feels confusing?"
- "Has anyone tried to use GitHub this week and run into something? What happened?"
- "What's the thing you're most nervous about doing?"
- "What would have to be true for GitHub to feel less scary to you?"
- "Who has a Claude Code or Lovable project they want to talk through?"

**Common things people are usually confused about at this stage:**
- "I don't know what branch I'm on" → GitHub Desktop always shows it at the top; GitHub.com shows it in the branch dropdown
- "My push didn't work" → Usually a permissions issue or you're trying to push to a protected branch; check the error message
- "I can't find my changes" → Might be on a branch; check which branch you're on
- "The diff looks terrifying" → Focus on just the green lines (what was added). Red is what's gone. You don't need to read every line.

---

## Things to Keep in Mind

- **Go slower than you think.** People who are new to this need time to see each click.
- **Narrate what you're clicking.** "I'm clicking the branch dropdown at the top..." Don't assume they can follow visually.
- **Normalize confusion.** If something doesn't work during your demo, say "this happens sometimes, here's how I debug it" — that's more valuable than a perfect demo.
- **The Patty section is the most valuable part.** Don't rush to get there; let it breathe.
- **It's okay to not know an answer.** "I don't know, let's look it up together" is a great answer in a session like this.

---

## Post-Session
- Remind attendees: tomorrow is the in-person workshop for anyone who wants hands-on setup help
- Share the follow-along guide link in Discord/Slack/wherever the community lives
- Note any questions that came up that should go into the reference guide
