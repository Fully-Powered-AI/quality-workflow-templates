# Quality management review pack: a trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs are the invented example in `public/example.md` (Quill Harbour Components, an invented company; the "history shown" line was removed from the settings after the first trial). No client data was used. The eight inputs are the ones listed under "The inputs" in the example: review settings, measure sheet, measure results (23 rows), complaints and defects (14 rows), audit results (5 rows), action register (8 rows), decisions from the previous review (3 rows) and owner notes (2 notes).

## About this record

This is the second run. A first run, by a model that did not write the template, found faults: the overdue-action decision (kind 5) dropped AC-33 because "named" was undefined, and the history setting, the period range wording, the missing-input rules, the owner-note conflict test, the month listing and the role for a missed target were unclear. The template was then revised, and this record replaces the first run's record.

After the run, an independent review asked for small edits to the template: a rule that a difference exactly at the level band counts as Level, the last reported period counting for a measure not reported in the latest period, a measure with no target listed in step 7, the quoting of long owner notes, and a longer not-reported line in the output format. None changes what the example inputs produce, so the run was not repeated and the output above is the unchanged record of that run.

This run is not independent and not blind. The same model that revised the template ran the revised instruction block and output format on the inputs, having already seen the example's output. The figures were checked with a short script, not taken from the example: M1 average 95.67 and difference -1.47, M2 1.93 and -0.43, ages 50, 43 and 35 days, and 7, 22 and 37 days overdue all agree. It shows that the revised wording produces the six decisions the example holds; it does not show that the template works for a real company or in other products.

## What came out

QUALITY MANAGEMENT REVIEW PACK: Quill Harbour Components, 2026-07 to 2026-09

For: Managing director, Operations director. Review meeting 2026-10-14. Pack date 2026-10-07; every age and overdue count runs to that date. Previous review 2026-07-08.
Inputs: review settings, measure sheet, measure results, complaints and defects, audit results, action register, decisions from the previous review, owner notes: all supplied. Settings taken from defaults: none.
This pack asserts no conformity with any standard or requirement. Managing director and Operations director decide.

**1. Measures**
- M1 First-pass yield (percent, higher is better; owner Production manager). Latest 2026-09: 94.2; target 96.0: not met. Trend: Worse than the average of 2026-06 to 2026-08, 95.67 (-1.47). Not met in 3 periods in a row. Owner's account: "September yield dropped after we changed the bracket material lot on 14 September."
- M2 Customer complaints per 1000 units shipped (rate, lower is better; owner Quality lead). Latest 2026-09: 1.5; target 2.0: met. Trend: Better than the average of 2026-06 to 2026-08, 1.93 (-0.43). Owner's account: none supplied.
- M3 Corrective actions closed by original due date (percent, higher is better; owner Quality lead). Latest 2026-09: 80.0; target 90.0: not met. Trend not shown: the definition changed from v1 to v2 in 2026-08, and 2 periods sit on the current definition. Not met in 2 periods in a row. Owner's account: none supplied.
- M4 Supplier incoming rejection rate (percent, lower is better; owner Purchasing lead). Latest 2026-09: not reported. Last reported 2026-08: 1.6; target 1.5: not met. Not met in 2 periods in a row, counted to 2026-08. Owner's account: "The September supplier rejection figures are not in. The supplier portal export failed. I expect them by 14 October."

**2. Complaints and defects**
Records: 14 in 2026-07 to 2026-09: 2026-07 4, 2026-08 4, 2026-09 6.
By category: Dimensional 8 (2026-07 2, 2026-08 3, 2026-09 3). Finish 4 (2026-07 2, 2026-08 0, 2026-09 2). Packaging 1 (2026-07 0, 2026-08 1, 2026-09 0). Documentation 1 (2026-07 0, 2026-08 0, 2026-09 1).
Open at the pack date: 6 (1 major). Open longer than 30 days: D-121, Dimensional, minor, 50 days; C-204, Dimensional, minor, 43 days; D-122, Dimensional, major, 35 days.

**3. Audit findings**
Audits in the period: 2. A-2026-02, 2026-08-18, Internal audit of the bracket line. A-2026-03, 2026-09-22, Supplier approval review.
Findings: 5: major 1, minor 3, observation 1. Open 4, closed 1.
Overdue: F-01, major, 2026-09-30, 7 days.
Open findings: F-01, major, Process control, due 2026-09-30, action AC-34. F-03, observation, Housekeeping, no due date, action AC-35. F-04, minor, Supplier records, due 2026-10-30, action AC-36. F-05, minor, Supplier records, due 2026-11-15, no action linked.

**4. Action status**
Actions: 8: done 4, open 4.
Done late: AC-37, due 2026-08-31, done 2026-09-05, 5 days.
Done with no evidence listed: AC-32, AC-37.
Open and overdue: AC-33, Purchasing lead, due 2026-09-15, 22 days. AC-34, Production manager, due 2026-09-30, 7 days.
Open, not yet due: AC-35, Maintenance lead, due 2026-10-31. AC-36, Purchasing lead, due 2026-10-30.
Note: "done" is the owner's report that the work was finished; it does not show that the action worked.

**5. Decisions from the previous review**
3 decisions made on 2026-07-08: settled 2, not settled 1.
D-MR-2, Decide whether purchasing reports supplier rejection data monthly, Operations director, due 2026-08-31, open, 37 days overdue.

**6. Gaps and changes**
- M4 has no figure for 2026-09.
- M3 changed definition from v1 to v2 in 2026-08; v1 values are not compared with v2 values.
- F-05 is open and has no action linked.
- AC-32 and AC-37 are marked done with no evidence listed.

**7. Decisions still open: 6**
1. Previous decision not settled. D-MR-2 (decide whether purchasing reports supplier rejection data monthly) was due 2026-08-31 and is open, 37 days overdue. Is it settled at this meeting? Decides: Operations director.
2. Request for resources. The Production manager writes: "We need two weeks of overtime for a re-sort of stock, about 120 hours. I need a yes or no on that." Is the request approved? Decides: Operations director.
3. Measure not met, no open action. M1 is 94.2 against 96.0. Its linked action AC-31 is done; no open action is linked to it. Is any further action wanted? Decides: Operations director.
4. Measure not met, no open action. M3 is 80.0 against 90.0 on the current definition. Its linked actions AC-32 and AC-38 are done; no open action is linked to it. Is any further action wanted? Decides: Operations director.
5. Finding to settle. F-01 (major, Process control) was due 2026-09-30 and is open, 7 days overdue. Its linked action AC-34 is open, 7 days overdue. What is needed to close it? Decides: Operations director.
6. Overdue action. AC-33 (agree supplier rejection reporting with purchasing), linked to M4, was due 2026-09-15 and is open, 22 days overdue, with the Purchasing lead. Is the date extended or is the action escalated? Decides: Operations director.

Every figure traces to the measure sheet, measure results, complaints and defects export, audit results, action register and previous decisions list supplied, as of 2026-10-07. The pack asserts no conformity with any standard, changes no record and sends nothing.

## What was observed

Every required part was produced. Nothing in the inputs triggered a stop: headers and words matched, no key was duplicated, no id was missing from the sheet, and no credential or personal data appeared.

- **Decisions: 6, matching the example.** AC-33 is open and 22 days overdue and its identifier appears in no decision above it, so kind 5 lists it. AC-34 is open and overdue too, but its identifier appears in the facts of decision 5, so it is not listed again.
- **Owner-note conflict:** the Production manager's note gives a reason for the September drop (the lot change on 14 September). It states no figure, date, count or status that an export contradicts, so under the test in the template it is not a conflict and Gaps and changes does not list it.
- **Month listing:** every month of the period covered is printed for every category, 0 where there are none, as the format now says.
- **M3:** not met, definition changed in the period; the further-actions question went to the Operations director, as the template's rule now states.
- **Not-met count for M4:** printed, labelled "counted to 2026-08", as the unreported-measure line allows.
- **Quoting a note:** the first sentence of the Production manager's note is quoted in section 1 and the request in decision 2; nothing was paraphrased.

Open in this run: the template did not say whether a long owner note is quoted whole or in the part that concerns the measure. This run quoted the part that concerns each use. The template was amended afterwards to say so (see the note below).

After this run the example's wording was aligned to the output recorded above (the M3 and M4 lines, the overdue line, the gaps and the decision wording), so the two now read alike. This is one run by one model. It was not tested in a client environment or in other products.
