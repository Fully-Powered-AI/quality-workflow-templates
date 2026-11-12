# Nonconformity record draft

A quality lead or supervisor who has spotted something wrong gets a draft record: the observation set against the stated requirement, the affected work counted from the register, and the containment options. The quality owner decides every call.

*Workflow template · Quality management · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/nonconformity-record-draft/)*

## The outcome

Something looks wrong on the floor, and the notes are in a pocket or a message thread. This workflow template turns them into a draft record the quality owner can confirm or reject the same day. What was observed is kept apart from what is only suspected. The requirement is quoted in its own words, with its document and revision, and the observation is set against it with the difference worked out. The work that may be affected comes from your own register, with the pieces counted and anything already shipped called out.

The draft ends with the decisions that belong to the quality owner, each written as a question: whether this is a nonconformity, how serious it is on your scale, what to contain, and whether anyone outside the company needs to know. The assistant classifies nothing, accepts or rejects no work, and certifies nothing.

## Who starts the work, and when

A quality lead or a supervisor starts it right after finding the problem, in an inspection, a review or ordinary work, while the notes are fresh and the work is still where it was left. The quality owner reads the draft, confirms the facts and makes the decisions. The work owner confirms what the register says about the affected lots.

## What they supply

- The observation notes, in the observer's own words, with any readings and the instrument used.
- The requirement: the document, its revision and date, the clause and its exact words.
- The work register, with one row per lot or batch, its machine, location, status and quantity.
- The evidence list: photos, reading sheets and documents, with who took them and when.
- The nonconformity log, so similar records can be found.
- Your settings: the quality owner, the safety role, the look-back period, your classification scale by name and your numbered containment options.

## What comes out

One draft record in a fixed order, with a place for everything the work needs: a safety flag first, the observations numbered, the requirement quoted, the comparison, the evidence and what is missing, the affected work with counts, similar records, the containment options with what each would cover, the decisions for the quality owner, and what to confirm. A section with nothing in it says so. No record number is invented; the quality owner assigns it.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Quality management](https://fullypowered.ai/functions/quality-management/), where the first record of a problem sets the quality of everything after it.
- [Operations & process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where supervisors find problems first and need a quick, consistent way to write them down.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where a lot made on one machine can carry the same problem across several shifts.
- [Construction](https://fullypowered.ai/industries/construction/), where work is checked against specifications and the affected area has to be pinned down.
- [Logistics & trade](https://fullypowered.ai/industries/logistics-and-trade/), where goods that differ from an order or a specification may already be on a vehicle.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where quality records have outgrown notes and memory.

It stops where cause and action begin. [Incident investigation and corrective actions](https://fullypowered.ai/workflows/incident-investigation-and-corrective-actions/) covers cause and corrective actions once the record is accepted, and [complaint and refund request handling](https://fullypowered.ai/workflows/complaint-and-refund-request-handling/) covers a customer's complaint.

## What has to change for your company

Name your quality owner and your safety role. Enter your classification scale; the assistant names it and never applies it. List the containment options you already use, numbered. Match the column headers of your register, evidence list and log to the defaults, or tell the assistant which column holds each field. Decide how "possibly affected" is searched if your scope is a tool, a supplier lot or a shift rather than a machine. Set the look-back for similar records and how record numbers are assigned. For work scoped by area or by shipment rather than by machine and lot, say so in the notes and name the register columns that stand for it.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried once on its invented example in Claude on 10 November 2026; the record is published with it, and lists the edits made afterward that have not been run again. Only the path with no safety risk and no reading within the limit was exercised: the stop conditions and the refusals were not tried. It has not yet been tested in a client environment, and has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past observations your quality lead already knows, with cases written in advance: a reading on the limit, a lot that has shipped, a requirement with no revision, a similar closed record. The quality lead checks every figure against the notes and the register before anyone relies on the draft. [Audit preparation](https://fullypowered.ai/workflows/audit-preparation/) is a good companion for keeping the records that go with it.

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

- [Incident investigation and corrective actions](https://fullypowered.ai/workflows/incident-investigation-and-corrective-actions/)
- [Complaint and refund request handling](https://fullypowered.ai/workflows/complaint-and-refund-request-handling/)
- [Audit preparation](https://fullypowered.ai/workflows/audit-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
