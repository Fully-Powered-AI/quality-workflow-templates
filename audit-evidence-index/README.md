# Audit evidence index

The quality lead gets an index of everything an audit has asked to see: each request linked to the document that answers it, its version and owner, the records found and the gaps. The quality owner decides what is shared; nothing is certified or sent.

*Workflow template · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/audit-evidence-index/)*

## The outcome

An audit request list is easy to receive and slow to answer. Each line has to be traced to a document, the right revision found, the records behind it located, and someone chased when a piece is missing. This workflow template does that tracing in one pass, before the audit, so the gaps surface while there is still time to close them.

You receive an index with one entry per request. Each entry says which document answers it, which revision the register holds and whether that revision is in force, who owns the document, which records were supplied and where they are kept, and which earlier findings touch the same ground. Every request ends up in one of four states: linked, check first, possible match only, or nothing found. A line at the top proves the four counts add up to the number of requests.

The index uses only what you supply. It does not open documents, judge what a file contains, or say that anything is ready. A file title is not evidence of what is inside it, and the auditors decide for themselves what the evidence shows.

## Who starts the work, and when

The quality lead or the office lead starts it once the audit request list arrives, whether the audit is internal or from a customer. It can be run again as requests are added or records are found. The quality owner reviews the index, asks each document owner to fill their gaps by the hand-off date, and decides what is shared with the auditors and when.

## What they supply

- **The request list,** as the auditors sent it, with a request number and the wording of each request.
- **The document register:** each controlled document with its number, title, revision, status, effective date, owner and next review date.
- **The records selected for the audit:** what each is, which document it belongs to, the revision it was made under, its date and where it is kept.
- **Last cycle's findings,** with their status and the action recorded against each.
- **The audit date and your lead time,** so the index can set the date by which owners respond.

If the columns of an export are named differently from those the template expects, the assistant stops and asks which is which.

## What comes out

One index in a fixed order. It opens with the count of requests and records and the line that proves the counts. Then comes one entry for every request: its state, the document with revision, status and owner, the records found with their dates and locations, the earlier findings that touch it, and what has to be settled and by whom. After the entries come the records and findings that link to no request, and a short list of decisions for the quality owner. A closing line says what the index cannot show.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/), where an audit request list lands on the quality owner and has to be answered from many people's files.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where an audit can ask for inspection, calibration and supplier records held in different places.
- [Life sciences](https://fullypowered.ai/industries/life-sciences/), where the revision a record was made under matters as much as the record itself.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where customers audit project records and procedures held by different teams.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where records have built up across years and owners have changed.

## What has to change for your company

Fix the four files and their column names once, so every audit starts from the same exports. Decide your lead time, which sets the hand-off date. Decide which register status means a document is in force; the template assumes "Effective". Say whether a blank owner means vacant or simply not recorded. Agree who answers for a document with no owner. Choose how the index reaches the auditors, because the template only prepares it. Separate this index from broader preparation: [Audit preparation](https://fullypowered.ai/workflows/audit-preparation/) covers a finance audit, and [Shared folder filing plan](https://fullypowered.ai/workflows/shared-folder-filing-plan/) tidies where files live.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026, in two runs: an independent review changed the instruction block, the output format and the example after the first, and the record of the second is published with it. It has not yet been tested in a client environment, or tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past audit you know well, with cases written in advance: a request that names a document the register lacks, a record made under a superseded revision, a document with no owner, a request that only half-matches. The quality owner checks every link against the actual files before anyone relies on the index. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Obsolete copy check](../obsolete-copy-check/)
- [Audit preparation](https://fullypowered.ai/workflows/audit-preparation/)
- [Shared folder filing plan](https://fullypowered.ai/workflows/shared-folder-filing-plan/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
