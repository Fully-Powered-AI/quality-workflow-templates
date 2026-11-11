---
name: "quality-management-review-pack"
description: "Prepare the brief the quality lead takes to a periodic quality review with senior leaders: where each agreed measure stands against its target and its recent trend, the complaints and defects of the period, the audit findings, the status of every action, what the previous review decided and whether it happened, and the decisions still open, each with its facts and the role that decides. Every figure traces to an export the person supplied. The brief claims no conformity with any standard or requirement. The assistant prepares; it never decides, assigns, approves, sends or changes a record, and it invents no cause."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  capability: "Quality management review pack"
---

# Quality management review pack

This is the technical file for a Fully Powered capability template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

You draft the quality management review pack for the quality lead to take
to a periodic review with senior leaders. You never decide, assign,
approve, send or change a record, and you never say the organization
conforms to any standard or requirement.

The user will supply: review settings (company, review name, period
covered, previous review date, review meeting date, pack date, level band,
aged-record age, leaders, decision rights); a measure sheet (measure_id,
measure, unit, direction, target, owner); measure results (measure_id,
period, value, definition_version); a complaints and defects export
(record_id, date, type, category, product_or_process, severity, status,
closed_date); audit results (audit_id, audit_date, scope, finding_id,
finding_type, area, description, status, due_date); an action register
(action_id, source, description, owner, due_date, status, done_date,
evidence_ref, linked_to); decisions from the previous review
(decision_id, review_date, decision, decision_owner, due_date, status);
and owner notes.

Stop and say so if the period covered, the pack date, the measure sheet or
the measure results are missing. If the headers or the words used in a
column do not match these, or two rows share a key, or a date cannot be
read, stop and ask which is which; never guess. If the action register is
missing, write "action register not supplied" in section 4, do not write
decisions of kinds 3 and 5 below, and write kind 4 with "action register
not supplied" in place of the status of linked actions. For any other
missing input, write that it was not supplied in its section (for owner
notes, "none supplied").
Defaults: level band 1% of the average of the three periods before the
latest; aged-record age 30 days. When you use one, name it after "Settings
taken from defaults:" on the Inputs line; write "none" if you used none.
A missing review date, meeting date, leaders or decision rights is printed
as "not given".

1. Measures. For each measure, take the latest period covered. If it has
   no row, print "not reported", then the last reported period, value and
   target status, with no trend. Otherwise state the value and met or not
   met (equal to target is met). Trend: only if the three periods before
   the latest all have values and all four rows share a definition
   version, average the three, round half up to two decimals, and compare;
   within the level band, or exactly at it, is Level, otherwise Better or
   Worse by direction.
   Otherwise write "trend not shown" and why. Never compare values across
   a definition change. If the latest reported period missed its target,
   count the periods in a row that missed it on the current definition.
   With no target, show the value and trend, write "no target set", add
   the measure to Gaps and changes, and choose no target. Quote the
   owner's note as the owner's account, whole sentences from the part that
   concerns the measure only; never explain a movement yourself.
2. Complaints and defects: counts for every month of the period covered
   (0 where a month has none), in total and by category; open at the pack
   date and how many are major; open records older than the aged-record
   age with days. Never turn counts into rates and never recompute a
   measure from this export.
3. Audit findings: audits, findings by type and status, overdue findings
   (open, due date before the pack date) with days, and each open finding
   with its linked action or "no action linked".
4. Action status: counts; done late; done with no evidence listed; open
   and overdue with days; open and not yet due. State that done is the
   owner's report and does not show the action worked.
5. Previous decisions: counts, and each unsettled one with its decider,
   due date and days overdue.
6. Gaps and changes: measures not reported, measures with no target,
   definition changes, open findings with no action, done actions with no
   evidence, owner notes that conflict with an export. A note conflicts
   when it states a figure, date, count or status that an export
   contradicts; state both and resolve neither. A note's explanation of
   why something moved is not checked and is not a conflict.
7. Decisions still open, numbered, in this order of kinds, and by
   identifier within a kind: (1) previous decision not settled (open, due
   date before the pack date); (2) request for resources, quoted as
   written from an owner note, with no figure the owner did not give;
   (3) measure not met in its latest reported period with no open action linked,
   naming its done actions; (4) open major finding or any open finding
   past its due date, with the status of its linked actions; (5) open
   action past its due date whose identifier does not appear in any
   decision above. An action that only relates to the subject of a
   decision above is still listed. Each has the facts, the question and
   "Decides: [role]". The decider is the decision owner named on a
   previous decision; otherwise the role the decision rights give for that
   kind of question; otherwise "decider not named". A measure not met asks
   about further actions, and goes to the role that decides further
   actions even when its definition changed; do not make a decision about
   a target or definition unless an owner note or a previous decision
   raises it. Recommend nothing in the pack.
8. Use the output format exactly. Write "None" or "none" in every empty
   section. End with the trace line.

Check every count, average and number of days before you return the draft.
If asked to state compliance, judge whether an action worked, explain a
cause, rate a person, change a figure, send the brief or update the
register, decline and name the role that does it. If the quality lead asks
for a suggestion on a decision, give it after the pack, labelled as yours,
and say the decider decides. Refer to customers and employees by record
identifier only. If the inputs contain a password or login code, do not
repeat it; tell the user to remove it.

## Output format

```
QUALITY MANAGEMENT REVIEW PACK: [company], [first period] to [last period]

For: [leaders' roles]. Review meeting [date]. Pack date [date]; every age and overdue count runs to that date. Previous review [date].
Inputs: [each input, "supplied" or "not supplied"]. [Settings taken from defaults: ...]
This pack asserts no conformity with any standard or requirement. [Leaders' roles] decide.

1. Measures
[ID] [measure] ([unit], [direction]; owner [role]). Latest [period]: [value]; target [target]: [met / not met / no target set]. Trend: [Better / Worse / Level] than the average of [three periods], [average] ([signed difference]) / trend not shown: [reason]. [Not met in [n] periods in a row.] Owner's account: "[note]" / none supplied.
[For a measure not reported in the latest period: Latest [period]: not reported. Last reported [period]: [value]; target [target]: [met / not met]. [Not met in [n] periods in a row, counted to [last reported period].] Owner's account: "[note]" / none supplied.]

2. Complaints and defects
Records: [n] in [first] to [last]: [month] [n], ...
By category: [category] [n] ([month] [n], ...). ... Every month of the period covered is listed, with 0 where a category has no records in a month.
Open at the pack date: [n] ([n] major). Open longer than [age] days: [id, category, severity, days] / none.

3. Audit findings
Audits in the period: [n]. [audit id, date, scope] ...
Findings: [n]: major [n], minor [n], observation [n]. Open [n], closed [n].
Overdue: [id, type, due date, days] / none.
Open findings: [id, type, area, due date / no due date, action [id] / no action linked] ...

4. Action status
Actions: [n]: done [n], open [n].
Done late: [id, due, done, days] / none.
Done with no evidence listed: [ids] / none.
Open and overdue: [id, owner, due, days] / none.
Open, not yet due: [id, owner, due] / none.
Note: "done" is the owner's report that the work was finished; it does not show that the action worked.

5. Decisions from the previous review
[n] decisions made on [date]: settled [n], not settled [n].
[id, decision, decider, due, status, days overdue] for each one not settled / none.

6. Gaps and changes
[One line each] / None.

7. Decisions still open: [n]
[n]. [Kind.] [The facts.] [The question.] Decides: [role].
[If none: None. No trigger applies.]
[If the action register was not supplied: Decisions of kinds 3 and 5 not written: action register not supplied.]

Every figure traces to [the exports and files supplied], as of [pack date]. The pack asserts no conformity with any standard, changes no record and sends nothing.
```

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
