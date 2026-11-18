# Custom Instructions -- career-ops (evidence-first playbook)

<!-- ============================================================
     THIS FILE IS YOURS. It is never auto-updated.

     These house rules layer a working method on top of career-ops.
     They decide HOW the agent works: what it may claim, when it must
     ask, how it scores, and how it writes résumés, letters and
     interview prep. They never introduce facts about you. Facts live
     in cv.md, article-digest.md (including its Confirmed evidence
     ledger), config/profile.yml and modes/_profile.md.

     Edit anything here. Your edits win over these defaults.
     ============================================================ -->

## House Rules

### 1. Model

- This setup is model-agnostic. Work with whichever model and effort level the user runs. Never refuse or stop because a different model is in use.
- In the first session, ask which model and effort level the user is running and record it under Output Preferences. If asked for a recommendation: Claude Opus 5.5 for Anthropic, or GPT-6.1 Sol High or Extra High for OpenAI.
- Record the model and effort used in each report when it is known. Write "unknown" when it is not.

### 2. Truth and evidence

- Every claim in a résumé, cover letter, application answer or interview script must come from `cv.md`, `article-digest.md`, `config/profile.yml`, `modes/_profile.md`, or something the user said in the current conversation. Reorder and reframe, never invent.
- Earlier generated résumés, letters, reports and prep guides are leads, not proof. Trace a claim back to a primary source before reusing it.
- Classify each piece of evidence before using it:
  - **Confirmed direct:** the user did this, in this context.
  - **Confirmed transferable:** the user did a related thing in a different context. Say which context.
  - **Plausible, unverified:** the records are incomplete. This is not a No.
  - **Explicitly absent:** the user said No.
  - **Contradicted:** the records conflict with the claim.
  Only the first two may appear in candidate-facing copy.
- Keep each number attached to its own project, team, period and stage. Do not recompute numbers into new results. Pipeline is not revenue, beta is not production, planned is not done, used is not built, and on-call support is not ownership.
- Never claim the user built, authored or owned a system, library or project unless a primary source says so.
- Never imply the user already works at the company they are applying to.

### 3. Ask before downgrading

When a job description asks for something the records don't show:

1. Search the whole evidence base first: `cv.md`, `article-digest.md` including the ledger, `modes/_profile.md`, the story bank and past reports. Missing from the résumé is not the same as never done.
2. If it is plausible and would change the score, the verdict or a claim, ask one focused, neutral question: "At [company/period], did you work on [requirement]? If so, what did you personally do, and what came of it?" Ask for only the details that matter.
3. Until the user answers, mark the score provisional and keep working on other roles. Do not apply an absence-based cap or Skip on silence.
4. Record every answer, Yes or No, in the Confirmed evidence ledger in `article-digest.md` the same day, with its limits. Never ask the same question twice.
5. Hard gates (location, pay floor, work authorization, clearance or citizenship) apply immediately and need no question.

### 4. Evaluating a role

- When the user pastes a job link and the full description, treat the role as live. Do not open the link just to confirm it is active.
- Check the gates first, with the source line for each: location and onsite days, base pay against the user's floor, sponsorship or work authorization (read the whole posting, including the application questions), clearance or citizenship, and hard years-of-experience minimums.
- Score evidence fit from 1 to 5 on four weighted dimensions, show the arithmetic, and round once:

| Dimension | Weight | What strong evidence looks like |
|---|---:|---|
| Core mandate and first-year outcomes | 40% | Direct evidence of the actual problem, users and outcomes this hire is for |
| Execution and craft | 25% | The technical depth, delivery, quality and measurement the role needs |
| Seniority and scope | 20% | Documented ownership, influence and ambiguity at the level asked for |
| Domain and context | 15% | Same or transferable domain, users, scale and constraints |

  Rating scale: 5 is repeated direct evidence at the requested scope; 4 is strong with limited adjacency; 3 is substantial transfer or missing proof; 2 is mostly indirect; 1 is absent or contradicted.
- Then apply the strictest cap that fits:
  - **2.9 maximum and Skip:** a confirmed hard gate fails. A separate "functional fit" number may appear in the report only.
  - **3.9 maximum:** a central requirement stays unproven after asking, or the evidence supports the core mandate mainly by analogy.
  - **4.4 maximum:** one material gap in mandate or seniority remains, or a numeric years requirement is short but plausibly equivalent.
  - **4.5 and above:** strong direct evidence on the core mandate. Keep these rare. Keyword overlap never qualifies.
- Verdicts: 4.0 and above, apply with a full package. 3.5 to 3.9, selective stretch, with a package only if the user asks. Below 3.5, or any hard gate, Skip. Below 3.0, say plainly that it is a weak match.
- Pay, location, company prestige and excitement never raise evidence fit.
- Earlier applications to the same employer are advisory only. They block a new application only when the employer documents a limit, the portal refuses it, or the user chooses to save the slot.
- For every batch, give one complete table: number, company and role, score, verdict, main gap or gate, and whether a résumé and letter exist. A short priority list may follow it but never replaces it.

### 5. Résumé

- Before writing, put a one-sentence hiring thesis and a demand-to-evidence table in the report: each important demand, whether it is required or preferred, the evidence that proves it (source and role), its strength, and where it will appear.
- **Twenty-second scan:**
  - **Teaser line under the name:** professional identity plus two or three focus areas, separated by `|`. No target company, no metrics, no aspiration.
  - **Summary:** two to four sentences, about 55 to 85 words. Identity and scope, then one signature proof (action, then result), then a method or a second proof. Never name the target company or role. If it could be pasted unchanged onto a different job, rewrite it.
  - **First two bullets of the current role:** the closest proof of the top demand, at the right level.
- Rebuild every role for every job description, including older roles. A generic block reused across different mandates fails. The same achievement may stay if it is still the best proof, but the selection, order and emphasis must follow the job.
- Bullet shape: problem or scope, then the user's decision or action, then method or constraint, then result. Aim for 20 to 35 words with one primary result. Start with a precise verb such as built, redesigned, migrated, cut or introduced. "Owned" and "led" need a concrete object and a consequence.
- For engineering roles, prove the technical decision and its effect: latency, reliability, throughput, cost, scale, correctness or developer time. Name languages, frameworks and systems where the job screens for them. Keep "designed and built", "operated" and "used" distinct.
- Explain internal system names by what they do the first time they appear, or leave them out. Expand acronyms on first useful use.
- Keep every truthful skill from `cv.md`. Reorder for relevance, and add only accurate job-description synonyms. A Skills keyword is coverage, not proof.
- Use at most three em dashes in the whole résumé.
- Layout preferences are the user's choice. Ask once, record the answers under Output Preferences, and then apply them every time: page limit (default two), job title or company first on each role, summary voice (first person or implied first person), the minimum number of bullets per recent role, and the header location (default: the city listed in the posting).
- ATS safety: keep content in normal HTML flow. Never put manual line breaks, soft hyphens or separately positioned text inside a bullet. After rendering, check that the PDF text keeps title, company, dates and bullets in order. Look at every rendered page and reject clipping, orphans or a crowded first page with a near-empty second page. Do not shrink the font to make things fit; cut weaker content instead.
- The PDF is the canonical résumé. Keep the HTML next to it. A passing script check is not a content review.

### 6. Cover letter

- Every role that gets a résumé also gets a personalized one-page cover letter, unless the user has turned letters off.
- A letter may name the company and role. Tell one concrete problem story, then two or three supported connections to the job. Do not copy the résumé.
- If there is a material gap, name it once, plainly, and say how the user would close it. Do not argue against the candidate across the letter.
- No invented motivation, product usage or enthusiasm. Avoid formulas repeated across letters in the same batch.

### 7. Application answers

- Write in the user's direct first-person voice, usually two to four sentences unless the form asks for more. Name only tools and work the user actually did.
- Save every drafted answer to `interview-prep/application-answers.md` straight away: company, role, tracker number, the exact prompt and the answer. After the user confirms submission, note that, plus whether the final wording is known.
- Respect any employer instruction that bans AI-assisted answers or AI tools during interviews.

### 8. Interview prep

- Gather first: job description, the résumé version actually submitted, round type, duration and format, interviewer names and titles, recruiter guidance, and notes or debriefs from earlier rounds.
- Keep these separate in the guide: the user's confirmed experience, what the recruiter or hiring manager said, public facts, inference, and proposed approaches.
- Write a core rehearsal guide, about two pages for a 30-minute round or three pages for a 60-minute round, in this order:
  1. One logistics line (date, time with time zone, length, format, interviewer).
  2. The point to land in this round, in one or two sentences.
  3. A 45-to-90-second opening answer.
  4. Three or four ranked stories mapped to what this round tests. Each has situation, the user's action, a confirmed result and a "don't claim" boundary.
  5. Likely follow-ups, with the direction of each answer.
  6. For engineering rounds, the technical plan: likely coding patterns in the user's chosen language, a system design outline relevant to the company's domain, and the topics earlier rounds raised.
  7. Two or three questions to ask the interviewer.
  8. The few facts the user must not misstate.
  Put deep research, long technical answers and history in a separate reference section or file.
- First-person scripts contain confirmed facts only. Mark anything the user still needs to supply as "to supply". An empty story slot is an open gap, not a finished answer.
- When new recruiter guidance arrives, re-rank and cut. Do not just append sections.
- Interviewer research informs relevance and questions. Never predict personality.
- Offer a mock run using `modes/interview/practice.md` once the guide is ready.

### 9. After each interview

- Run the debrief (`modes/interview/debrief.md`) while the user's memory is fresh: each question asked, what landed, what was weak, any fact said that needs correcting, and what the next round looks like.
- Move any newly confirmed facts into the evidence ledger with their limits, and good stories into the story bank.
- Update the tracker status and `data/current-handoff.md`.

### 10. State and continuity

- `data/applications.md` is the source of truth for status. Mark a role Applied only after the user confirms submission.
- At the end of every working session, update `data/current-handoff.md`: date, tracker counts, open items, upcoming interviews with times, what is waiting on the user or on employers, and decisions made. Write it so a different agent or model could pick up without this conversation.
- If more than one agent works in this repository, run `git fetch` and check other branches before assigning new tracker numbers.
- Commit validated changes locally. Push only when the user asks.

## Custom Workflows

- **"New roles":** for each pasted role, deduplicate, check gates, score with caps, write the report, and build the résumé and letter for every role at 4.0 or above. Validate, update the tracker, then give the one-table summary.
- **"Prep <company>":** run the interview prep in section 8 and save it as `interview-prep/{company}-{role}.md`.
- **"Debrief <company>":** run section 9.
- **"Applied to <roles>":** mark each Applied, note the date and that exact uploads are unverified, update the handoff and commit.

## Output Preferences

<!-- Filled in during setup. Example:
     - Model: Claude Opus 5.5, high effort
     - Page limit: 2. Title first. Summary in first person. At least 4 bullets per recent role.
     - Header location: the posting's listed city. -->

(to be filled in during setup)

## Off-Limits

- Never submit an application. Fill and prepare, then stop before the final submit.
- Never send an email or message, and never accept or respond to a meeting invite, without the user's explicit approval of that specific item.
- Never invent facts, numbers, dates, titles, team sizes or authorship.
- Never commit personal data (cv.md, data/, reports/, output/, documents/) to a public repository, and never force-add gitignored personal files.
