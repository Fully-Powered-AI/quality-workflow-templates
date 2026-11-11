# Nonconformity record draft: a trial on the invented example

- **Product:** Claude, run in Claude Code

- **Model:** Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md` (settings, observation notes, requirement, work register, evidence list and log). No client data was used. The run was made by an assistant that had not written the template. It read the template and the inputs first, produced the draft by following the instruction block and the output format, and only then read the example's published output.

## What came out

The full draft, as produced before the example's output was read:

```
NONCONFORMITY RECORD (DRAFT): Bracket B-220, lot L-3314, flange height
Status: Draft for the quality lead. Suspected, not confirmed. Nothing classified, held, released, sent or recorded.
Record number: To be assigned by the quality lead.
Observed: 2026-11-10, about 07:45, by the early-shift supervisor, at the press area, rack 4. Prepared 2026-11-10 for the quality lead. Inputs read: observation notes; DWG-B220 revision C (2026-08-18) as typed by the supervisor; work register (export, no as-of date given); evidence list; nonconformity log (2 records).
Safety flag: None stated in the notes. This draft is not a safety assessment.

WHAT WAS OBSERVED
O1. The supervisor, about 07:45 on Tuesday 10 November, before the first shift moved lot L-3314 of Bracket B-220 on from rack 4 in the press area, picked 5 parts at random from the 120 on the rack.
O2. Flange height measured with caliper CAL-07 (sticker: calibration due 30 Nov 2026). Readings in mm: 41.2, 41.3, 41.1, 41.4 and 42.0. 5 of 120 pieces examined.
O3. The parts were made on press brake PB-4 on Monday 9 November.
O4. The drawing at the press is revision C. The supervisor has not checked the document register.
O5. Photos were taken and the readings were written on a sheet.
O6. The rest of the lot has not been touched and is still on rack 4.
O7. Belief, not a finding: "I think the tool setting may have drifted, but I have not looked."
O8. The supervisor has told nobody except the quality lead.

THE REQUIREMENT
DWG-B220, Bracket B-220, revision C dated 2026-08-18, Note 3, flange height: "Flange height 42.0 mm, tolerance plus or minus 0.5 mm." (Range: 41.5 mm to 42.5 mm.)
Source of the extract: typed by the supervisor from the drawing at the press (revision as printed on that drawing).

OBSERVATION AGAINST THE REQUIREMENT
41.2 mm against lower limit 41.5 mm: differs by 0.3 mm (41.5 - 41.2).
41.3 mm against lower limit 41.5 mm: differs by 0.2 mm (41.5 - 41.3).
41.1 mm against lower limit 41.5 mm: differs by 0.4 mm (41.5 - 41.1).
41.4 mm against lower limit 41.5 mm: differs by 0.1 mm (41.5 - 41.4).
42.0 mm against 41.5 to 42.5 mm: within the requirement as written.
Summary: 4 of 5 examined differ from the requirement as written; 115 of 120 not examined.

EVIDENCE
E1, photo, Caliper reading 41.2 on part 1 of 5, Early-shift supervisor, 2026-11-10 07:50
E2, photo, Rack 4 label showing lot L-3314, Early-shift supervisor, 2026-11-10 07:52
E3, measurement sheet, Handwritten readings for the five parts, Early-shift supervisor, 2026-11-10 07:55
Not supplied: measurements of the 115 pieces not examined; a photo of the drawing at the press (the source of the requirement); a record of the document register check of the current revision.

AFFECTED WORK
Observed: B-220, lot L-3314, PB-4, Press area rack 4, In process, 120
Last known good: B-220, lot L-3310, made 2026-11-03, inspection Pass (2026-11-03)
Possibly affected, not yet examined:
  B-220, L-3311, PB-4, Shipped to Customer 1 on 2026-11-05, Shipped, 100 (no inspection result in the register)
  B-220, L-3312, PB-4, Finished goods shelf F2, Finished, 150 (no inspection result)
  B-220, L-3315, PB-4, Press area rack 5, In process, 80 (made 2026-11-10, no inspection result)
Basis: same item_id on the same machine (PB-4), made after the last known good lot (L-3310) and up to today, other than the observed lot. This is a search basis, not a finding.
Counts: observed 120; possibly affected 330; together 450. By status: In process 200; Finished 150; Shipped 100. (200 + 150 + 100 = 450.)
Left out, and why: L-3313, B-220 on PB-2, 150 pieces (same item, different machine); L-3320, B-231 on PB-4, 60 pieces (same machine, different item).
Already outside your control per the register: L-3311, Shipped to Customer 1 on 2026-11-05, 100 pieces. (L-3310, the last known good lot, 200 pieces, also shows as shipped, on 2026-11-04; it is not in the possibly affected set.)

SIMILAR RECORDS
NC-0412, 2026-10-21, B-220, DWG-B220 rev C Note 3, Flange height low on 2 parts in lot L-3271, Closed
Records checked: 2, dated within the last 90 days (since 2026-08-12). NC-0431 (B-190) matches neither the item nor the requirement and is not listed.

IMMEDIATE CONTAINMENT OPTIONS (NONE DONE)
1 Hold in place and tag: would cover L-3314 (120, rack 4), L-3315 (80, rack 5), L-3312 (150, shelf F2); L-3311 (100) is shipped and cannot be held on site. Not done.
2 Move to quarantine cage Q1: would cover the same on-site lots, 350 pieces; L-3311 (100) is shipped. Not done.
3 Inspect every piece: would cover up to 450 pieces; 100 of them (L-3311) are with Customer 1. Not done.
4 Inspect a sample from each lot: would cover L-3314, L-3311, L-3312, L-3315; L-3311 is shipped. 5 of 120 in L-3314 already measured. Not done.
5 Pause the machine on this part until checked: would cover PB-4 for B-220; lot L-3320 (B-231, 60, rack 6) is also on PB-4 and L-3315 is in process (80). Not done.
6 Tell the customer about shipped lots: would cover L-3311 (100, Customer 1, shipped 2026-11-05). Not done.
No option is recommended.

DECISIONS FOR THE QUALITY LEAD
1. Whether this is a nonconformity and its classification on the company's own scale (Minor, Major, Critical; defined in the quality manual).
2. Which containment options (1 to 6), for which lots.
3. Whether NC-0412 (same item and requirement, 2026-10-21, closed) points to a recurrence.
4. Whether Customer 1 must be told about shipped lot L-3311 (100 pieces); this draft informs no one.
5. Whether a second measurement (the 115 pieces not examined) or more evidence is needed before the record is accepted.
6. Who owns the record.
7. Is lot L-3315, dated 2026-11-10, still being made, and is its quantity final?
8. Is the scope "same machine" the right basis, or is it a tool, a shift or a material lot?

CONFIRM BEFORE RELYING ON THIS
Current revision of DWG-B220 (notes say the document register was not checked): document register.
Caliper CAL-07: calibration due 30 Nov 2026, 20 days after today (counted from 2026-11-10); check the sticker and calibration record.
Register status of L-3314 and the 120 pieces on rack 4: matches the notes (In process, rack 4).
Date counted: look-back start 2026-08-12 (90 days before 2026-11-10).

NOT IN THIS DRAFT
Cause and corrective actions: see Incident investigation and corrective actions. Customer complaint: see Complaint and refund request handling. Disposition of the work: for the quality lead.
Prepared for the early-shift supervisor. Nothing has been classified, held, released, sent or recorded by the assistant.
Not completed, and what is needed: current revision check; measurement of the pieces not examined.
```

## What was observed

- Every part of the output format was produced, in order, with no stop condition triggered. The notes, requirement, register headers, evidence list and log were all present and matched.
- The figures matched the published example: four of five readings differ (by 0.3, 0.2, 0.4 and 0.1 mm), one is within, 115 of 120 not examined. Last known good lot L-3310; possibly affected 330 pieces in three lots; together 450; one similar record, NC-0412; one lot shipped, L-3311.
- Differences from the published example:
  - The example puts lot L-3310, the last known good lot, under "Left out, and why". The draft here did not, and mentioned it (it also shows as shipped) in a note under "Already outside your control". The template does not say which is right.
  - The draft split the observation into eight statements; the example uses five. The template does not say how finely to split.
  - The example ends "Nothing outstanding". The draft listed two things as not completed (the revision check and the unexamined pieces). The template does not say whether open items in "Confirm" and "Decisions" also belong on the closing line.
  - The draft added two decisions (the state of lot L-3315, which was made on the day of the draft, and whether "same machine" is the right search basis). The example has six.
  - The example's "Not supplied" evidence names photos of the other four readings; the draft did not, because the handwritten sheet E3 covers all five readings. The draft named the missing record of the revision check instead.
  - The example says lot L-3311 is "not on site per the register" and the draft said it "cannot be held on site". Both read that from the word "Shipped"; neither is stated in the register as a fact about location.
  - The draft's "Prepared for" line named the supervisor, as the template's output format says "Prepared for [starter]". The example names the quality lead.
- Facts in either output that are not in the inputs: none found. Counts and dates are calculations from the inputs (the 90-day start of 2026-08-12, 20 days to the caliper due date, the piece totals). The draft's statement that lot L-3311 "cannot be held on site" and the example's "not on site per the register" are inferences from the word Shipped.

## Where the template was ambiguous or needed a guess

- Who the "starter" is. The roles section says a quality lead or a supervisor; in the example the supervisor wrote the notes and the quality lead ran the capability. "Prepared for [starter]" is therefore unclear.
- Whether the last known good lot belongs in "Left out" or "Already outside your control" when it has also left the site. The template says to list "any lot" that has left the site under the second heading, but the last known good lot is not in the possibly affected set.
- "Register as of date": the export has no as-of date, and the format asks for one. The draft wrote "no as-of date given".
- Whether a lot made today (L-3315) is complete. The register cannot say, and the template has no line for it, so it became a decision.
- Containment wording: the template says to give the facts that bear on each option and recommend none, but a fact such as "this lot has shipped, so it cannot be held" shades into a conclusion. The line between a fact and a judgment is left to the assistant.
- The "Not completed" line is not defined: whether it covers only inputs the assistant lacked or any open item.
- The template contains an unfilled placeholder, "[your look-back]", in the inputs and the procedure, which reads oddly beside the real 90 days supplied in settings.
- The instruction block does not number its steps the same way as the procedure (it has no "check the inputs" step and the numbers shift by one), which is harmless but could confuse a reviewer.

Nothing in the notes triggered a stop: there was no safety risk, no instruction inside the notes or register, no complaint, and no request to classify or find a cause.

This is one run, by one model, on one invented example. It shows the instructions can be followed to the format and reach the same counts. It does not show how the template behaves with real data, other models or other products.

## Edits made after the run

Made following an independent review. The recorded output and observations above are unchanged, and the template was not run again after these edits. Each settles an ambiguity the run found, mostly in the way the run already chose.

- Shipped lots: the template (step 7, the instruction block and reviewer checklist item 6) now says every lot that has left the site is listed under "Already outside your control", whether it is possibly affected, the last known good lot or left out of the search, and says which. The published example now lists lot L-3310 there, as this run's draft did. Acceptance test 15 covers it.
- Observer and starter: Roles now separate the observer (spotted it, wrote the notes) from the starter (runs the capability). "Prepared for [starter]" means the person who ran it, which is the quality lead in the example; this run's draft named the supervisor, who was the observer.
- Register as-of date: the output format now accepts "as-of date not given", as this run wrote; the example says so.
- "Not completed": defined as each open check under "Confirm" and each item under "Not supplied" the starter could settle, with what would settle it. The example's line now lists the revision check, the caliper calibration and the 115 unexamined parts, as this run did.
- Within-requirement case: the exception now overrides "print every section".
- Containment wording: facts are stated as the register gives them ("status Shipped"), not as conclusions about what can or cannot be done. Option 4 in the example now says lot L-3311 has status Shipped.
- "Not supplied" in the example no longer names photos of the other four readings, since sheet E3 holds all five readings.
- The instruction block's steps are renumbered to match the procedure, with the input check and the closing step added.
- "[your look-back]" now reads as "the look-back in your settings". "What to customize" gains a line on scoping by area, work package or shipment.
- Second round of edits, after a further independent review, also not run again: the "Left out, and why" step and instruction now name the last known good lot as a third kind of exclusion; the procedure's containment step now says the section heading carries "(NONE DONE)" instead of marking each option "not done"; the within-requirement exception reads "every reading"; in the example, options 1 and 3 give lot L-3311 as "status Shipped per the register" (and option 3 no longer says "on site"), the supervisor's statement about the photos and the sheet is now observation O4, and a decision 7 asks whether lot L-3315, made today, is complete, which this run had raised as its own decision 7.
- Because the instruction block, the output format and the example were edited, a fresh run is needed before the published example is called the output of the current wording.

