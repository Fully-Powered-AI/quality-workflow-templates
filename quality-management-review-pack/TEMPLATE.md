# Quality management review pack

Capability template, version 0.1.0.

## Purpose

Prepare the brief the quality lead takes to a periodic quality review with senior leaders: where each agreed measure stands against its target and its recent trend, the complaints and defects of the period, the audit findings, the status of every action, what the previous review decided and whether it happened, and the decisions still open, each with its facts and the role that decides. Every figure traces to an export the person supplied. The brief claims no conformity with any standard or requirement. The assistant prepares; it never decides, assigns, approves, sends or changes a record, and it invents no cause.

## When to use it and when not to

Use it about a week before each periodic review, once the period's exports are out and owners have added their notes. Run it a second time after owners correct their entries, to produce the version that goes to the leaders.

Do not use it:

- as a monthly page of operating measures. That is a different piece of work, a scorecard of a few measures with a red, amber or green status;
- to prepare a board or investor pack;
- to say that the organization conforms to a standard, a regulation or a customer requirement, or to rate a person's performance;
- to investigate the cause of a defect or to judge whether an action worked. Those are tasks for the people who own them;
- when no measure sheet or results export exists. The quality lead writes the first versions; this capability reads them.

## Roles

- **Runs it:** the quality lead, or someone working for the quality lead.
- **Checks every figure and approves the brief:** the quality lead.
- **Owns each measure, action and finding:** the role named on the sheet or register. Owners write their own notes.
- **Decides:** the leaders named in the settings, each within the decision rights stated there. The decision owner named in a previous decision stays the decider for it.
- **Records the decisions taken at the meeting:** the quality lead, in the organization's own register. The assistant records nothing.

## Inputs

All inputs are files or text the person supplies. The assistant needs no connection to any system and never asks for a password or a login code.

1. **Review settings.** Company, the review and its name, period covered, previous review date, review meeting date, pack date, the level band (default 1% of the average of the three periods before the latest), the age at which an open complaint or defect is listed (default 30 days), the leaders, and the decision rights. If the period covered or the pack date is missing, stop and ask. For the level band and the aged-record age use the default if missing, and name it after "Settings taken from defaults" on the Inputs line. A missing previous review date, meeting date, leaders or decision rights is printed as "not given"; a missing decider reads "decider not named".
2. **Measure sheet.** Default headers: `measure_id,measure,unit,direction,target,owner`. Direction is `higher_is_better` or `lower_is_better`. If missing, stop.
3. **Measure results.** Default headers: `measure_id,period,value,definition_version`. Periods are written `YYYY-MM`. If missing, stop.
4. **Complaints and defects.** Default headers: `record_id,date,type,category,product_or_process,severity,status,closed_date`. Type is `complaint` or `defect`; status is `open` or `closed`. If missing, write "complaints and defects not supplied" in section 2 and continue.
5. **Audit results.** Default headers: `audit_id,audit_date,scope,finding_id,finding_type,area,description,status,due_date`. Finding type is `major`, `minor` or `observation`. If missing, write "audit results not supplied" in section 3.
6. **Action register.** Default headers: `action_id,source,description,owner,due_date,status,done_date,evidence_ref,linked_to`. Status is `open` or `done`. The `linked_to` field holds a measure id, a finding id or a record id. If missing, write "action register not supplied" in section 4, do not write decisions of kinds 3 and 5, and write kind 4 with "action register not supplied" in place of the status of linked actions.
7. **Decisions from the previous review.** Default headers: `decision_id,review_date,decision,decision_owner,due_date,status`. Status is `open` or `done`. If missing, write "previous decisions not supplied" in section 5.
8. **Owner notes.** Free text from the owners. If missing, write "owner's account: none supplied" for each measure.

If the headers of any export do not match, or a status or direction uses other words, stop and ask which column or word means what. Never guess a mapping. Dates that cannot be read as dates stop the work in the same way.

## The procedure

1. **Check the inputs.** Confirm one period covered (first and last month) and one pack date. Confirm every measure id in the results is on the measure sheet, and every period is `YYYY-MM`. Count the rows of each file. If two rows of one file share a key (the same measure and period, the same record id, the same finding id, the same action id), stop and ask which is right.
2. **Measures.** For each measure on the sheet, take the latest period in the period covered.
   1. If the results hold no row for that period, print "not reported" for the latest period and then the last reported period and its value, with its target status. Show no trend.
   2. Otherwise state the latest value and whether it meets the target. A value equal to the target meets it. For `higher_is_better` it meets the target if it is at or above; for `lower_is_better`, at or below.
   3. Trend: find the three periods immediately before the latest. If all three have values and all four rows carry the same definition version, take the average of the three, round half up to two decimals, and compare the latest value with it. If the difference is within the level band (a difference exactly equal to the band counts as Level), print Level. Otherwise print Better if the difference moves in the good direction and Worse if not. Print the average and the signed difference to two decimals.
   4. If a period is missing among the three, or the definition version changes between them and the latest, print "trend not shown" with the reason. A definition change is named with the period it took effect and how many periods sit on the current definition. Values on the earlier definition are never compared with values on the current one.
   5. Count the periods in a row, going back from the latest reported period, in which the target was not met, using only periods on the current definition. Print the count only if the latest reported period did not meet the target.
   6. Add the owner's note about the measure, quoted as written and marked as the owner's account. If the note is long or concerns several measures, quote whole sentences, as written, only from the part that concerns this measure; a request for resources is quoted in full in its decision. Never explain a movement in your own words.
3. **Complaints and defects.** Count the records dated in the period covered, by month, and by category with a count for each month. Count those open at the pack date and how many of them are major. List each open record older than the aged-record age, with its category, severity and age in days to the pack date. Do not turn counts into rates. A measure's figure comes from the results export and is never recomputed from this one.
4. **Audit findings.** List the audits dated in the period covered. Count findings by type and by status. A finding is overdue if its status is open, it has a due date and the due date is before the pack date; print how many days. List every open finding with its type, area, due date and the action linked to it, or "no action linked". A finding with no due date prints "no due date".
5. **Action status.** Count actions by status. List: actions done after their due date, with the days late; actions marked done with no evidence listed; actions open and past their due date, with owner and days overdue; actions open and not yet due. Always end the section with the statement that done is the owner's report and does not show the action worked.
6. **Decisions from the previous review.** Count them by status. List each one not settled with its decision owner, due date and, if past due, the days overdue.
7. **Gaps and changes.** List, each once: a measure with no figure for the latest period; a measure with no target; a definition change; an open finding with no action linked; an action marked done with no evidence listed; an owner note that conflicts with an export (state both, resolve neither). A note conflicts when it states a figure, date, count or status that an export contradicts. A note's explanation of why something moved is not checked and is not a conflict.
8. **Decisions still open.** Write one numbered decision for each trigger below, in this order, and inside a kind in the order of the identifiers. A decision states the facts, the question, and who decides.
   1. **Previous decision not settled:** a decision with status open and a due date before the pack date.
   2. **Request for resources:** an owner note that asks for people, time, money or equipment. Quote the request as written. Add no figure the owner did not give.
   3. **Measure not met, no open action:** a measure that did not meet its target in its latest reported period (a measure not reported in the latest period counts by its last reported period) and has no open action linked to it. Name its linked actions that are done.
   4. **Finding to settle:** an open major finding, or any open finding past its due date, with the status of its linked actions.
   5. **Overdue action:** an open action past its due date whose identifier does not appear in the text of any decision above. An action that only relates to the subject of a decision above, without its identifier appearing there, is still listed. An identifier in the facts of an earlier decision counts as named.

   Who decides: the decision owner named on a previous decision; otherwise the role the decision rights give for that kind of question; otherwise "decider not named". A measure not met (kind 3) asks about further actions and goes to the role that decides further actions, even when the measure's definition changed in the period. Make no decision about a target or definition unless an owner note or a previous decision raises it; then it goes to the role that decides targets and definitions. Recommend nothing in the pack.
9. **Trace line and return.** Name the exports and the pack date behind every figure. Return the draft to the person who ran it, for the quality lead's approval. A person decides what goes to the leaders.

## Exceptions and stop conditions

- **No measure sheet or results, or no period covered or pack date:** stop and ask. Do not propose measures.
- **No action register:** do not stop. Follow input 6.
- **Headers or words that do not match the defaults:** stop and ask which column or word means what.
- **A measure id in the results that is not on the sheet, or two rows with the same key:** stop and ask.
- **A measure with no target:** show its latest value and trend, write "no target set" for the target status, and add it to Gaps and changes. Do not choose a target.
- **A missing period:** report it as not reported. Never read it as zero and never fill it from another period.
- **Asked to state that the organization conforms, to judge whether an action worked, to explain a cause, to rate a person, or to change a figure so it looks better:** decline. The people accountable decide. Offer to list the facts that bear on the question.
- **Asked to recommend a decision:** put no recommendation in the pack. If the quality lead asks for a suggestion, give it after the pack, labelled as the assistant's, and say that the decider decides.
- **Asked to send the brief, update the register or close an action:** decline; a person does that.
- **Records containing names of customers or patients, or personal data about an employee:** refer to the record by its identifier only.
- **Any credential in the inputs:** do not repeat it; tell the person to remove it from the source.

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

## Reviewer checklist

1. Every value, target status and not-met count matches the results export and the measure sheet. (Quality lead)
2. Every trend average and difference is recomputed by hand and rounds as stated, and no trend crosses a definition change. (Quality lead)
3. Counts of complaints and defects match the export by month and category, and every age is counted to the pack date. (Quality lead)
4. Audit findings, overdue findings and the actions linked to them match the audit results and the register. (Quality lead)
5. Every action is counted once, and "done" is never worded as "effective". (Quality lead)
6. Every owner note is quoted as written, and no cause is given in the assistant's own words. (Each owner)
7. Every decision traces to one of the five triggers, names a decider, and recommends nothing in the pack. (Quality lead)
8. No decision from the previous review has been dropped, and no gap has been hidden. (Quality lead)
9. Nothing in the brief says the organization conforms to anything. (Leaders' delegate)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary period.** Complete files, all measures reported, no definition change. Expected: all seven sections complete, trend shown for every measure, decisions only where a trigger applies.
2. **Missing latest period.** A measure has no row for the latest period. Expected: "not reported", the last reported value and its target status, no trend, an entry in Gaps and changes, and the owner's note quoted.
3. **Definition change.** A measure moves from v1 to v2 two periods before the end. Expected: trend not shown with the reason, v1 values never compared with v2 values, not-met count only on v2.
4. **Value on the target.** A value equal to the target. Expected: met.
5. **Value inside the level band.** Latest value within 1% of the prior three average, and a second case with a difference exactly equal to 1%. Expected: Level in both.
6. **Column renamed.** The results export uses `month` for `period`. Expected: stops and asks.
7. **Measure not met with its only action done.** Expected: a decision of the third kind, naming the done actions and stating no open action is linked.
8. **Action done, no evidence.** Expected: listed under done with no evidence and under Gaps and changes; not counted as effective.
9. **Request in an owner note.** Expected: a decision of the second kind with the request quoted and no figure added.
10. **Asked to say the organization conforms.** Expected: declines and offers the facts.
11. **Asked to recommend a decision.** Expected: puts no recommendation in the pack; if the quality lead asks for a suggestion, gives it after the pack, labelled as the assistant's.
12. **Empty sections.** No open findings, no overdue actions. Expected: "none" or "None" in each, never a blank.
13. **Duplicate key.** Two action rows with the same id. Expected: stops and asks.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
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
```

## What to customize

- The measure sheet, with one owner per measure, and the rule for recording a definition change.
- The period, the meeting date and the level band.
- The age at which an open complaint or defect is listed.
- The leaders, and which role decides resources, further actions, targets and definitions.
- The status words in your action register and decision list, and the columns of your exports.
- Whether a major finding always becomes a decision, or only when overdue.
- Who adds owner notes, and by which day before the meeting.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 10 November 2026 (the record is published with it); the trial was not blind. The trial found faults, and the template was revised afterwards: the test for an overdue action named above, one rule for missing inputs, the defaults and decision rules in the pasted block, the month listing, the owner-note conflict test and the suggestion rule. The revised template was run again on the example by the model that revised it, which is not an independent test. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
