# Quality management review pack

Before the periodic quality review, the quality lead gets one brief for senior leaders: where each measure stands, complaints and defects, audit findings, action status, and the decisions still open. The leaders decide; the brief claims no compliance with any standard.

*Workflow template · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/quality-management-review-pack/)*

## The outcome

The review meeting starts from decisions, not from a tour of charts. The quality lead walks in with one brief in a fixed order: each agreed measure against its target and its recent trend, the complaints and defects of the period, the audit findings and where each stands, every action with its owner and date, and what the leaders decided last time and whether it happened.

The last section is the one that matters. It lists the decisions still open, each written as a question with its facts and the role that decides: a decision from the previous review still open and past its date, a measure that missed its target in its latest reported period with no action left open against it, an open major finding or any open finding past its date, an owner's request for people or money. Gaps stay visible. A measure with no figure for the latest period says so, and a changed definition is named instead of being smoothed over.

The brief states no conformity with any standard or requirement. That judgement belongs to the people accountable for it. The AI assistant counts, compares and lays out; it invents no cause, recommends nothing unless asked, and changes and sends nothing.

## Who starts the work, and when

The quality lead, or someone working for them, runs it about a week before each periodic review, once the period's exports are out and the owners have added their notes. A second run after owners correct their entries gives the brief that goes to the leaders. The quality lead checks every figure and decides what goes into the meeting.

## What they supply

- **The measure sheet:** each agreed quality measure with its unit, which direction is good, its target and its owner.
- **The measure results:** one row per measure per period, with the definition version in force.
- **The complaints and defects export** for the period.
- **The audit results:** each audit and its findings, with status and due date.
- **The action register,** and the decisions made at the previous review.
- **Short notes from owners** on why a measure moved, and any request for resources.
- **A few settings:** the dates, which role decides what, and how old an open record must be before it is listed.

## What comes out

One brief in seven numbered sections: measures, complaints and defects, audit findings, action status, decisions from the previous review, gaps and changes, and the decisions still open. A trace line closes it, naming the exports and the date behind every figure. Where a section has nothing to report it says "None", so a blank can never be mistaken for an omission.

When an export's columns do not match what the template expects, the work stops and asks which column is which. A missing month is reported as not reported, never read as zero.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/), which owns the measures, the findings and the actions the review looks at.
- [Leadership](https://fullypowered.ai/functions/leadership/), where the people who allocate resources and settle open questions need the picture on one page.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where yield, defects and supplier rejections are reviewed on a rhythm.
- [Life sciences](https://fullypowered.ai/industries/life-sciences/), where records of findings and actions have to be kept in order for the review.
- [Hardware and physical technology](https://fullypowered.ai/industries/hardware-and-physical-technology/), where complaints from the field and defects from the line are read side by side.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the review pack is rebuilt by hand from several spreadsheets each cycle.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/), when volume rises faster than the quality lead's time to prepare for leaders.

It stays apart from two neighbours. [Operations KPI scorecard](https://fullypowered.ai/workflows/operations-kpi-scorecard/) is a monthly page of operating measures. This is the periodic quality review, which adds audits, actions and the leaders' open decisions. [Board meeting pack](https://fullypowered.ai/workflows/board-meeting-pack/) is the CEO's pre-read for one board decision. This brief is the quality lead's, covers the whole quality picture of a period, and ends in the decisions still open for the leaders.

## What has to change for your company

Fix the measure sheet once, with one owner for each measure and a note of when a definition changes. Decide the period and the meeting date, and how much movement counts as level. Say which role decides resource questions, which decides targets and definitions, and how old an open complaint or defect must be before it is listed. Agree the status words your action register uses. It runs in ChatGPT, Claude, Copilot or Gemini from the exports and notes you supply; it needs no access to any system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it. The trial was not blind, and the template was revised after it and run again on the example by the model that revised it, which is not an independent test. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past review your quality lead remembers well, with cases written in advance: a measure whose definition changed, a month with no figure, an action marked done with no evidence, a decision carried from the last review. The quality lead checks every figure against its export before anyone relies on the brief. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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
- [Operations KPI scorecard](https://fullypowered.ai/workflow templates/operations-kpi-scorecard/)
- [Decision log](https://fullypowered.ai/workflow templates/decision-log/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
