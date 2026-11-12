# Obsolete copy check

The quality lead gets the master document list set against the copies found at each point of use: which copies are out of date, which withdrawn documents are still held, and what proof of withdrawal exists. The document owner withdraws and replaces copies; nothing is changed.

*Workflow template · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/obsolete-copy-check/)*

## The outcome

When a procedure is revised, the old version does not disappear on its own. It stays pinned above a bench, saved on a shared tablet or filed in a binder, and the people using it have no way to know. This workflow template gives the quality lead a clear answer to one question: where is an instruction in use that should no longer be?

You receive a comparison of your master document list with the inventories of the places where copies are kept. Every copy found is sorted: current, out of date, a withdrawn document, a revision nobody recognises, a document the master list does not know, or not yet due to change. For each out-of-date copy you see the withdrawal evidence on file and whether it agrees with what was found. You also see the places nobody has inventoried, so the report never pretends to be a clean bill of health.

The workflow template changes no document and removes no copy. Document control confirms what is obsolete, and the document owner withdraws and replaces copies through your agreed process.

## Who starts the work, and when

The document controller or the quality lead starts it when the agreed document-control review is due, after a batch of revisions has been released, or before an audit. Area owners supply the inventories for their own places. Document control reviews the comparison and decides what happens to each finding.

## What they supply

- **The master document list:** one row per document, with its current revision, effective date, status and owner.
- **The revision history,** so a superseded revision can be told from one that is simply unrecognised.
- **The distribution list:** where each document should be held and how many copies.
- **The point-of-use inventories:** what was found at each location, which revision, how many, in what form, and when it was checked.
- **The withdrawal records:** where and when a superseded revision was taken out, and the reference to the evidence.
- **The settings:** the organization or site name, the review date, the document control role and how recent an inventory must be to count (30 days unless you choose otherwise).

If the columns of an export are named differently from those the template expects, the assistant stops and asks which is which.

## What comes out

One report in a fixed order. It opens with a count of every copy found and a tie-out line proving the counts add up. Then come the out-of-date copies, each with the evidence of withdrawal on file; copies of withdrawn documents; unrecognised revisions; documents missing from the master list; coverage gaps; copies not yet due to change; and withdrawal records that match nothing found. The report ends with a numbered list of decisions for document control, and a line stating what it cannot prove.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/), where controlled documents are one of the first things an auditor asks to see in use.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where work instructions sit at the machine and a superseded one can stay there for months.
- [Life sciences](https://fullypowered.ai/industries/life-sciences/), where the revision in use at the point of work matters as much as the one approved.
- [Construction](https://fullypowered.ai/industries/construction/), where site teams work from printed method statements and drawings kept in cabins and vehicles.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where copies have accumulated over years and nobody has a full picture of them.

## What has to change for your company

Fix the files and their column names once, so each review starts from the same exports. Decide how recent an inventory must be to count; the template assumes 30 days. Decide what counts as evidence of withdrawal in your business, such as a signed return slip or a recorded removal. Agree who inventories each place and in what form, including saved files on shared drives and tablets, which are copies too. Name who confirms an obsolete copy and who removes it. Settle how revisions are written, since the comparison reads them as they appear.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it, and it was not a blind trial, since the run had seen the published output before writing its own. The points that run and the independent review found open were settled afterwards, without a rerun. It has not yet been tested in a client environment, or tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past review you already know well, with cases written in advance: a withdrawal recorded but the copy still there, a location nobody inventoried, an inventory that predates the withdrawal, a revision not on the history. Document control checks every finding against the physical copy before anyone relies on the report. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep. For writing the procedure itself, see [Write an SOP from how the work is done](https://fullypowered.ai/workflows/sop-from-how-the-work-is-done/); for tidying electronic folders, see [Shared folder filing plan](https://fullypowered.ai/workflows/shared-folder-filing-plan/).

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

- [Write an SOP from how the work is done](https://fullypowered.ai/workflows/sop-from-how-the-work-is-done/)
- [Shared folder filing plan](https://fullypowered.ai/workflows/shared-folder-filing-plan/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
