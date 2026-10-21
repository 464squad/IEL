# How Product 1 Is Graded

> **Due: Monday, Nov 2** · **Presentations: in class, Mon Nov 2 and Wed Nov 4**
> Product 1 is the product you built **for yourself**. We're **not** grading how finished it is. We're grading whether you have a clear plan, real progress you can show, and whether you understand what you built.

> *"I'm not going to be judging you on completeness as much as… here's your spec. I can see what you built, and you have the ability to talk through it."*

---

## The three parts (equal weight)

| Part | Weight | In one sentence |
|---|---|---|
| **1. Your spec** | ⅓ | Your repo's `README.md` is a complete, finalized product spec. |
| **2. Your repo and demo evidence** | ⅓ | Your repo has real code that matches your spec, plus proof that it runs. |
| **3. Your code review presentation** | ⅓ | You can pitch it, walk through how it's built, and answer questions about your code and process. |

Think of it like a **cooking show**. The **spec** is your recipe card. The **repo** is the dish, plus photos of it coming out of the oven. The **code review** is you explaining to the judges how you made it, and answering their questions about why you added each ingredient.

---

## Part 1: Your spec

Your spec lives in your repo as **`README.md`**. It's the first thing anyone sees when they open your repo.

**What "complete" means:** all five sections from the [Spec Guide](./product-spec-guide.md) are filled in, specific, and up to date with what you actually built:

- [ ] **About me (the user)**, with real moments the problem happened and what it costs you
- [ ] **Problem statement**: the full *When… I struggle to… which costs me… This happens because… Right now I… but…* and your **"I'll know this is solved when…"** line
- [ ] **Existing solutions**, and why they fall short *for you*
- [ ] **Features and benefits**, with your **MVP** marked, plus a "Later" list and a "Not doing" list
- [ ] **Tech stack**: front end, back end, data and hosting, a reason for each, and an **architecture diagram** (Mermaid or a photo)

> 💡 **Update your spec as you build.** If you changed your stack or cut a feature, change the README too. A spec that matches what you built beats a spec you wrote in week 3 and never touched again.

---

## Part 2: Your repo and demo evidence

### Your repo
- [ ] It's on **GitHub**, and you've shared the link (see [How to submit](#how-to-submit)).
- [ ] It has **your code**: a working first version of at least one MVP feature. It doesn't have to be finished or pretty.
- [ ] The code **matches your spec**. Someone reading your README and then your code should see the same product.
- [ ] It has **commit history**: lots of small saves over time, not one giant upload the night before. *(Need a refresher? See the [Git & GitHub Setup Guide](./git-github-setup.md).)*
- [ ] **No secrets.** No passwords or API keys in your code. Use a `.env` file, and make sure `.env` is listed in `.gitignore`.

### Demo evidence: show that it runs
Add at least **one** of these to your README in a **"Demo"** section. The further down the list you get, the better:

| Level | What to add | How |
|---|---|---|
| 👍 Good | **Screenshots** of your app working | Take screenshots, drag them into your repo folder, then add `![Home screen](screenshot-home.png)` to your README |
| 👏 Better | A **GIF or short video** (under 2 min) of someone using it | Record your screen with your computer's built-in screen recorder, then add the file to your repo, or upload it to YouTube/Loom (unlisted is fine) and link it |
| 🏆 Best | A **live link**: a deployment URL anyone can open | See the [surface guides](../../surfaces/README.md) for how to deploy each kind of app |

> ⚠️ **`localhost` is not a link.** `http://localhost:3000` only works on *your* computer. It's like giving someone directions to a room in your house. To share it, it has to be deployed, or you show screenshots and video instead.

---

## Part 3: Your code review presentation

This happens **live in class**, one person at a time. Plan for about **5 minutes**, plus a few minutes of questions. You'll present from your repo on GitHub.

### What to cover

1. **Pitch (about 1 min).** Use your spec: who it's for (you), your problem statement, and your "solved when" line. *Why does this product exist?*
2. **How it's built (about 1 min).** Show your **architecture diagram** and **tech stack**. Follow one action through it: *"When I tap Save, the front end sends… to… and it's stored in…"*
3. **Demo (about 1–2 min).** Show it working: live, a deployment URL, or your video and screenshots.
4. **Code walkthrough (about 1–2 min).** Open **one or two files you understand well**. Explain what the code does, line by line where it matters.
5. **What you learned (about 30 sec).** What you didn't know before, how you figured it out, and what you'd build next.

### Questions you might be asked
These are the kinds of questions you'll get. **Practice answering them out loud**, or have an AI agent quiz you (see [Learn with Agents](../../modules/learn-with-agents.md#step-6-prep-for-your-code-review)).

**About your product**
- Why did you choose this problem? How will you know it's solved?
- What's in your MVP, and what did you leave out on purpose?

**About your architecture and stack**
- Why this surface (web, mobile, CLI, desktop or chat)? Why this stack?
- Where does your data live? What happens if you close the app and open it again?
- What happens, step by step, when a user does *[some action]*?

**About your code**
- What does this file or function do? What would happen if I deleted this line?
- Where would you add *[a new feature]*?
- What was the hardest bug, and how did you fix it?

**About your process and AI use**
- What didn't you know at first that you had to research?
- Which AI tool or tools did you use, and for what? Where did the AI get it wrong, and how did you notice?
- How did you build this first version? What did you learn from a tutorial, and what did you change or add yourself?

> 🤖 **Using AI is allowed and expected.** But **you are responsible for every line in your repo.** If an agent wrote code you can't explain, ask it to explain it to you before you present. "I don't know, the AI wrote it" isn't an answer, but "I asked Claude, it suggested X, I didn't understand Y so I asked about it, and here's how it works" is a great answer.

---

## What a strong Product 1 looks like

| | Needs work | Meets expectations | Strong |
|---|---|---|---|
| **Spec** | Sections missing or vague. The problem statement describes a solution. | All sections filled in. Specific problem statement and "solved when" line. Stack and diagram included. | Spec matches what was built, with clear scope (MVP / Later / Not doing) and a reason for each stack choice. |
| **Repo and demo** | Little or no code, or code unrelated to the spec. No evidence it runs. | Code for at least one MVP feature, several commits, screenshots in the README. | A working MVP slice with steady commit history, plus a video, GIF or **live URL**. |
| **Code review** | Can't explain the code or the stack. | Clear pitch and demo. Can explain your architecture and walk through one file. | Confident, specific answers about code, decisions and trade-offs. Can explain how AI was used, and where it was wrong. |

---

## How to submit

By **Monday, Nov 2**, before class:
1. Make sure everything is **committed and pushed** (`git status` should say "nothing to commit").
2. Open your repo on GitHub and **check that your README shows your full spec and a Demo section**.
3. **Submit your repo link** the way your instructor asks (Brightspace or Slack).
4. Have your repo open and ready to present in class on **Mon Nov 2 or Wed Nov 4**.

**Private repo?** Add your instructor as a collaborator: on GitHub, go to **Settings → Collaborators → Add people**.

### Final checklist
- [ ] README = finalized spec (all 5 sections, with an architecture diagram)
- [ ] Code for at least one MVP feature, pushed to GitHub
- [ ] "Demo" section with screenshots, GIF/video, or a live URL
- [ ] No secrets in the repo
- [ ] Practiced my 5-minute pitch, architecture, demo, code walkthrough and lessons learned
- [ ] Practiced answering the questions above
- [ ] Repo link submitted
