# Obsolete copy check: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs were the invented example's six input tables and settings, in `public/example.md`: review date 2026-11-09, inventory age limit 30 days, seven documents, seven history rows, nine distribution lines, fourteen inventory rows at seven locations and four withdrawal records. No client data was used. The run was one pass, with no follow-up questions.

## A limit on this trial

I did not write the template. I was told to read only the example's inputs before producing the output, but my first read of the example file printed all of it, including its published output. I noticed this before writing my own report. So I worked the classification out again by hand from the inputs (every class, every day count, every withdrawal state and every coverage line) and checked each figure against the inputs, not against the example. But this trial is not blind, and a reader should weigh it accordingly. A later run that has not seen the example would be a stronger test.

## What came out

The report followed the output format section by section. Its main figures:

- Copies found: 16 in 14 rows at 7 locations. Current 6. Out of date 5. Withdrawn document 1. Revision not recognised 1. Not on master list 1. Not yet due 2. Tie-out: 6 + 5 + 1 + 1 + 1 + 2 = 16.
- Locations: 8 on the distribution list; 7 inventoried; 1 not inventoried (Cell 2); 1 inventory too old (Quarantine Cage, checked 2026-08-18, 83 days before the review date). The cut-off was 2026-10-10.
- Out of date, oldest first: Gauge Store WI-210 revision B (234 days; record dated after the inventory, so the location needs a new look); Final Assembly WI-102 revision A, two saved files (161 days; record dated 2026-06-03, copy found after it); Cell 1 WI-101 revision C (56 days; no record); Goods-In WI-205 revision E (35 days; no record. The only record for E is at the Inspection Bay, so it does not match this location).
- Copy of a withdrawn document: Cell 1 WI-140 revision C (454 days, no record).
- Revision not recognised: Inspection Bay WI-210 revision D.
- Not on master list: Despatch LBL-77 revision B.
- Coverage: nine distribution lines, 6 met, 2 cannot say (Cell 2 and Quarantine Cage), 1 short (Inspection Bay, WI-210, none found). Tie-out 6 + 2 + 1 = 9.
- Not yet due: Despatch WI-330 revision D, two printed copies, in force until 2026-11-16.
- Withdrawal records with no copy found: 2 of 4, both consistent (WI-101 revision B at Cell 1, WI-205 revision E at the Inspection Bay).
- Ten decisions for the document controller: four out-of-date copies, one withdrawn document, one revision not recognised, one document not on the master list, then three coverage gaps (Cell 2 not inventoried, Quarantine Cage inventory too old, Inspection Bay expected copy missing).
- "Not proven" named Cell 2 and the Quarantine Cage, and the closing line said that no copy had been confirmed, removed, replaced or recorded.

## What was observed

- Every required part of the output format was produced, and both tie-outs added up. No stop condition was triggered: the headers matched, no id was duplicated, dates were year-month-day, no count cell was blank and no history date was blank. Nothing in the inputs asked for a confirmation, a removal or a record, so the decline paths were not exercised.
- The figures matched the published example in every class, day count, withdrawal state and coverage result. Because of the limit above, that agreement is weaker evidence than it would otherwise be.
- Differences from the published example were small. I dated "Prepared" 2026-11-10, the day of the run, where the example used the review date. I used the singular "1 copy" for one copy where the format shows only "[n] copies", and I wrote the section header counts in copies, not rows (the Out of date section says 5 copies over four lines, because one line holds two saved files).
- Neither output contains a fact that is not in the inputs. A few decision questions in both put forward possible explanations as questions (the example asks whether files were "restored or saved again", or whether a copy is "a draft, a mislabelled copy or a revision missing from the history"). These are guesses offered as questions, not statements.

## Ambiguities and shortcomings in the template

1. **No organization name in the inputs.** The output heading needs "[organization or site]", but the settings do not ask for one. I had to choose a name, and the example uses "the firm". The settings should include an organization or site name.
2. **Withdrawal records match on location, so a record at another location is silently "no record".** The Goods-In revision E copy has a record only for the Inspection Bay. The format has no way to say "a record exists for this revision elsewhere". It reads as "no record", which is correct under the rules but may surprise a reader.
3. **"Inventoried" in the Locations line is not defined.** It could count every location with inventory rows, or only those on the distribution list. They are the same here. They would differ when a location has an inventory but no distribution line, and the template does not say what to do.
4. **A document whose current revision is not yet effective.** WI-330's current revision E takes effect after the review date. The rules handle copies of the older revision D correctly (Not yet due), but a person could read the master list as saying D is already out of date. The template covers the case only in the sorting rule and the description of Not yet due.
5. **The coverage count treats Not yet due copies as meeting an expected count.** That is stated in step 7, but a reader of the report sees "met" for Despatch with two revision D copies of a document that is about to be replaced. The report does not flag it.
6. **Section counts mix copies and lines.** The headings count copies; the lines are inventory rows. The format does not say so, which makes a heading of 5 over four lines look like an error.
7. **Singular and plural.** The format shows "[n] copies" and gives no singular form.
8. **"Recommend nothing unless asked" against the decision wording.** The decisions are written as questions, as required, but some in the example come close to suggesting an answer ("Do you confirm them as obsolete?"). That is within the rule, but the line is thin.
9. **The acceptance tests are marked proposed and none has been run.** This trial ran one scenario that touches tests 2, 3, 4, 5, 6, 7 and 8 in effect. It did not run tests 1, 9 or 10, so the stop-and-ask and decline behaviours remain unchecked.

Everything was done from the supplied text alone. Nothing was sent, recorded or changed, and no copy was confirmed as obsolete.

## Changes made after this trial

After an independent review the same day, and without a rerun, the template, the pasted instructions, the example and the profile were changed. The recorded output and observations above are unchanged and describe the run as it was; where they differ from the rules as they now stand, the rules now stand. The changes:

- Defect 1 (which above says the example used "the firm", its name at the time of the run): the settings now ask for an organization or site name; the example's settings give "Firm A" (invented) and its heading uses it.
- Defects 6 and 7: the format now says headings count copies and each line is one inventory row, and gives "1 copy" or "n copies" and "1 saved file" or "n saved files". The example now prints "2 saved files".
- Defect 3: "inventoried" is defined in the format and under What to customize.
- Defects 2, 4 and 5: notes on withdrawal records matched by location, and on Not yet due copies counting toward an expected number, were added to the format and to What to customize.
- The pasted instructions now carry the ordering rule, the case of a withdrawal record for a document not on the master list, and the singular and plural forms.
- The "Not proven" line now says that copies counted as Current at a location whose inventory is too old are not confirmed as current; the example's line says so for the Quarantine Cage.

A second round of small edits followed a second review, also without a rerun: a printed copy now takes its noun on a line ("1 printed copy", "2 printed copies") in the format, the pasted instructions and the example; the pasted instructions gained the rules for a missing count column and a blank date_checked; the empty Coverage gaps section is made explicit; and two decision questions in the example (the Final Assembly files and the Inspection Bay revision D copy) no longer offer possible explanations. The recorded run above used the wording in force at the time.

The run was not repeated, so these changes are untested. A rerun by a run that has not seen the example is still wanted.

