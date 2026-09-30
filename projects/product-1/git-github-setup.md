# Product 1: Put Your Spec on GitHub

> **In-class · Wednesday, Sep 30 · no Git experience needed**
> By the end of class, your Product 1 spec will be online in **your own GitHub repository** as its `README.md`, and you'll know the basic loop you'll use all semester: **save → label → upload**.

**Bring:** your laptop, your spec document from Monday ([Spec Guide](./product-spec-guide.md)), and your architecture sketch photo if you made one.

**Never used a terminal or Git before? Good. This guide is written for you.** Go one step at a time, copy the commands exactly, and check off each step before moving on. If you get stuck, look in [Troubleshooting](#troubleshooting) or raise your hand.

---

## Today's steps

| Step | What you'll do | Time |
|---|---|---|
| [0](#0-the-big-picture-git-is-a-save-system) | Understand the big picture (no typing) | 5 min |
| [1](#1-make-a-github-account) | Make a GitHub account | 5 min |
| [2](#2-install-git) | Install Git | 10 min |
| [3](#3-open-a-terminal-and-check-git) | Open a terminal and check Git | 5 min |
| [4](#4-install-the-github-cli-gh) | Install the GitHub CLI (`gh`) | 5 min |
| [5](#5-log-in-to-github-from-your-terminal) | Log in to GitHub from your terminal | 5 min |
| [6](#6-tell-git-who-you-are) | Tell Git who you are | 2 min |
| [7](#7-make-your-product-1-folder-and-add-your-spec) | Make your Product 1 folder and add your spec | 10 min |
| [8](#8-save-your-first-version-commit) | Save your first version (commit) | 5 min |
| [9](#9-put-it-on-github-push) | Put it on GitHub (push) ⭐ | 5 min |
| [10](#10-the-everyday-loop) | Learn the everyday loop | 5 min |
| [11](#11-your-first-pull-request-stretch) | *Stretch:* your first pull request | 15 min |
| [12](#12-connect-an-ai-agent-to-your-repo-stretch--at-home) | *Stretch / at home:* connect an AI agent to your repo | 15 min |

⭐ **Steps 1–9 are today's goal.** Steps 11–12 are for if you finish early, or for at home.

---

## 0. The big picture: Git is a save system

Think of your project like a **video game**.

| Word | What it means | Video game version |
|---|---|---|
| **Git** | A program on your computer that remembers every version of your project | The game's **save system** |
| **Repository** ("repo") | A project folder that Git is watching | Your **save file** for one game |
| **Commit** | A saved version of your project, with a short label | A **save point**. You can always go back to it. |
| **Commit message** | The label on that save | The name you give the save ("Before the boss fight") |
| **GitHub** | A website that stores your repos online | **Cloud saves**: your progress is safe even if your laptop dies, and others can see it |
| **Push** | Upload your commits from your computer to GitHub | **Upload** your saves to the cloud |
| **Pull** | Download the newest commits from GitHub | **Download** your cloud saves onto a device |
| **Branch** | A separate line of work that doesn't touch the main version | A **side quest** or second save slot. Experiment without risking your main story. |
| **Pull request** ("PR") | A request to bring a branch's changes into the main version, with a review first | Asking a teammate "check my side quest before we add it to the main story" |

**Git vs. GitHub:** Git is the save system on your laptop. GitHub is the cloud where those saves live. You use Git *to talk to* GitHub.

**The terminal** is a window where you type instructions to your computer instead of clicking. It's like texting your computer: type a command, press **Enter**, and it replies.

> 💡 **Terminal tips**
> - Type (or paste) a command, then press **Enter**.
> - **Silence is usually good.** Many commands print nothing when they work.
> - Don't type the `$` you might see in examples. It just means "this is a command."
> - Stuck or something running forever? Press **Ctrl + C** to cancel.
> - Paste in the terminal: **Cmd + V** on Mac. In Git Bash on Windows, use **right-click → Paste** or **Shift + Insert**.

---

## 1. Make a GitHub account

*Skip this step if you already have one.*

1. Go to **[github.com/signup](https://github.com/signup)**.
2. **Pick your username carefully.** It will be in your portfolio link (`github.com/your-username`) and employers will see it. Use something simple and professional, like your name.
3. **Use an email you'll keep after graduating** (a personal email is fine). You can add your school email later.
4. Verify your email when GitHub sends you a message.

> 🎓 **Optional, and worth it: GitHub Education.** Verified students get free benefits, including **GitHub Copilot Student** (free AI help, used in [Step 12](#12-connect-an-ai-agent-to-your-repo-stretch--at-home)). Apply at **[education.github.com](https://education.github.com)** with your school email. Approval can take a day or two, so apply today and it'll be ready later.

---

## 2. Install Git

Git is the save system. You install it once.

### Windows
1. Go to **[git-scm.com/downloads](https://git-scm.com/downloads)** and download **Git for Windows**.
2. Run the installer. **Clicking "Next" on every screen is fine.** The default choices work.
3. This also installs an app called **Git Bash**. That's the terminal you'll use on Windows. It understands Git commands better than PowerShell does.

### Mac
Many Macs already have Git. You'll check in the next step. If it isn't there, your Mac will offer to install it for you (see Step 3).

---

## 3. Open a terminal and check Git

### Open your terminal
- **Mac:** press **Cmd + Space**, type **Terminal**, press **Enter**.
- **Windows:** click the **Start** button, type **Git Bash**, and open it. *(Use Git Bash, not PowerShell or Command Prompt.)*
- **Using Cursor or VS Code?** Those have a terminal built in (**Terminal → New Terminal**). On Windows, choose **Git Bash** from the dropdown next to the **+** in the terminal panel.

### Check Git
Type this and press **Enter**:

```bash
git --version
```

- ✅ If you see something like `git version 2.x.x`, you're good.
- ❌ If you see `command not found`:
  - **Mac:** a pop-up may ask to install "command line developer tools." Click **Install**, wait for it to finish, then run `git --version` again.
  - **Windows:** make sure you're in **Git Bash**. If you still get the error, re-run the Git installer from Step 2.

---

## 4. Install the GitHub CLI (`gh`)

The **GitHub CLI** is a small program called `gh` that lets your terminal talk to GitHub. It makes logging in easy (no passwords or keys to copy around) and can create repos and pull requests for you.

### Windows
1. Go to **[cli.github.com](https://cli.github.com)** and click **Download for Windows**.
2. Run the installer.
3. **Close Git Bash and open it again** so it notices the new program.

### Mac
1. Go to **[cli.github.com](https://cli.github.com)** and download the Mac installer, then run it.
   *(If you already use Homebrew, you can run `brew install gh` instead.)*
2. **Close Terminal and open it again.**

### Check it worked

```bash
gh --version
```

✅ You should see `gh version 2.x.x`.

---

## 5. Log in to GitHub from your terminal

This connects **your computer** to **your GitHub account**, like tapping a key card once so the door opens every time after.

```bash
gh auth login
```

It will ask you some questions. Use the **arrow keys** to choose, and press **Enter** to confirm:

| It asks… | You choose… |
|---|---|
| Where do you use GitHub? | **GitHub.com** |
| What is your preferred protocol for Git operations on this host? | **HTTPS** |
| Authenticate Git with your GitHub credentials? | **Yes** |
| How would you like to authenticate GitHub CLI? | **Login with a web browser** |

Then:
1. It shows a **one-time code** like `ABCD-1234`. Copy it (or write it down).
2. Press **Enter**. Your browser opens to GitHub.
3. Sign in if asked, **paste the code**, and click **Continue** and then **Authorize**.
4. Go back to your terminal. You should see **✓ Logged in as your-username**.

Double-check anytime with:

```bash
gh auth status
```

---

## 6. Tell Git who you are

Every save point (commit) gets signed with your name, like signing your work. Run these two lines **with your own name and the email from your GitHub account**. Keep the quotation marks.

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Nothing prints? That means it worked. You only do this once per computer.

---

## 7. Make your Product 1 folder and add your spec

### 7a. Name your project
Pick a short name for your product, all **lowercase**, with **dashes instead of spaces**. Examples: `meal-planner`, `shift-tracker`, `patch-notes-helper`. This becomes your repo's name, so pick something you're OK showing people.

In the commands below, **replace `my-product` with your name.**

### 7b. Make the folder
These commands go to your **Documents** folder, make a new folder, and step inside it:

```bash
cd ~/Documents
mkdir my-product
cd my-product
```

> 🧭 **Where am I?** Type `pwd` ("print working directory") to see which folder you're in. It should end in `/Documents/my-product`. `cd` means "change directory", or "walk into this folder."

### 7c. Add your spec as `README.md`
`README.md` is the front page of every GitHub repo. It's the first thing people see. In this class, **your README *is* your spec.**

1. **Open the folder in a code editor.** We recommend **[VS Code](https://code.visualstudio.com)** (free) or **Cursor**. Choose **File → Open Folder…** and pick `Documents/my-product`.
2. **Create a new file** named exactly **`README.md`** (capital `README`, lowercase `.md`).
3. **Paste your spec** into it and **save** (**Cmd + S** or **Ctrl + S**).
   - **Wrote your spec in Google Docs?** Use **File → Download → Markdown (.md)**, then open that file and copy everything into `README.md`. This keeps your headings and tables.
   - **Wrote it somewhere else?** Copy and paste the text. It's OK if the formatting isn't perfect yet. You can fix it later.
4. **Have an architecture sketch photo?** Drag the image into the `my-product` folder and rename it `architecture.jpg` (or `.png`). Then, in the Tech Stack section of your README, add this line where you want the picture to appear:

   ```markdown
   ![My architecture sketch](architecture.jpg)
   ```

> ⚠️ **Don't use Word or TextEdit** to make `README.md`. They secretly save extra formatting, or add `.txt` to the end, and GitHub won't show your spec correctly.

---

## 8. Save your first version (commit)

Back in your terminal, make sure you're in your project folder (`pwd` should end in `my-product`). Then run these **one at a time**:

**① Turn on the save system for this folder**
```bash
git init
```
This makes the folder a **repository**. It prints `Initialized empty Git repository…`.

**② Name your main line of work "main"**
```bash
git branch -M main
```
GitHub calls the main version of a project `main`. This just makes the name match.

**③ Check what Git sees**
```bash
git status
```
`git status` is your **minimap**: it shows what's changed and what's ready to save. You should see `README.md` listed in red under "Untracked files."

**④ Choose what goes into this save**
```bash
git add .
```
The `.` means "everything in this folder." Run `git status` again: `README.md` should now be **green**, meaning "ready to be saved."

**⑤ Make the save point, with a label**
```bash
git commit -m "Add Product 1 spec"
```
`-m` means "here's my message." You just made your first commit. 🎉

---

## 9. Put it on GitHub (push)

This one command creates the repo on GitHub **and** uploads your save:

```bash
gh repo create my-product --public --source=. --remote=origin --push
```

What each part means:
- `gh repo create my-product`: make a new repo on GitHub with this name (**use your project's name**)
- `--public`: anyone can view it. This builds your portfolio.
- `--source=.`: use the folder I'm in right now
- `--remote=origin`: nickname the GitHub copy `origin` (the standard name)
- `--push`: upload my commits now

**See it online:**
```bash
gh repo view --web
```
Your browser opens your repo, and your spec shows up on the front page. **That's today's goal. You're done with the required part!** ✅

> 🔒 **Public means public.** Anyone can read your spec. Only include personal details you're comfortable sharing. Never put passwords, API keys, or other people's private info in a repo. If you'd rather keep it private, use `--private` instead of `--public`, and ask your instructor how to share access for grading.

<details>
<summary><strong>Another way:</strong> create the repo on the GitHub website instead</summary>

1. On GitHub, click **+** (top right) → **New repository**.
2. Enter your project name. **Leave "Add a README file" unchecked**, because you already have one. Click **Create repository**.
3. GitHub shows you a page of commands. In your terminal, run the ones under "…or push an existing repository from the command line". They look like this (with **your** link):

   ```bash
   git remote add origin https://github.com/your-username/my-product.git
   git branch -M main
   git push -u origin main
   ```
   - `git remote add origin …`: connect this folder to that GitHub repo
   - `git push -u origin main`: upload your `main` saves to `origin`. The `-u` makes Git remember this, so next time you can just type `git push`.
</details>

---

## 10. The everyday loop

From now on, every time you change your project, you'll use the same four commands:

```bash
git status                          # 🗺️  What changed?
git add .                           # 🎒 Pick what goes in this save
git commit -m "Describe the change" # 💾 Make the save point
git push                            # ☁️  Upload it to GitHub
```

**Try it now:** make a small edit to your README (fix a typo, or fill in something you skipped), save the file, then run the four commands with a message like `"Update problem statement"`. Refresh your repo page to see the change.

### Good habits (start them now)
- **Save often, in small pieces.** Commit each time you finish one thing. Lots of small save points are easier to go back to than one giant one.
- **Write labels your future self will understand.** `"Add MVP features table"` beats `"stuff"` or `"asdf"`. Start with a verb: *Add, Fix, Update, Remove.*
- **Push at the end of every work session.** If it's not on GitHub, it's not safe, and your instructor can't see it.
- **Check the minimap.** Run `git status` whenever you're unsure what's going on.
- **Never commit secrets.** Passwords and API keys never go in a repo, not even a private one.

---

## 11. Your first pull request *(stretch)*

On real teams, nobody changes `main` directly. You do your work on a **branch** (a side quest), then open a **pull request** so someone can review it before it joins the main story. AI agents work the same way: they make a branch and open a PR, and **you** review it. Practicing this now will pay off.

**① Start a side quest (make a branch and switch to it)**
```bash
git switch -c improve-spec
```

**② Make a change.** Edit your README, for example to tighten your "solved when" line, then save.

**③ Save and upload the branch**
```bash
git add .
git commit -m "Tighten solved-when line"
git push -u origin improve-spec
```

**④ Open the pull request**
```bash
gh pr create --fill
```
`--fill` uses your commit message as the PR title. It prints a link. Open it in your browser.

**⑤ Review it like a teammate would.** On the PR page, click **Files changed** to see exactly what's different (green lines were added, red lines were removed). Ask a classmate to look too, and leave a comment.

**⑥ Merge it into main.** Click **Merge pull request → Confirm merge** on GitHub.

**⑦ Come back to main and download the merged version**
```bash
git switch main
git pull
```

You just did the full professional workflow: **branch → commit → push → PR → review → merge**.

---

## 12. Connect an AI agent to your repo *(stretch / at home)*

Once your repo is on GitHub, you can connect an AI agent to it. Treat the agent like a **new teammate you just gave a key to**:
- Give it a key to **one room**, not the whole building: when GitHub asks which repositories to allow, choose **"Only select repositories"** and pick your Product 1 repo.
- Have it work on a **branch** and open a **pull request**. **You** review every change before it goes into `main`.
- **You're responsible for everything it writes.** Read it, test it, and be able to explain it. Keep AI work visible in your PRs and commit history (that's a course rule).
- Use it as a **tutor**, not just a doer (see the prompts below).

> ⏳ **These apps change fast.** The steps below are current as of fall 2026, but button names move around. If something doesn't match, ask the tool itself: *"How do I connect you to my GitHub repository?"*

### Option A: GitHub Copilot app (desktop) · good first pick for students
GitHub's own desktop app for working with AI agents on your repos.
- **Cost:** GitHub says it works with any Copilot plan, including **Copilot Free** and **Copilot Student**. Copilot Student is free for verified students through [GitHub Education](https://education.github.com) (see Step 1). If the app asks you to upgrade, check that your student benefits are active.
- **Get it:** download from **[github.com/github/app](https://github.com/github/app)** (Windows, Mac, Linux), install, and **sign in with your GitHub account**. Because it's GitHub's own app, your repos are already connected.
- **Add your project:** add your Product 1 repo, either as the **local folder** you made in Step 7 or by picking it from **your GitHub repositories**.
- **How it works:** each session runs in its own copy of your project on its own branch (a Git **worktree**, like a separate save slot). You **review the changes**, then open a **pull request** into `main`.

### Option B: Claude desktop app (Code tab)
- **Cost:** the **Chat** tab is free: you can paste in your README or a Git error and ask for help. The **Code** tab, which works directly on your project files, needs a **paid Claude plan (Pro or higher)**.
- **Get it:** download from **[claude.com/download](https://claude.com/download)**, sign in, and click the **Code** tab.
- **Open your project:** choose **Local**, click **Select folder**, and pick your `my-product` folder.
- **Stay in control:** set the **permission mode** (next to the send button) to **Manual**, so Claude asks before every file edit or command. Or use **Plan**, so it proposes a plan before changing anything.
- **Review:** after Claude edits files, click the `+12 -1`-style indicator to see a **diff** (what changed, line by line) before you commit.
- **Pull requests:** Claude uses the **GitHub CLI** you installed in Step 4 to open PRs.
- **See your GitHub issues and PRs too:** click **+** next to the prompt box → **Connectors** → **GitHub**.

### Option C: ChatGPT
- **To explain your code (read-only):** connect GitHub in ChatGPT's **Settings** (look for **Apps**, **Connectors**, or **Plugins** → **GitHub**). GitHub will ask you to approve the ChatGPT app and choose which repos it can see. ChatGPT can then **read** your repo to answer questions, but **it can't change anything**.
- **To make changes and open PRs:** use **Codex** (inside the ChatGPT desktop app, or at [chatgpt.com/codex](https://chatgpt.com/codex)). Connect GitHub when it asks, pick your Product 1 repo, describe a task, and Codex hands back a **pull request** for you to review.
- **Cost:** access on the free plan is limited and changes often. Check what your plan includes.

### 🤖 Prompts to learn *with* your agent (works in any of them)

**Be my Git tutor:**
```text
I'm brand new to Git and GitHub. Act as my tutor. Before you run any Git
command, explain in one or two plain sentences what it does and why, then
ask me to type it myself. Don't run Git commands for me unless I say
"you do it."
```

**Explain what I'm seeing:**
```text
I ran `git status` and got this output: [paste it]. Explain what each part
means in plain language, and tell me what I should probably do next.
```

**Help me fix an error (without just fixing it):**
```text
I got this error: [paste the full error]. I was trying to [what you were
doing]. Explain what went wrong in simple terms, then walk me through fixing
it step by step so I understand it next time.
```

**Review my spec as a pull request:**
```text
Read the README.md in my Product 1 repo. It's my product spec. Don't edit it.
Leave review comments like a teammate would: what's clear, what's vague, and
the top 3 questions I should answer before I start building.
```

**Make a change the right way:**
```text
Create a new branch, make this change: [describe it], then open a pull
request into main. Don't merge it. I'll review it first. Explain every
command you run.
```

---

## Troubleshooting

| You see… | What it means | Try this |
|---|---|---|
| `git: command not found` | Git isn't installed, or your terminal can't find it | Install Git (Step 2). Close and reopen your terminal. On Windows, use **Git Bash**. |
| `gh: command not found` | The GitHub CLI isn't installed, or the terminal was open during install | Install it (Step 4), then **close and reopen** your terminal. |
| Weird errors in **PowerShell** on Windows | PowerShell handles some Git commands differently | Use **Git Bash** instead. |
| `fatal: not a git repository` | You're in the wrong folder | Run `pwd` to check where you are. Then `cd ~/Documents/my-product`. |
| `Author identity unknown` | Git doesn't know your name yet | Do Step 6. |
| `error: src refspec main does not match any` | You haven't made a commit yet, so there's nothing to upload | Run `git add .` and `git commit -m "Add Product 1 spec"`, then push again. |
| `nothing to commit, working tree clean` | Everything is already saved | That's fine! Did you save your file in the editor first? |
| `remote origin already exists` | This folder is already connected to a GitHub repo | Run `git remote -v` to see where it points. |
| `Repository not found` / `Permission denied` / `403` | Your computer isn't logged in to the right GitHub account | Run `gh auth status`. If needed, run `gh auth login` again, then `gh auth setup-git`. |
| `Name already exists on this account` | You already have a repo with that name | Pick a different name in the `gh repo create` command. |
| A strange full-screen text editor opened after `git commit` | You forgot `-m "message"`, so Git opened an editor (usually **Vim**) | Type `:q!` and press **Enter** to quit without saving, then run the commit again with `-m "your message"`. |
| Your README shows as plain text or doesn't appear on GitHub | The file is named wrong (e.g. `README.md.txt` or `readme.txt`) | Rename it to exactly `README.md`, then add, commit, and push. |

---

## Watch the walkthroughs

These recordings from a previous semester walk through the same setup (installing Git and `gh`, `gh auth login`, and the first push):
- [Git & GitHub setup: install Git, GitHub CLI, `gh auth login`, first push](https://app.read.ai/analytics/meetings/01KGNKK64CMAWGYXZRPFWATBFS?utm_source=Share_CopyLink)
- [Git & GitHub setup, part 2: live walkthrough, with extra Windows (Git Bash) tips](https://app.read.ai/analytics/meetings/01KH2FJH16W5BZQ2Y36S1CV89Y?utm_source=Share_CopyLink)
- [What Git, GitHub, and pull requests are (Sep 2)](https://app.read.ai/analytics/meetings/01M1J2KR2VXMS9S66WY5WNJX8R?utm_source=Share_CopyLink)

---

## ✅ Done looks like

- [ ] I have a GitHub account *(and applied for GitHub Education)*
- [ ] `git --version` and `gh --version` both work
- [ ] `gh auth status` says I'm logged in
- [ ] My Product 1 folder has a `README.md` with my spec
- [ ] I made my first commit
- [ ] My repo is on GitHub and my spec shows on the front page
- [ ] I pushed at least one more change using the everyday loop
- [ ] *(Stretch)* I opened and merged my first pull request
- [ ] *(Stretch)* I connected an AI agent to my repo and had it review my spec
- [ ] I posted my repo link in Slack
