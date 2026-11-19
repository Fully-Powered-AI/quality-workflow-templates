# Supplier quality response check

Set a supplier's reply to a defect finding beside what was asked: what is answered, what is not and what is unverified. A person decides. Free template.

> [!TIP]
> **Missing a template that is not listed here, or want these customized for your organization? Reach out to us.** This is a template, made to be customized and deployed. FullyPowered AI customizes and builds AI workflows, connects them to your business systems, installs them in your agents and puts them in the hands of the people who own the work. [See Supplier quality response check on our website](https://fullypowered.ai/workflows/supplier-quality-response-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check). Not sure where to start? Email hello@fullypowered.ai and a person will answer.

**Quick start**

1. Read EXAMPLE.md to see what a good result looks like.
2. Copy all of TEMPLATE.md into your assistant, then give it your own inputs, or the invented ones from EXAMPLE.md.
3. Read what comes back. It marks what it checked and what is left for you.

*Workflow template · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/supplier-quality-response-check/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check)*

## The outcome

A supplier's reply to a quality finding is easy to read as an answer and hard to read as a comparison. This workflow template does the comparison. It takes the approved finding, lays each thing the finding asked for beside what the reply actually says, and marks each one as addressed in full, addressed in part, not addressed or disputed.

It then separates what the supplier has done from what the supplier has promised. A promised action is not a completed one, and a completed one is not a verified one, so each action is labelled with where it stands. The reply is also read against your own records: a lot the reply never mentions, a figure that differs from yours, a cause that explains only part of the failures.

The result ends with the evidence still worth asking for, what must be seen before the finding can close, and the choices open to the owner. It accepts nothing, closes nothing and writes nothing to the supplier. For the notice that raises a problem, use [supplier issue notice](https://fullypowered.ai/workflows/supplier-issue-notice/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check); for the supplier's record over time, use [supplier performance scorecard](https://fullypowered.ai/workflows/supplier-performance-scorecard/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check).

## Who starts the work, and when

The supplier-quality owner, or the quality or purchasing person who raised the finding, starts it when the supplier's reply arrives, and again if a second reply follows. It needs the finding to be approved already, so that there is a fixed statement of what was found and what was asked.

## What they supply

- **The approved finding,** with the requirement, what was found, the lots and quantities in scope and the numbered things asked of the supplier.
- **The supplier's reply,** exactly as received, with the date it arrived.
- **A list of the attachments** that came with it, one line each.
- **The agreed quality responsibilities:** the reply period, what a reply must cover, who verifies and any escalation route.
- **Their settings:** today's date, working days, closed dates and the next scheduled delivery.

## What comes out

One check, in a fixed order: whether the reply was on time; each request in the finding against the reply; where the reply differs from your records or is unclear; the actions proposed, each labelled promised or reported done; the attachments received and the evidence to ask for; what is still to be verified, with the criterion where the finding states one; and the decision left to the owner. Every empty section says so.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where findings are raised, replies judged and effectiveness checked.
- [Procurement and suppliers](https://fullypowered.ai/functions/procurement-and-suppliers/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where the same supplier relationship is managed commercially.
- [Supply chain and inventory](https://fullypowered.ai/functions/supply-chain-and-inventory/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where stock in transit and on hold has to be accounted for.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where a purchased part that fails often stops a line.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where a supplier's defect becomes a customer's complaint.
- [Hardware and physical technology](https://fullypowered.ai/industries/hardware-and-physical-technology/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where components come from many small suppliers.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), where supplier replies pile up in inboxes and are judged from memory.
- [Growth and scaling](https://fullypowered.ai/situations/growth-and-scaling/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check), when more suppliers and more findings outgrow one person's recall.

## What has to change for your company

Name the owner who decides whether a reply is accepted, and write down the agreed reply period and what a reply must cover. Give each finding numbered requests, so the reply can be set against them, and state a verification criterion wherever you can, such as how many later lots must pass. Decide who may see the check and where it is kept. It runs in ChatGPT, Claude, Copilot or Gemini from the text you paste in; it needs no access to any system.

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026 in two runs; the record of the second is published with it, and no edit has been made since. It has not yet been tested in a client environment, and it has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past finding and reply your quality owner already knows well, plus cases written in advance: a reply that never mentions one lot, a promised action reported as done, a figure that differs from your records, a late reply, a finding label left out. The owner checks every line against the finding and the reply before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check) describes the record we keep.

- Written by FullyPowered AI.
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

- [Supplier issue notice](https://fullypowered.ai/workflows/supplier-issue-notice/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check)
- [Supplier performance scorecard](https://fullypowered.ai/workflows/supplier-performance-scorecard/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check)
- [Incident investigation and corrective actions](https://fullypowered.ai/workflows/incident-investigation-and-corrective-actions/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/?utm_source=github&utm_medium=referral&utm_campaign=workflow-collections&utm_content=quality-supplier-quality-response-check&from=gh-supplier-quality-response-check).
