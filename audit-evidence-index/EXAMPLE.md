# Audit evidence index: an invented example

*Illustrative example with invented data.* The company, the people, the documents, the records and the dates below are all invented. The company is an invented 80-person precision-parts manufacturer preparing for an internal audit of its quality system. In this example the quality manager is both the quality lead who runs the capability and the quality owner who reviews the index. First come the inputs the quality manager supplied, in full, then the index the capability returned.

## The inputs

### 1. Audit settings

```
Audit: internal audit of the quality system
Audit date: Tuesday 24 November 2026
Today: Tuesday 10 November 2026
Lead time: 7 calendar days before the audit date
Quality owner: Quality manager
In force means register status "Effective"
A blank owner means not assigned
```

### 2. Audit request list

```
request_id,request_text,asks_for,reference,period_from,period_to
R01,Current quality manual,document,QM-01,,
R02,Document control procedure and the document change requests raised since 1 July 2026,both,SOP-DC-01,2026-07-01,2026-11-10
R03,Corrective action procedure and the corrective action reports closed in the third quarter of 2026,both,SOP-CA-02,2026-07-01,2026-09-30
R04,Training and competence records for the new inspector hired in August 2026,records,,2026-08-01,2026-10-31
R05,Calibration records for the gauges used in final inspection from January to October 2026,records,WI-CAL-07,2026-01-01,2026-10-31
R06,Supplier approval procedure and the supplier evaluations completed in 2026,both,SOP-PU-03,2026-01-01,2026-10-31
R07,Evidence of management review meetings held in 2026,records,,2026-01-01,2026-10-31
R08,Control of nonconforming product procedure,document,SOP-NC-05,,
```

### 3. Document register

```
doc_id,title,revision,status,effective_date,owner,next_review_date
QM-01,Quality manual,C,Effective,2025-03-03,Quality manager,2027-03-03
SOP-DC-01,Document control procedure,D,Effective,2026-01-12,Quality manager,2027-01-12
SOP-CA-02,Corrective action procedure,B,Effective,2025-06-02,Quality manager,2026-06-02
SOP-TR-04,Training and competence procedure,A,Effective,2024-09-16,Training coordinator,2026-09-16
WI-CAL-07,Gauge calibration work instruction,E,In review,,Maintenance lead,
SOP-PU-03,Supplier approval procedure,B,Effective,2025-11-17,,2027-11-17
WI-INS-11,Incoming inspection work instruction,C,Effective,2026-05-04,Receiving supervisor,2027-05-04
```

### 4. Records selected for the audit

```
record_id,title,doc_id,procedure_revision,record_date,location
CAR-029,Corrective action report: superseded work instruction at the bench,SOP-CA-02,B,2026-06-27,Quality share / CAR / 2026
CAR-031,Corrective action report: mislabelled batch,SOP-CA-02,B,2026-07-21,Quality share / CAR / 2026
CAR-034,Corrective action report: late supplier certificate,SOP-CA-02,B,2026-08-18,Quality share / CAR / 2026
CAR-036,Corrective action report: damaged packaging,SOP-CA-02,B,2026-10-05,Quality share / CAR / 2026
CAL-099,Gauge calibration record: bore gauge,WI-CAL-07,D,2025-12-11,Maintenance office / CAL binder
CAL-118,Gauge calibration record: height gauge,WI-CAL-07,D,2026-02-09,Maintenance office / CAL binder
CAL-131,Gauge calibration record: micrometer set,WI-CAL-07,D,2026-06-15,Maintenance office / CAL binder
CAL-140,Gauge calibration record: bore gauge,WI-CAL-07,D,2026-09-28,
SUP-EV-12,Supplier evaluation: Supplier A,SOP-PU-03,B,2026-03-10,Purchasing share / Evaluations
SUP-EV-19,Supplier evaluation: Supplier C,SOP-PU-03,A,2026-09-02,Purchasing share / Evaluations
TR-188,Training record: machine operator,SOP-TR-04,A,2026-02-02,Training office / Files
TR-210,Training record: new inspector,SOP-TR-04,A,2026-08-24,Training office / Files
```

### 5. Last cycle's findings

```
finding_id,finding_text,related_ref,status,action_ref
F-2025-03,Superseded work instruction found at the inspection bench,WI-CAL-07,Closed,CAR-029
F-2025-05,Corrective actions closed without a recorded effectiveness check,SOP-CA-02,Open,CAR-036
F-2025-07,Management review minutes could not be produced,,Open,
```

## The index

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
  To settle: 1. No document change request was supplied for 1 July 2026 to 10 November 2026. The Quality manager locates them or confirms none were raised, by 17 November 2026.

R03: Corrective action procedure and the corrective action reports closed in the third quarter of 2026
  Status: Check first
  Document: SOP-CA-02, Corrective action procedure, revision B, Effective, effective 2 June 2025, review due 2 June 2026; owner Quality manager
  Records: CAR-031, Corrective action report: mislabelled batch, 21 July 2026, held at Quality share / CAR / 2026; CAR-034, Corrective action report: late supplier certificate, 18 August 2026, held at Quality share / CAR / 2026
  Prior findings: F-2025-05, Open, action CAR-036
  To settle: 1. The review due date, 2 June 2026, is before the audit date. The Quality manager confirms the review status by 17 November 2026. 2. Prior finding F-2025-05 is open; the index does not show whether its action worked. The Quality manager confirms its status by 17 November 2026.

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
  To settle: 1. The register status is In review, not Effective. The revision comparison was skipped because the document is not in force. The Maintenance lead tells the Quality manager which revision applies, by 17 November 2026. 2. CAL-140 has no location. The Maintenance lead supplies it by 17 November 2026.

R06: Supplier approval procedure and the supplier evaluations completed in 2026
  Status: Check first
  Document: SOP-PU-03, Supplier approval procedure, revision B, Effective, effective 17 November 2025, review due 17 November 2027; owner not assigned
  Records: SUP-EV-12, Supplier evaluation: Supplier A, 10 March 2026, held at Purchasing share / Evaluations; SUP-EV-19, Supplier evaluation: Supplier C, 2 September 2026, held at Purchasing share / Evaluations
  Prior findings: None
  To settle: 1. No owner is assigned to SOP-PU-03. The Quality manager names one by 17 November 2026. 2. SUP-EV-19, dated 2 September 2026, cites revision A; revision B has been effective since 17 November 2025. With no owner assigned, the Quality manager asks for or gives the explanation by 17 November 2026.

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
  To settle: 1. SOP-NC-05 is not in the register. The Quality manager confirms whether the document exists, by 17 November 2026.

Supplied but not linked to any request: CAR-029 (dated before the 1 July 2026 start of R03); CAR-036 (dated after the 30 September 2026 end of R03); CAL-099 (dated before the 1 January 2026 start of R05); TR-188 (dated before the 1 August 2026 start of R04, and candidate document only); TR-210 (candidate for R04, not linked until confirmed).

Prior findings not linked to any request: F-2025-07, Open, Management review minutes could not be produced; action not recorded.

Decisions for the quality owner
1. Possible matches to confirm: R04.
2. Requests with nothing found: R07, R08.
3. Prior findings to link to a request: F-2025-07.
4. What is shared with the auditors, in what form and when.

This index, built from the lists supplied for the internal audit of the quality system, shows where each item is held and what the register says about its revision. It does not show that a document's content is right, that a record proves the procedure worked, or that anything is ready for audit. The auditors judge the evidence themselves. The index changes no records and sends nothing.
```

Every entry traces to the five inputs above. The hand-off date is 7 days before 24 November 2026. The tie-out is 1 + 4 + 1 + 2 = 8 requests, and 7 + 5 = 12 records. The candidate SOP-TR-04 has a review date, 16 September 2026, that is before the audit date, and R04 raises no flag for it: only linked documents and records are flagged, and a candidate is not linked until the quality manager confirms it.
