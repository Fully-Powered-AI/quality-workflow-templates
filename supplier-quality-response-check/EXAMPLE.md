# Supplier quality response check: an invented example

*Illustrative example with invented data.* The companies, the finding, the reply, the lots and every figure below are invented. Company K is an invented maker of insulated steel flasks. Supplier B, also invented, moulds the screw lids with silicone seals that Company K buys. Company K's supplier-quality owner raised a finding about leaking lids and has received Supplier B's reply. A quality technician prepares the check for the owner, who decides whether the answer is accepted. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The check follows.

## The inputs

### 1. The settings

```
Today: Tuesday 10 November 2026
Working days: Monday to Friday
Closed dates: none between 27 October and 20 November 2026
Owner who decides: supplier-quality owner, Company K
Next scheduled delivery from Supplier B: Tuesday 17 November 2026
```

### 2. The approved finding

```
Finding ref: QF-26-014
Status: Approved by the supplier-quality owner on 27 October 2026
Supplier: Supplier B
Item: LID-07 screw lid with silicone seal
Requirement: Spec LID-07 revision C, clause 4.2: no leakage during a
  10-minute inverted hold of a filled flask.
Raised: Tuesday 27 October 2026
Reply due: Tuesday 3 November 2026
Found: Incoming inspection of lot L-8831 found seal leakage.
Sample and failures: 200 lids sampled from L-8831; 14 failed the
  inverted hold.
Cavity marks on the 14 failed lids: cavity 6: 11; cavity 3: 2; not
  readable: 1.
Lots in scope:
  - L-8831: 4,000 lids, received at Company K on 20 October 2026,
    moulding run R-1016.
  - L-8834: 1,200 lids, shipped by Supplier B on 30 October 2026, in
    transit, moulding run R-1016.
  - Stock held at Supplier B from run R-1016: quantity not known to
    Company K.
Requested of the supplier:
  R1. Contain: confirm the quantity held at Supplier B and the quantity
      in transit or at Company K from run R-1016.
  R2. Cause: state the cause, with evidence.
  R3. Lot L-8831: propose how the lids not sampled will be sorted or
      replaced, and replace the failed lids.
  R4. Corrective action: state the corrective actions, with owners and
      dates.
  R5. Effectiveness: show leak-test results for the next three lots
      shipped.
Verification criteria:
  R1: hold confirmed by a count and a hold record.
  R5: each of the next three lots shipped passes the inverted hold with
      no failures in a sample of 200 tested by Company K.
  R2, R3, R4: none stated.
```

### 3. The supplier's reply

```
Received: Thursday 5 November 2026, from the quality manager, Supplier B

Thank you for the report on lot L-8831.

We have put 1,800 lids from run R-1016 on hold in our warehouse. The
cause is a worn seal groove in the mould for cavity 6, which let the
seal seat unevenly (photo attached). Our tooling lead will replace the
cavity 6 mould insert by 20 November 2026. Our production manager will
add a seal groove check to the start-of-shift checklist from 16
November 2026 (draft attached). We have sorted the remaining stock and
found no further defects. We will replace the 14 failed lids at our
cost.

Regards,
Quality manager, Supplier B
```

### 4. The attachments list

```
attachment_ref,description,date
A1,Photo of the cavity 6 mould insert showing the seal groove,2026-11-05
A2,Draft start-of-shift checklist with a new line "seal groove check",2026-11-05
```

### 5. The agreed quality responsibilities

```
Supplier B replies within 5 working days of an approved finding.
A reply covers containment, cause, correction, corrective action with
owners and dates, and evidence.
Company K verifies effectiveness.
Escalation route: none stated.
```

## The check

```
SUPPLIER QUALITY RESPONSE CHECK: QF-26-014, Supplier B

For: Supplier-quality owner, Company K. Prepared Tuesday 10 November 2026 from the finding, the reply and the records supplied.

Inputs checked: finding QF-26-014, approved 27 October 2026; reply received 5 November 2026 from the quality manager, Supplier B; 2 attachments listed; reply period 5 working days (counted from 28 October 2026, the working day after the date raised, it ends on 3 November 2026, which agrees with the finding's due date); next scheduled delivery 17 November 2026; escalation route none stated. The cavity marks add up: 11 + 2 + 1 = 14 failed lids, as stated.
Timeliness: reply due Tuesday 3 November 2026, received Thursday 5 November 2026, 2 working days late.

1. EACH REQUEST AGAINST THE REPLY
R1. Contain: confirm the quantity held at Supplier B and the quantity in transit or at Company K from run R-1016.
  Reply: S1 says 1,800 lids from run R-1016 are on hold in the Supplier B warehouse.
  Status: Addressed in part. Left out: the quantity in transit (L-8834) and the quantity at Company K (L-8831). No count or hold record supplied.
  Evidence supplied: none.
R2. Cause: state the cause, with evidence.
  Reply: S2 gives a worn seal groove in the cavity 6 mould as the cause.
  Status: Addressed in full. A cause is stated and A1 is attached. (What the cause leaves unexplained is in D1; this status does not say the cause is accepted.)
  Evidence supplied: A1.
R3. Lot L-8831: propose how the lids not sampled will be sorted or replaced, and replace the failed lids.
  Reply: S7 says the 14 failed lids will be replaced at Supplier B's cost. S5 and S6 say the remaining stock was sorted with no further defects found (D3).
  Status: Addressed in part. Left out: a proposal that names the 3,800 lids of L-8831 not sampled (4,000 less the 200 sampled from L-8831), and a date for the replacement lids.
  Evidence supplied: none.
R4. Corrective action: state the corrective actions, with owners and dates.
  Reply: S3 (tooling lead, by 20 November 2026) and S4 (production manager, from 16 November 2026).
  Status: Addressed in full. Each action has an owner and a date.
  Evidence supplied: A2 (a draft, not a record of the check in use).
R5. Effectiveness: show leak-test results for the next three lots shipped.
  Reply: nothing.
  Status: Not addressed.
  Evidence supplied: none.
Count: 5 requests: 2 addressed in full, 2 in part, 1 not addressed, 0 disputed.

2. WHERE THE REPLY DIFFERS FROM OUR RECORDS OR IS UNCLEAR
D1. Differs. The finding records the cavity marks on the 14 failed lids as cavity 6: 11, cavity 3: 2, not readable: 1. S2 names cavity 6 only, so the cause leaves 2 failed lids (cavity 3) and 1 lid (mark not readable) unexplained.
D2. Not mentioned. L-8834 (1,200 lids, shipped 30 October 2026, run R-1016) is in scope in the finding. The reply does not mention it. L-8831 appears only in the opening thanks; the reply says nothing about its lids beyond the 14 failed.
D3. Unclear. S5 says "the remaining stock" was sorted and S6 says no further defects were found. The reply does not say which stock, how many lids or what method, and no sort record is attached.
D4. Unclear. S1 gives 1,800 lids on hold with no date of the hold, no person and no count record, and does not say whether the 1,800 includes or excludes L-8831 and L-8834. The finding states that the quantity at Supplier B is not known to Company K, so there is no record to set 1,800 against.
D5. Timing. S3 is dated 20 November 2026, 3 days after the next scheduled delivery on 17 November 2026. S4 is dated 16 November 2026, 1 day before that delivery, and is supported only by a draft (A2). S7 has no date, so it cannot be set against the delivery.
D6. Not in the finding. S7 offers replacement "at our cost". The finding does not address cost. Listed only; no view is given.

3. ACTIONS PROPOSED
S1. Put 1,800 lids from run R-1016 on hold in the warehouse. By: not named. When: no date. State: Reported done, no evidence.
S3. Replace the cavity 6 mould insert. By: tooling lead. When: by 20 November 2026. State: Promised.
S4. Add a seal groove check to the start-of-shift checklist. By: production manager. When: from 16 November 2026. State: Promised. A2 is a draft and does not show the check in use.
S5. Sort the remaining stock. By: not named. When: no date. State: Reported done, no evidence.
S7. Replace the 14 failed lids at Supplier B's cost. By: not named. When: no date. State: Promised.
Count: 5 actions: 3 promised, 2 reported done with no evidence, 0 reported done with evidence supplied.
Not actions: S2 (statement of cause); S6 (other: a result reported, "no further defects").

4. ATTACHMENTS AND EVIDENCE TO ASK FOR
Received:
A1. Photo of the cavity 6 mould insert showing the seal groove (2026-11-05). Supports: S2, as a picture of the groove in cavity 6. Does not show: any link to the failed lids, or anything about cavity 3.
A2. Draft start-of-shift checklist with a new line "seal groove check" (2026-11-05). Supports: S4, as a plan. Does not show: that the check is in use.
Evidence to ask for:
E1. The count and the hold record behind S1, and the position of L-8834 and L-8831. For R1 and S1. Why: the reply does not mention L-8834 and gives no record (D2, D4).
E2. What accounts for the 2 failed lids from cavity 3 and the 1 lid with no readable mark. For R2 and S2. Why: S2 names cavity 6 only (D1).
E3. The sort record behind S5 and S6: which stock, how many lids, the method and the results. For R3, S5 and S6. Why: "the remaining stock" is not defined (D3).
E4. Supplier B's proposal for the lids of L-8831 not sampled. For R3. Why: the reply covers only the 14 failed lids.
E5. The date and the person for the replacement of the 14 lids. For R3 and S7. Why: S7 has no date or owner (D5).
E6. A record of the insert replaced and the completed start-of-shift checklists once the check is in use. For R4, S3 and S4. Why: both are promised, and A2 is a draft (D5).
E7. Leak-test results for each of the next three lots shipped. For R5. Why: R5 is not addressed.

5. STILL TO BE VERIFIED
V1. R1: the held quantity, seen by count and hold record. Criterion: hold confirmed by a count and a hold record. Earliest check: now.
V2. R3: the replacement of the 14 failed lids and the handling of the lids not sampled, seen on receipt. Criterion: not stated; owner to set. Earliest check: no date given.
V3. R4: the insert replaced and the groove check in use. Criterion: not stated; owner to set. Earliest check: 16 November 2026 for S4; 20 November 2026 for S3.
V4. R5: each of the next three lots shipped, tested by Company K. Criterion: each of the next three lots shipped passes the inverted hold with no failures in a sample of 200 tested by Company K. Earliest check: no date given.

6. FOR THE OWNER
Open: 3 of 5 requests are not addressed in full; 5 actions proposed, none verified by this check.
Questions:
1. Does a cause that covers cavity 6 (11 of the 14 failed lids) satisfy the finding, given that 2 lids carry cavity 3 and 1 is not readable? (D1, E2)
2. What is the position of L-8834 (1,200 lids, shipped 30 October 2026), and of the lids of L-8831 at Company K? (D2, E1)
3. Which stock do S5 and S6 refer to, and how many lids? (D3, E3)
4. What is the date, quantity and record of the hold in S1, and does the 1,800 include L-8831 and L-8834? (D4, E1)
5. Does the delivery due 17 November 2026 count toward the next three lots in R5, and is it to be inspected, given that S3 is dated 20 November 2026 and S4 rests on a draft? (D5, V4)
6. S7 offers replacement at Supplier B's cost, which the finding does not address. Who in the company deals with that? (D6)
7. What is to happen to the 3,800 lids of L-8831 that were not sampled? (R3, E4)
8. When are the leak-test results in R5 expected? (R5, E7)
Options, none recommended: (a) accept the response as it stands; (b) accept the actions proposed and keep the finding open until they are verified; (c) ask the supplier for the evidence in E1 to E7; (d) escalate by the route in the agreed responsibilities (none stated).

This check compares the reply with the finding and the records supplied. It does not accept the reply, close the finding, verify any action, or write to the supplier. The supplier-quality owner decides, and nothing has been sent or changed.
```
