# career-ops playbook

An evidence-first way of working with [career-ops](https://github.com/career-ops-hq/career-ops), the open-source job-search agent. career-ops does the mechanics: evaluating postings, generating résumés, tracking applications and preparing interviews. This playbook adds the working method on top: what the agent may claim, when it has to ask you instead of guessing, how it scores roles, and how it writes résumés, cover letters and interview prep.

It contains no one's personal data. You bring your own résumé and history.

## Start here

Open your coding agent (Claude Code, Codex or similar) in the folder where you want the project, and paste this:

```text
Set up my job-search agent, then work with me on it from day one onward.

1. Clone the playbook and read its setup prompt completely before doing anything else:
   git clone https://github.com/satishk92/career-ops-playbook.git
   Then read career-ops-playbook/SETUP-PROMPT.md from start to finish and follow it phase by phase, running every step yourself. It installs career-ops (the open-source job-search agent), adds the playbook's house rules, and sets out how we'll work every day.
2. Start with its two Phase 0 questions: which model and effort level I'm running, and when my next interview is. If the interview is within 72 hours, do the interview fast path right after the install and save the full setup for afterwards.
3. These rules apply from the first message: never submit an application; never send an email or message, or respond to a meeting invite, without my explicit approval of that specific item; never invent facts (ask me one question at a time and record my answers); keep my personal data out of git and out of any public repository; commit locally and push only when I ask; and work with whatever model I'm running.
4. When setup is done, tell me what's installed, what's in my handoff file, and what to send you next.
```

If your agent can't clone repositories, paste the whole of [SETUP-PROMPT.md](SETUP-PROMPT.md) instead. Either way, answer its questions as they come. With an interview in the next few days, it prepares you for that first and finishes the full setup afterwards.

## What's in the playbook

| File | Installed as | What it does |
|---|---|---|
| [playbook/_custom.md](playbook/_custom.md) | `modes/_custom.md` | House rules for every mode: evidence states, ask-before-downgrade, scoring caps, résumé and letter rules, interview prep format, debriefs, handoff |
| [playbook/evidence-ledger.md](playbook/evidence-ledger.md) | appended to `article-digest.md` | A running record of facts you've confirmed and things you've said No to, so the agent never invents and never asks twice |
| [playbook/current-handoff.md](playbook/current-handoff.md) | `data/current-handoff.md` | Live state, so a fresh agent or a different model can pick up where the last one stopped |
| [playbook/application-answers.md](playbook/application-answers.md) | `interview-prep/application-answers.md` | Every drafted application answer, saved as it's written |

All four land in career-ops's user layer, so career-ops updates never overwrite them.

## The core ideas

- **Evidence before prose.** Each claim is confirmed direct, confirmed transferable, unverified, explicitly absent or contradicted. Only the first two reach a résumé.
- **Ask, don't downgrade.** If something plausible is missing from your résumé, the agent asks one focused question before scoring you down, and records the answer.
- **Calibrated scores.** Evidence fit is weighted 40/25/20/15 across core mandate, craft, seniority and domain, then capped: a failed hard gate caps at 2.9 (Skip), an unproven central requirement at 3.9, one material gap at 4.4.
- **Every role rebuilt for every job.** No generic older-role blocks. Every viable role also gets a one-page cover letter.
- **Short interview guides.** About two pages per 30 minutes: an opening, ranked stories, follow-ups, technical prep and questions to ask, with scripts that contain confirmed facts only.
- **Model-agnostic.** It works with Claude, OpenAI models or anything else your agent runs.
- **You stay in control.** The agent never submits applications or sends messages.

## Licence

MIT. career-ops itself is MIT-licensed by Santiago Fernández de Valderrama; this playbook is a separate add-on and is not affiliated with that project.
