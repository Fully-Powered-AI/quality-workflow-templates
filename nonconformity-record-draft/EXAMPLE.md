# Nonconformity record draft: an invented example

*Illustrative example with invented data.* The company, the people, the parts, the readings, the lots and the dates below are all invented. The company is an invented 80-person sheet-metal fabrication shop, called Workshop A here. A supervisor on the early shift spots a possible problem on a bracket, and the quality lead runs the capability to prepare the draft record. First come the inputs the quality lead supplied, in full, then the draft the capability returned.

## The inputs

### 1. Settings

```
Today: Tuesday 10 November 2026
Quality owner: the quality lead
Safety role: the operations manager
Look-back for similar records: 90 days
Classification scale: the company's own (Minor, Major, Critical), defined
  in its quality manual. The assistant only names it.
Containment options the company uses:
  1 Hold in place and tag
  2 Move to quarantine cage Q1
  3 Inspect every piece
  4 Inspect a sample from each lot
  5 Pause the machine on this part until checked
  6 Tell the customer about shipped lots
Record numbers: assigned by the quality lead from the nonconformity log
```

### 2. Observation notes (typed by the early-shift supervisor)

```
Tuesday 10 Nov, about 07:45, before the first shift moved lot L-3314 of
Bracket B-220 on from rack 4 in the press area. I picked 5 parts at
random from the 120 on the rack and measured flange height with caliper
CAL-07 (its sticker says calibration due 30 Nov 2026). Readings in mm:
41.2, 41.3, 41.1, 41.4 and 42.0. The parts were made on press brake PB-4
on Monday 9 Nov. The drawing at the press is revision C. I have not
checked the document register. I took photos and wrote the readings on a
sheet. I have not touched the rest of the lot; it is still on rack 4.
I think the tool setting may have drifted, but I have not looked.
I have told nobody except the quality lead.
```

### 3. Requirement (typed by the supervisor from the drawing at the press)

```
Document: DWG-B220, Bracket B-220
Revision: C, dated 2026-08-18 (as printed on the drawing at the press)
Clause: Note 3, flange height
Words: "Flange height 42.0 mm, tolerance plus or minus 0.5 mm."
```

### 4. Work register (exported by the work owner)

```
item_id,description,lot,machine,location,status,quantity,made_date,last_inspection_date,last_inspection_result
B-220,Bracket B-220,L-3310,PB-4,Shipped to Customer 1 on 2026-11-04,Shipped,200,2026-11-03,2026-11-03,Pass
B-220,Bracket B-220,L-3311,PB-4,Shipped to Customer 1 on 2026-11-05,Shipped,100,2026-11-04,,
B-220,Bracket B-220,L-3312,PB-4,Finished goods shelf F2,Finished,150,2026-11-05,,
B-220,Bracket B-220,L-3313,PB-2,Finished goods shelf F3,Finished,150,2026-11-06,2026-11-06,Pass
B-220,Bracket B-220,L-3314,PB-4,Press area rack 4,In process,120,2026-11-09,,
B-220,Bracket B-220,L-3315,PB-4,Press area rack 5,In process,80,2026-11-10,,
B-231,Bracket B-231,L-3320,PB-4,Press area rack 6,In process,60,2026-11-09,,
```

### 5. Evidence list

```
evidence_id,type,description,taken_by,taken_at
E1,photo,Caliper reading 41.2 on part 1 of 5,Early-shift supervisor,2026-11-10 07:50
E2,photo,Rack 4 label showing lot L-3314,Early-shift supervisor,2026-11-10 07:52
E3,measurement sheet,Handwritten readings for the five parts,Early-shift supervisor,2026-11-10 07:55
```

### 6. Nonconformity log (export)

```
record_id,date,item_id,requirement_ref,summary,status
NC-0412,2026-10-21,B-220,DWG-B220 rev C Note 3,Flange height low on 2 parts in lot L-3271,Closed
NC-0431,2026-11-02,B-190,DWG-B190 rev B Note 5,Hole position offset on 1 part in lot L-3290,Open
```

## The output

```
NONCONFORMITY RECORD (DRAFT): Bracket B-220, lot L-3314, flange height
Status: Draft for the quality lead. Suspected, not confirmed. Nothing classified, held, released, sent or recorded.
Record number: To be assigned by the quality lead.
Observed: 2026-11-10, about 07:45, by the early-shift supervisor, at press area rack 4. Prepared 2026-11-10 for the quality lead. Inputs read: the supervisor's notes; DWG-B220 revision C; the work register (seven rows; as-of date not given); the evidence list (three rows); the nonconformity log (two records).
Safety flag: None stated in the notes. This draft is not a safety assessment.

WHAT WAS OBSERVED
O1. Five parts picked at random from the 120 on rack 4 (lot L-3314, Bracket B-220, made on PB-4 on 2026-11-09), measured for flange height with caliper CAL-07, whose sticker shows calibration due 2026-11-30.
O2. Readings in mm: 41.2, 41.3, 41.1, 41.4 and 42.0. Five parts examined of 120.
O3. The drawing at the press is revision C. The supervisor has not checked the document register.
O4. The supervisor took photos and wrote the readings on a sheet.
O5. The rest of the lot has not been touched and is still on rack 4. Nobody has been told except the quality lead.
O6. The supervisor's belief, not an observation: the tool setting may have drifted. The supervisor has not looked.

THE REQUIREMENT
DWG-B220, revision C, dated 2026-08-18, Note 3, flange height: "Flange height 42.0 mm, tolerance plus or minus 0.5 mm." The limits are 41.5 mm and 42.5 mm.
Source of the extract: typed by the early-shift supervisor from the drawing at the press.

OBSERVATION AGAINST THE REQUIREMENT
41.2 mm against a lower limit of 41.5 mm: differs by 0.3 mm (41.5 - 41.2).
41.3 mm against a lower limit of 41.5 mm: differs by 0.2 mm (41.5 - 41.3).
41.1 mm against a lower limit of 41.5 mm: differs by 0.4 mm (41.5 - 41.1).
41.4 mm against a lower limit of 41.5 mm: differs by 0.1 mm (41.5 - 41.4).
42.0 mm against limits of 41.5 mm and 42.5 mm: within the requirement as written.
Summary: 4 of 5 examined differ from the requirement as written; 115 of 120 not examined.

EVIDENCE
E1, photo, caliper reading 41.2 on part 1 of 5, early-shift supervisor, 2026-11-10 07:50
E2, photo, rack 4 label showing lot L-3314, early-shift supervisor, 2026-11-10 07:52
E3, measurement sheet, handwritten readings for the five parts, early-shift supervisor, 2026-11-10 07:55
Not supplied: measurements of the other 115 parts in lot L-3314; a photo of the drawing at the press.

AFFECTED WORK
Observed: B-220, lot L-3314, PB-4, press area rack 4, In process, 120 pieces.
Last known good: B-220, lot L-3310, made 2026-11-03, inspection Pass on 2026-11-03.
Possibly affected, not yet examined:
B-220, lot L-3311, PB-4, Shipped to Customer 1 on 2026-11-05, Shipped, 100 pieces.
B-220, lot L-3312, PB-4, Finished goods shelf F2, Finished, 150 pieces.
B-220, lot L-3315, PB-4, Press area rack 5, In process, 80 pieces.
Basis: lots of the same item on the same machine made after the last lot with a recorded Pass, up to today. This is a search basis, not a finding.
Counts: observed 120; possibly affected 330 (100 + 150 + 80); together 450. By status: Shipped 100; Finished 150; In process 200 (120 observed + 80).
Left out, and why: lot L-3313, 150 pieces, same item but made on PB-2; lot L-3320 of B-231, 60 pieces, same machine but a different item; lot L-3310, 200 pieces, the last known good lot.
Already outside your control per the register: lot L-3311, Shipped to Customer 1 on 2026-11-05, 100 pieces (possibly affected); lot L-3310, Shipped to Customer 1 on 2026-11-04, 200 pieces (the last known good lot, not in the possibly affected set).

SIMILAR RECORDS
NC-0412, 2026-10-21, B-220, DWG-B220 rev C Note 3, flange height low on 2 parts in lot L-3271, Closed.
Records checked: 2 within the last 90 days.

IMMEDIATE CONTAINMENT OPTIONS (NONE DONE)
1 Hold in place and tag: would cover lot L-3314 (120, rack 4), lot L-3315 (80, rack 5) and lot L-3312 (150, shelf F2), 350 pieces. Lot L-3311 (100) has status Shipped per the register.
2 Move to quarantine cage Q1: would cover the same three lots, 350 pieces. No further fact.
3 Inspect every piece: would cover up to 450 pieces across the four lots, 350 of them in the lots on rack 4, rack 5 and shelf F2. Lot L-3311 (100) has status Shipped per the register.
4 Inspect a sample from each lot: would cover lots L-3314, L-3312, L-3315 and L-3311. Lot L-3311 has status Shipped per the register. Five of the 120 pieces in lot L-3314 have been measured already.
5 Pause the machine on this part until checked: would stop PB-4 for B-220. Lot L-3315, 80 pieces, was made on 2026-11-10 and is in process.
6 Tell the customer about shipped lots: would cover lot L-3311 (100 pieces, Customer 1). Nothing has been sent.
No option is recommended.

DECISIONS FOR THE QUALITY LEAD
1. Whether this is a nonconformity and, if so, its classification on the company's own scale (Minor, Major, Critical).
2. Which containment options apply, and to which lots.
3. Whether the closed record NC-0412 (same item, same drawing note) points to a recurrence.
4. Whether Customer 1 must be told about lot L-3311, which has shipped. The draft informs no one.
5. Whether more measurements, or a second reading with another instrument, are needed before the record is accepted.
6. Who owns the record.
7. Whether lot L-3315, made today, is complete: the register does not say, so the 80 pieces may not be its final quantity.

CONFIRM BEFORE RELYING ON THIS
Revision C is the current revision of DWG-B220: check the document register.
Caliper CAL-07 is in calibration: the supervisor reports a due date of 2026-11-30; check the calibration record.

NOT IN THIS DRAFT
Cause and corrective actions: see Incident investigation and corrective actions. Customer complaint: see Complaint and refund request handling. Disposition of the work: for the quality lead.
Prepared for the quality lead. Nothing has been classified, held, released, sent or recorded by the assistant.
Not completed, and what is needed: the current revision of DWG-B220 (document register); the calibration status of CAL-07 (calibration record); measurements of the other 115 parts in lot L-3314, if the quality lead wants them before the record is accepted.
```
