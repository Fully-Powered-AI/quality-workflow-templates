# Cost of poor quality worksheet

An owner or operations lead who senses that rework, scrap and returns are costly gets one worksheet: the failure costs already on record, sorted by category, with estimates, gaps and unresolved allocations listed. The owner decides what to fix first.

*Workflow template · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/cost-of-poor-quality-worksheet/)*

## The outcome

Most owners can feel what rework, scrap and returns cost long before anyone has added it up. The figures live in different places: a timesheet note here, a stock write-off there, a credit note in the accounts, a courier invoice nobody split. This workflow template gathers what is already on record into one worksheet for a period.

Every cost is shown with how it is known: recorded in the books, or estimated from hours and an approved rate. A cost nobody has put a figure on stays unknown and is listed as such; it is never counted as zero. Costs that cannot yet be assigned to a category or a product are listed as unresolved allocations, and rows that look counted twice are held out for a person to confirm.

The worksheet shows where the known cost sits. It does not say what to fix first, and it claims no saving. The owner decides, with finance confirming the cost basis.

## Who starts the work, and when

The owner, operations lead or quality lead starts it when failures keep recurring and nobody can say what they add up to, before a planning or pricing round, or on a set rhythm such as each quarter. A finance contact reviews the cost basis before anyone acts on the figures.

## What they supply

- **The failure cost export for the period,** as a spreadsheet: one row per rework, scrap, return, credit or replacement, with its date, category, process or product, hours or amount, and where the figure came from.
- **Prevention and appraisal costs,** if the business tracks them: training, calibration, inspection and similar, as a second export.
- **Their settings:** the period, the currency, the category list, the approved hourly labor rate if there is one, and the costing rules finance has agreed, such as how a credit note is counted.

## What comes out

One worksheet in a fixed order: known failure cost by category, split into internal and external failure; where the known cost sits by process or product; estimated costs with their hours and rate; rows with no cost; unresolved allocations; possible duplicates held out; prevention and appraisal costs as supplied; the assumptions used; rows left out of the period; and numbered questions.

Each total is shown with how much of it is recorded and how much is estimated, so a reader can see how firm the number is.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/), where failures are recorded and where the cost of repeating them is rarely seen in one place.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), which owns the processes the worksheet points at.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which confirms the cost basis before the figures are used.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where scrap and rework are counted in hours and materials.
- [Construction](https://fullypowered.ai/industries/construction/), where redoing work on site is the common failure.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where returns and credits are the visible cost.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where years of records exist and nobody has added them up.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the volume of work grows faster than the checks on it.

## What has to change for your company

Agree your categories before the first run and keep them stable, because the totals are only as good as the labels. Decide with finance which costs count: whether a credit note is counted at its value, whether a returned item's lost value is included, and whether an hourly rate covers wages only. Set the period and how often it runs. Decide who reads the worksheet and who may see it. It runs in ChatGPT, Claude, Copilot or Gemini, from the exports you supply; it needs no access to any system.

For a single product's import costs, use [product landed cost worksheet](https://fullypowered.ai/workflows/product-landed-cost-worksheet/). For why actual spending differs from plan, use [budget versus actual variance commentary](https://fullypowered.ai/workflows/budget-versus-actual-variance-commentary/). This one is about the cost of failures only.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once, with Claude, on its invented example on 10 November 2026; no stop condition was exercised in that run, and the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past quarter your finance contact already knows, plus cases written in advance: a column renamed in the export, a row with hours and no rate, the same write-off listed in two exports, a cost with no category. Finance checks every total against the books before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Repeat incident pattern review](https://fullypowered.ai/workflows/repeat-incident-pattern-review/)
- [Product landed cost worksheet](https://fullypowered.ai/workflows/product-landed-cost-worksheet/)
- [Budget-versus-actual variance commentary](https://fullypowered.ai/workflows/budget-versus-actual-variance-commentary/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
