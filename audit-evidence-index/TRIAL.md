# Audit evidence index: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (`claude-sonnet-5-5`)
- **Date:** 2026-11-10

The inputs were the invented example in `public/example.md` (the settings, the eight audit requests, the document register, the twelve records and the three earlier findings). The company, people, documents and records are all invented. No client data was used. The run followed the instruction block and the output format in `member/template.md`, and nothing else in the template.

This is the second run. An earlier run on the same date used the first version of the block; an independent review then found that the block left out rules the procedure depends on (an open linked finding becomes an item to settle; the list of ignored words in the overlap rule; the wording of the items for a possible match and for nothing found; the whole-system exception) and that the format had no wording for a missing location or date or for a records request with no linked document. The block, the format and the example were revised, and this record replaces the first. The first run's observations that led to those changes are listed under "What changed since the first run".

One limit on this trial. I had read the example and the first trial before this run, so it is not a blind test. I worked the output out from the revised block and the inputs, line by line, then compared it with the example. Agreement with the example should be read with that in mind. A blind rerun, by a runner who has not seen the example or this record, would be stronger evidence and is recommended before the template is relied on.

## What came out

```
AUDIT EVIDENCE INDEX: internal audit of the quality system, audit date 24 November 2026

Prepared for: Quality manager. Owners respond by 17 November 2026. Register and records as supplied on 10 November 2026.

Count: 8 requests. Linked 1. Check first 4. Possible match only 1. Nothing found 2. Tie-out: 1 + 4 + 1 + 2 = 8. Records supplied 12: linked 7, not linked 5.

Index

R01: Current quality manual
  Status: Linked
  Document: QM-01, Quality manual, revision C, Effective, effective 3 March 2025, review due 3 March 2027; owner Quality manager
  Records: Not requested
  Prior findings: None
  To settle: Nothing

R02: Document control procedure and the document change requests raised since 1 July 2026
  Status: Check first
  Document: SOP-DC-01, Document control procedure, revision D, Effective, effective 12 January 2026, review due 12 January 2027; owner Quality manager
  Records: None supplied for 1 July 2026 to 10 November 2026
  Prior findings: None
  To settle: 1. Records were requested and none were supplied for 1 July 2026 to 10 November 2026. The Quality manager locates them or confirms none were raised, by 17 November 2026.

R03: Corrective action procedure and the corrective action reports closed in the third quarter of 2026
  Status: Check first
  Document: SOP-CA-02, Corrective action procedure, revision B, Effective, effective 2 June 2025, review due 2 June 2026; owner Quality manager
  Records: CAR-031, Corrective action report: mislabelled batch, 21 July 2026, held at Quality share / CAR / 2026; CAR-034, Corrective action report: late supplier certificate, 18 August 2026, held at Quality share / CAR / 2026
  Prior findings: F-2025-05, Open, action CAR-036
  To settle: 1. Review overdue: the review was due 2 June 2026, before the audit date. The Quality manager confirms the review status by 17 November 2026. 2. Prior finding F-2025-05 is open. The Quality manager settles it by 17 November 2026. The index does not say whether its action worked.

R04: Training and competence records for the new inspector hired in August 2026
  Status: Possible match only
  Document: Candidate, not linked: SOP-TR-04, Training and competence procedure, revision A, Effective, effective 16 September 2024, review due 16 September 2026; owner Training coordinator
  Records: Candidate, not linked: TR-210, Training record: new inspector, 24 August 2026, held at Training office / Files
  Prior findings: None
  To settle: 1. The request names no document. The Quality manager confirms by 17 November 2026 whether SOP-TR-04 and TR-210 are what was meant.

R05: Calibration records for the gauges used in final inspection from January to October 2026
  Status: Check first
  Document: WI-CAL-07, Gauge calibration work instruction, revision E, In review, effective date not recorded, review due date not recorded; owner Maintenance lead
  Records: CAL-118, Gauge calibration record: height gauge, 9 February 2026, held at Maintenance office / CAL binder; CAL-131, Gauge calibration record: micrometer set, 15 June 2026, held at Maintenance office / CAL binder; CAL-140, Gauge calibration record: bore gauge, 28 September 2026, location not recorded
  Prior findings: F-2025-03, Closed, action CAR-029
  To settle: 1. Not in force: the register status is In review. The revision comparison was skipped because the document is not in force. The Maintenance lead tells the Quality manager which revision applies, by 17 November 2026. 2. No location: CAL-140 has none. The Maintenance lead supplies it by 17 November 2026.

R06: Supplier approval procedure and the supplier evaluations completed in 2026
  Status: Check first
  Document: SOP-PU-03, Supplier approval procedure, revision B, Effective, effective 17 November 2025, review due 17 November 2027; owner not assigned
  Records: SUP-EV-12, Supplier evaluation: Supplier A, 10 March 2026, held at Purchasing share / Evaluations; SUP-EV-19, Supplier evaluation: Supplier C, 2 September 2026, held at Purchasing share / Evaluations
  Prior findings: None
  To settle: 1. No owner: the register shows none for SOP-PU-03. The Quality manager names one by 17 November 2026. 2. Revision mismatch: SUP-EV-19, dated 2 September 2026, cites revision A; the register shows revision B, effective since 17 November 2025. With no owner, the Quality manager asks for or gives an explanation by 17 November 2026.

R07: Evidence of management review meetings held in 2026
  Status: Nothing found
  Document: None found
  Records: None linked: no document linked
  Prior findings: None
  To settle: 1. Nothing in the register matched this request. The Quality manager says what document or records are meant, by 17 November 2026.

R08: Control of nonconforming product procedure
  Status: Nothing found
  Document: None found; reference SOP-NC-05 is not in the register
  Records: Not requested
  Prior findings: None
  To settle: 1. The reference SOP-NC-05 is not in the register. The Quality manager confirms whether the document exists, by 17 November 2026.

Supplied but not linked to any request: CAR-029 (outside the period of R03, before 1 July 2026); CAR-036 (outside the period of R03, after 30 September 2026); CAL-099 (outside the period of R05, before 1 January 2026); TR-188 (outside the period of R04, and its document is a candidate only); TR-210 (candidate for R04 only, not linked).

Prior findings not linked to any request: F-2025-07, Open, Management review minutes could not be produced; action not recorded.

Decisions for the quality owner
1. Possible matches to confirm: R04.
2. Requests with nothing found: R07, R08.
3. Prior findings to link to a request: F-2025-07.
4. What is shared with the auditors, in what form and when.

This index, built from the lists supplied for the internal audit of the quality system, shows where each item is held and what the register says about its revision. It does not show that a document's content is right, that a record proves the procedure worked, or that anything is ready for audit. The auditors judge the evidence themselves. The index changes no records and sends nothing.
```

## What was observed

- **Every required part was produced:** the heading, the prepared-for line, the count line with the tie-out, one block per request in order, the unlinked records, the unlinked findings, the four decisions and the closing paragraph. The tie-out adds up (1 + 4 + 1 + 2 = 8) and the records add up (7 + 5 = 12).
- **Nothing made the run stop.** All headers matched, no id was repeated, and the audit date was given. Nothing in the inputs asked for a judgment of readiness, so the decline rule was not exercised, and no request was a whole-system request.
- **The block alone was enough for each earlier gap.** Working from the block, R03 kept its second item (the open finding F-2025-05); "inspector" and "inspection" were not matched, because the block says whole words; titles sharing only "procedure" plus one other word were not candidates; R04 asked the quality owner to confirm the candidate; R07 and R08 named the quality owner; R07's Records line read "None linked: no document linked"; and R05's missing location and dates used the block's wording.
- **Against the example, the statuses, counts, links, flags, dates and the unlinked lists are the same.** The differences are in wording only: how the items to settle are phrased (my run opens R03, R05 and R06 items with the name of the flag, and the example does not), and the reasons given in the unlinked list. Both name a single person for each item and the hand-off date.
- **Facts not in the inputs:** none in my output. I checked every date, id and location against the inputs and found no invented one.
- **Remaining places where two careful readers could differ:**
  1. A record that is outside a period and belongs to a candidate document only (TR-188) has two possible reasons in the unlinked list. The template does not say which comes first; my run gave the period first.
  2. R03 asks for reports "closed in the third quarter". The records list has only a `record_date`; I treated it as the date to test against the period, which the template now says under "What to customize".
  3. "Prepared for" takes the quality owner's role from the settings (a role, not a person). The template does not say what to print if the settings name a person.
  4. It is not stated whether a record linked to two requests counts once in "linked". I assumed once.
- **What the first run showed that the example got wrong.** The example had named a person with no standing to act on SOP-PU-03 (a document with a blank owner) and had mixed a revision comparison into a document the template says to skip. Both were fixed in the example, so on this run the example and the template agree.
- This is one further run, by one model, on an invented example, by an assistant that had already seen the published output. It is not a test in a client environment and says nothing about how the template performs on real audit lists.

## Settled after this run

A later independent review closed the four open points above in the template, without changing this recorded output: the period reason comes first for a record that is both outside the period and on a candidate document; "Prepared for" prints the quality owner setting exactly as given; a record linked to two requests counts once as linked; and the period is always tested on the record date. It also defined the ignored small words as words of three letters or fewer and added the rules for a missing records list or findings list. The template was not run again after these edits, so this record is of the run before them; none of them changes anything in the output above.

## What changed since the first run

From the first run: the block gained the open-finding rule, the ignored-words list, the whole-word rule, the items for Possible match only and Nothing found, and the whole-system exception; the format gained "location not recorded", "date not recorded" and "None linked: no document linked"; and the example's R04, R05, R06, R07 and R08 items were reworded. The first run's output is not kept, because this run replaces it.
