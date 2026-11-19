# AI workflow templates for quality management

FullyPowered Workflow Templates for quality management teams turn the AI your company already pays for into a team that knows how the work is done: a quality lead with the audit evidence indexed to each request, an operations lead with the cost of poor quality worksheet prepared, a purchasing person with the supplier's reply checked against the defect. 6 workflow templates, made to be customized and deployed. All plain Markdown, all free, MIT license.

We are FullyPowered AI. We build AI workflows for companies, and these are the templates we start from. We publish them because a good starting point should be open to everyone. Copy one. Change it. Make it yours.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** These are templates, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See more examples for quality management teams](https://fullypowered.ai/functions/quality-management/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme) · [Have one built for your team](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme) Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Who this is for**

- Owners and CEOs who want quality work that is documented, current and ready when an audit asks.
- Quality leads who want audits, reviews and corrective actions prepared the same careful way every time.
- The person who owns a process, who gets a clear draft to work from and decides.

**What these are for**

- **Your best way of doing it, for the whole team.** One piece of work, written down precisely enough that an assistant prepares it the same way every time.
- **Work you can check.** Every template says what it needs, what it produces, what it checked and what it could not.
- **A person decides.** Anything that sends, posts, pays or changes a record waits for someone to approve it.
- **Tied into your business systems.** A workflow can be designed to pull from the systems your company already runs, and even push data back into them, with guardrails and a person approving. [Browse the Connectors Directory](https://fullypowered.ai/connectors/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme).
- **Free, open and portable.** MIT-licensed plain instructions that run in the assistant or agent your team already uses: ChatGPT, Claude, Claude Code, Claude Cowork, Codex, Copilot, Gemini, Grok, Perplexity.

**Quick start**

1. **Draft a record for a problem you just spotted.** Open ChatGPT, Claude, Copilot or Gemini. Copy the text below into a new chat. Replace the square brackets with your own notes and the exact wording of the requirement. Read the draft, then decide what to do with it.

   ```text
   You prepare the draft record of one possible nonconformity for a quality lead. Use only what I give you. Never classify anything, accept or reject work, hold or release anything, contact anyone, or change a record. A person decides; you prepare and check. Never guess a requirement. If my notes or the requirement are missing, stop and ask. Give me: what was observed, numbered, with guesses labelled as guesses; the requirement quoted exactly with document, revision and clause; each reading compared with the limit and the amount it differs by, worded as "differs from the requirement as written"; evidence not supplied; decisions for the quality owner; and what to confirm before relying on the draft. Propose no cause and no fix. My observation notes: [paste notes]. The requirement, exact words: [paste wording, document, revision, clause].
   ```

2. Read what comes back. It marks what it checked and what is left for you. What comes back, with invented data:

   ```text
   NONCONFORMITY RECORD (DRAFT): Bracket B-220, lot L-3314, flange height
   Status: Draft for the quality lead. Suspected, not confirmed. Nothing classified, held, released, sent or recorded.
   Record number: To be assigned by the quality lead.
   Observed: 2026-11-10, about 07:45, by the early-shift supervisor, at press area rack 4. Prepared 2026-11-10 for the quality lead. Inputs read: the supervisor's notes; DWG-B220 revision C; the work register (seven rows; as-of date not given); the evidence list (three rows); the nonconformity log (two records).
   Safety flag: None stated in the notes. This draft is not a safety assessment.

   WHAT WAS OBSERVED
   O1. Five parts picked at random from the 120 on rack 4 (lot L-3314, Bracket B-220, made on PB-4 on 2026-11-09), measured for flange height with caliper CAL-07, whose sticker shows calibration due 2026-11-30.
   O2. Readings in mm: 41.2, 41.3, 41.1, 41.4 and 42.0. Five parts examined of 120.
   O3. The drawing at the press is revision C. The supervisor has not checked the document register.
   O4. The supervisor took photos and wrote the readings on a sheet.
   O5. The rest of the lot has not been touched and is still on rack 4. Nobody has been told except the quality lead.
   O6. The supervisor's belief, not an observation: the tool setting may have drifted. The supervisor has not looked.
   ```

3. Stop there. You will know if this is for you. When you want it fitted to your company, or built into your agents, [that is what we do](https://fullypowered.ai/pricing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme).

The quality owner decides what conforms, what is held and what is shared; the template prepares and checks, and nothing here certifies, sends or changes a record.

These are samples and a starting point, made to be changed to fit your procedures, your records and your wording. Your own quality work may look different, and a workflow can be a single step or many, so if the work you do is not listed here it can still be built.

## The quality workflow templates here today

- **[Audit evidence index](audit-evidence-index/)**: The quality lead gets an index of everything an audit has asked to see: each request linked to the document that answers it, its version and owner, the records found and the gaps. The quality owner decides what is shared; nothing is certified or sent.
- **[Cost of poor quality worksheet](cost-of-poor-quality-worksheet/)**: An owner or operations lead who senses that rework, scrap and returns are costly gets one worksheet: the failure costs already on record, sorted by category, with estimates, gaps and unresolved allocations listed. The owner decides what to fix first.
- **[Nonconformity record draft](nonconformity-record-draft/)**: A quality lead or supervisor who has spotted something wrong gets a draft record: the observation set against the stated requirement, the affected work counted from the register, and the containment options. The quality owner decides every call.
- **[Obsolete copy check](obsolete-copy-check/)**: The quality lead gets the master document list set against the copies found at each point of use: which copies are out of date, which withdrawn documents are still held, and what proof of withdrawal exists. The document owner withdraws and replaces copies; nothing is changed.
- **[Quality management review pack](quality-management-review-pack/)**: Before the periodic quality review, the quality lead gets one brief for senior leaders: where each measure stands, complaints and defects, audit findings, action status, and the decisions still open. The leaders decide; the brief claims no compliance with any standard.
- **[Supplier quality response check](supplier-quality-response-check/)**: A quality or purchasing person who has raised a defect with a supplier gets the supplier's reply set against the finding: what is answered, what is not, the evidence still to ask for, the actions proposed and what has yet to be verified. The person decides whether the answer is accepted.

## How to use one

Open a folder and start with its README. Every folder stands alone, so copy the one you want and leave the rest. The templates are written for ChatGPT, Claude, Copilot and Gemini: paste the instruction block and the output format in as custom instructions, or load the folder in a product that reads `SKILL.md` packages.

To take the whole collection, press **Use this template** at the top of this page: it copies every folder into a repository in your own account, yours to change.

In every template a person starts the work, supplies the inputs and decides. The template prepares and checks. Anything that sends, posts, pays or changes a record waits for a person to approve it.

## What SKILL.md is

Each folder holds a file named `SKILL.md`. It is the technical file: the same instructions and output format as the template, in the packaged form that AI products which load instructions from a folder read. It is generated from `TEMPLATE.md`, so the two always agree. The workflow template is the whole folder; `SKILL.md` is one way of loading it. If your AI product does not read that format, use `TEMPLATE.md`.

## What "checked" means here

Each folder says exactly what was checked and when: who wrote it, that its sources and rights were reviewed, the date of its editorial review, and whether it has been tried on its invented example in a named AI product. Nothing is described as tested for a client unless it was. Test a template on your own past work before your team relies on it; each one comes with acceptance tests for that.

## More workflow templates

The [FullyPowered Workflows Directory](https://fullypowered.ai/workflows/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme) lists every workflow template across functions and industries, with search. A machine-readable list of this repository is in [index.json](index.json).

For the work these templates come from, by team and by task, see [AI workflow examples for quality teams](https://fullypowered.ai/functions/quality-management/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme).

## Licence and credits

MIT, in [LICENSE](LICENSE) and in every folder. Each folder's SOURCES.md names what the workflow template drew on. Published by [FullyPowered AI](https://fullypowered.ai/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-readme&from=gh-quality-readme).
