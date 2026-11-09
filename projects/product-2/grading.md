# How Product 2 Is Graded

> **Check-in: Mon Nov 23** · **Due and presented: Mon Nov 30** (in class)
> Same idea as [Product 1](../product-1/grading.md): we're **not** grading how finished it is. We're grading how well you **listened**, whether you built something **real that helps**, and whether you **understand** what you built.

---

## The four parts (25% each)

| Part | Weight | In one sentence |
|---|---|---|
| **1. Discovery** | 25% | You talked to a real partner, mapped how their work happens, and found a real problem. |
| **2. Spec and solution brief** | 25% | Your README is a complete spec about your partner, with a plain-language brief they could read. |
| **3. Repo and demo evidence** | 25% | Your repo has working code for your MVP, plus proof that it runs. |
| **4. Presentation, code review and partner feedback** | 25% | You tell the story, demo it, explain your code, and share what your partner said. |

Think of it like being a **contractor fixing someone's kitchen**. **Discovery** is visiting the house and hearing how they cook. The **spec and brief** are the plan you show the homeowner. The **repo** is the work itself, with before-and-after photos. The **presentation** is the walkthrough with the homeowner's review.

---

## Part 1: Discovery (25%)

In the **Discovery Log** section of your README:
- [ ] **At least 2 conversations** with your partner, with **at least 1 in person**
- [ ] Notes for each one: goals, how the work happens, pain points **with numbers** (how often, what it costs), tools they use now, and what they wish existed
- [ ] A **workflow map** of how the work happens *today*, with the pain points marked
- [ ] **Existing vs desired solutions**: what they use now, what they want, and the gap
- [ ] **Partner privacy respected**: no customer names or contact info, no revenue or prices, and the business is nicknamed if they asked

*The feedback conversation (Part 4) can count as your second conversation.*

---

## Part 2: Spec and solution brief (25%)

Your repo's **`README.md`**, using the [Product 2 Spec Template](./SPEC_TEMPLATE.md):
- [ ] **About the partner**
- [ ] **Problem statement** written about your **partner** (not you), using facts from discovery, plus a "they'll know this is solved when…" line
- [ ] **Features and benefits**, with the **MVP** marked, plus "Later" and "Not doing" lists
- [ ] **Tech stack and architecture**: surface, stack, a reason for each, and a diagram. Automations show **trigger → logic → action**.
- [ ] **Solution brief**: a plain-language page you could hand your partner
- [ ] Kept **up to date** with what you actually built

---

## Part 3: Repo and demo evidence (25%)

- [ ] On **GitHub**, with the link submitted
- [ ] **Working code for at least one MVP feature** that addresses your partner's problem
- [ ] **Code you wrote and can explain.** For automations, no-code tools are fine for the plumbing, but your repo must include **your own code** (scripts, API routes, an app or interface).
- [ ] **Commit history** over time. **Pairs: both teammates' commits**, ideally through branches and pull requests.
- [ ] **No secrets** (API keys, passwords, the partner's login details) in the repo
- [ ] A **Demo** section in your README. As with Product 1: screenshots are 👍, a GIF or video is 👏, a live link is 🏆. For automations, **record the whole flow** from trigger to result.

---

## Part 4: Presentation, code review and partner feedback (25%)

**Live in class on Mon Nov 30.** Plan for about **6 minutes** (about **8 minutes for pairs**), plus questions. **In pairs, both of you present.**

### What to cover
1. **Who and why (about 1 min):** your partner, how you found them, and the problem in their words
2. **Discovery story (about 1 min):** what you learned, your workflow map, and the "aha" moment
3. **Solution and architecture (about 1 min):** what you built, why that type of solution (app, automation or both), and your diagram
4. **Demo (about 1–2 min):** live, a link, or a video
5. **Code walkthrough (about 1 min):** one or two files you wrote. **Pairs: each person explains code they wrote.**
6. **Partner feedback (about 30 sec):** what they said (with quotes) and what you'd build next

### Partner feedback (required)
In your README's **Partner Feedback** section:
- [ ] Date and format of the feedback conversation
- [ ] **At least 2 direct quotes**
- [ ] What worked, what didn't, and what they'd want next
- [ ] *(Strong evidence)* a short note from your partner, or an audio or video clip, **with their permission**

### Questions you might be asked
**Discovery:** How did you find your partner? What surprised you? How do you know this is *their* problem and not one you assumed?
**Solution:** Why an app, an automation, or both? What did you leave out?
**Architecture:** What triggers it? Where does the data live? What happens if something fails?
**Code:** What does this file do? Where would you add *[a feature]*? What was the hardest bug?
**AI and process:** What did you have to research? Which AI tools did you use, and where were they wrong?
**Partner:** What did they say? Would they actually use it? What would make them use it every day?

> 🤖 **AI is allowed and expected. You're responsible for every line.** Rehearse with the mock code review prompts in [Learn with Agents](../../modules/learn-with-agents.md#step-6-prep-for-your-code-review).

---

## What a strong Product 2 looks like

| | Needs work | Meets expectations | Strong |
|---|---|---|---|
| **Discovery** | Fewer than 2 conversations, or vague notes. The problem seems assumed. | 2 conversations (1 in person), clear notes with numbers, and a workflow map. | Rich notes and quotes, a detailed workflow map, and the problem clearly comes from the partner's own words and observed work. |
| **Spec and brief** | Missing sections. The problem statement is about the student or describes a solution. | Complete spec about the partner, a clear MVP, a stack with reasons, and a readable brief. | The brief is something the partner would actually understand and agree with. Scope is sharp and matches what was built. |
| **Repo and demo** | Little code, or code unrelated to the problem. No evidence it runs. | Working MVP feature, steady commits (both teammates), screenshots. | A working flow that solves a real piece of the problem, with a video or live link and a clean repo. |
| **Presentation and feedback** | Can't explain the code or the problem. No partner feedback. | Clear story and demo, explains the code and architecture, includes partner quotes. | Confident, specific and honest about trade-offs. The partner feedback shows real use, and there's a clear next step. |

---

## Timeline and how to submit

| Date | What's due |
|---|---|
| **Wed Nov 11** | Partner confirmed. Conversation #1 scheduled. Posted in Slack. |
| **Fri Nov 13** | Conversation #1 done, and notes in your repo |
| **Wed Nov 18** | Workflow map, problem statement, solution brief and stack in your README |
| **Mon Nov 23** | **Check-in:** show your progress and your plan for the feedback conversation |
| **Sun Nov 29** | Partner feedback conversation done and written up |
| **Mon Nov 30** | **Due + presentations.** Submit your repo link before class. |

**Private repo?** Add your instructor (and your teammate) under **Settings → Collaborators**.

### Final checklist
- [ ] README follows the Product 2 Spec Template (all sections, including the Discovery Log and Solution Brief)
- [ ] 2+ conversations (1+ in person), plus a workflow map
- [ ] Working MVP code you wrote, pushed to GitHub, with no secrets
- [ ] Demo section (screenshots, video or link)
- [ ] Partner Feedback section with 2+ quotes
- [ ] Team section (pairs)
- [ ] Practiced the presentation and the questions above
- [ ] Repo link submitted
