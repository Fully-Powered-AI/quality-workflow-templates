# Quality management review pack: an invented example

*Illustrative example with invented data.* The company, the people, the records and every figure below are invented. The company is an invented 140-person maker of metal enclosures and brackets, with a quality lead who reports to an operations director and a managing director. First come the inputs the quality lead supplied, in full, then the brief the capability returned.

## The inputs

### 1. Review settings

```
Company: Quill Harbour Components (invented)
Review: quarterly quality management review
Period covered: 2026-07 to 2026-09
Previous review: 2026-07-08
Review meeting: 2026-10-14
Pack date: 2026-10-07 (all ages and overdue counts run to this date)
Level band: 1% of the average of the three periods before the latest
Aged record: an open complaint or defect older than 30 days
Leaders: Managing director, Operations director
Decision rights: Resources and further actions: Operations director.
  Targets and definitions: Managing director.
```

### 2. Measure sheet

```
measure_id,measure,unit,direction,target,owner
M1,First-pass yield,percent,higher_is_better,96.0,Production manager
M2,Customer complaints per 1000 units shipped,rate,lower_is_better,2.0,Quality lead
M3,Corrective actions closed by original due date,percent,higher_is_better,90.0,Quality lead
M4,Supplier incoming rejection rate,percent,lower_is_better,1.5,Purchasing lead
```

### 3. Measure results (export)

```
measure_id,period,value,definition_version
M1,2026-04,95.1,v1
M1,2026-05,95.6,v1
M1,2026-06,96.2,v1
M1,2026-07,95.8,v1
M1,2026-08,95.0,v1
M1,2026-09,94.2,v1
M2,2026-04,1.8,v1
M2,2026-05,2.1,v1
M2,2026-06,1.9,v1
M2,2026-07,2.2,v1
M2,2026-08,1.7,v1
M2,2026-09,1.5,v1
M3,2026-04,82.0,v1
M3,2026-05,85.0,v1
M3,2026-06,88.0,v1
M3,2026-07,91.0,v1
M3,2026-08,78.0,v2
M3,2026-09,80.0,v2
M4,2026-04,1.4,v1
M4,2026-05,1.6,v1
M4,2026-06,1.3,v1
M4,2026-07,1.7,v1
M4,2026-08,1.6,v1
```

### 4. Complaints and defects (export)

```
record_id,date,type,category,product_or_process,severity,status,closed_date
C-201,2026-07-06,complaint,Finish,Enclosure line,minor,closed,2026-07-20
C-202,2026-07-14,complaint,Dimensional,Enclosure line,major,closed,2026-08-11
D-118,2026-07-21,defect,Dimensional,Bracket line,minor,closed,2026-07-30
D-119,2026-07-28,defect,Finish,Enclosure line,minor,closed,2026-08-04
C-203,2026-08-04,complaint,Packaging,Despatch,minor,closed,2026-08-12
D-120,2026-08-11,defect,Dimensional,Bracket line,major,closed,2026-09-01
D-121,2026-08-18,defect,Dimensional,Bracket line,minor,open,
C-204,2026-08-25,complaint,Dimensional,Enclosure line,minor,open,
D-122,2026-09-02,defect,Dimensional,Bracket line,major,open,
D-123,2026-09-09,defect,Finish,Enclosure line,minor,closed,2026-09-16
C-205,2026-09-15,complaint,Documentation,Despatch,minor,closed,2026-09-22
D-124,2026-09-17,defect,Dimensional,Bracket line,minor,open,
C-206,2026-09-23,complaint,Finish,Enclosure line,minor,open,
D-125,2026-09-29,defect,Dimensional,Bracket line,minor,open,
```

### 5. Audit results

```
audit_id,audit_date,scope,finding_id,finding_type,area,description,status,due_date
A-2026-02,2026-08-18,Internal audit of the bracket line,F-01,major,Process control,Dimensional check frequency not followed on two shifts,open,2026-09-30
A-2026-02,2026-08-18,Internal audit of the bracket line,F-02,minor,Records,Two inspection sheets unsigned,closed,2026-09-15
A-2026-02,2026-08-18,Internal audit of the bracket line,F-03,observation,Housekeeping,Gauge storage cabinet not labelled,open,
A-2026-03,2026-09-22,Supplier approval review,F-04,minor,Supplier records,Two supplier approvals past their review date,open,2026-10-30
A-2026-03,2026-09-22,Supplier approval review,F-05,minor,Supplier records,No incoming inspection plan for one part family,open,2026-11-15
```

### 6. Action register

```
action_id,source,description,owner,due_date,status,done_date,evidence_ref,linked_to
AC-31,Previous review,Add a second gauge to the bracket line,Production manager,2026-08-31,done,2026-08-28,PO-4471,M1
AC-32,Previous review,Rewrite the closure reminder for corrective actions,Quality lead,2026-08-15,done,2026-08-14,,M3
AC-33,Previous review,Agree supplier rejection reporting with purchasing,Purchasing lead,2026-09-15,open,,,M4
AC-34,Audit A-2026-02,Retrain both shifts on dimensional check frequency,Production manager,2026-09-30,open,,,F-01
AC-35,Audit A-2026-02,Label the gauge storage cabinet,Maintenance lead,2026-10-31,open,,,F-03
AC-36,Audit A-2026-03,Review the two supplier approvals,Purchasing lead,2026-10-30,open,,,F-04
AC-37,Complaint C-202,Add a customer-side check to despatch,Despatch lead,2026-08-31,done,2026-09-05,,C-202
AC-38,Previous review,Report the on-time closure definition change to the leaders,Quality lead,2026-08-31,done,2026-08-31,MR-0708-note,M3
```

### 7. Decisions from the previous review

```
decision_id,review_date,decision,decision_owner,due_date,status
D-MR-1,2026-07-08,Fund a second gauge for the bracket line,Operations director,2026-07-31,done
D-MR-2,2026-07-08,Decide whether purchasing reports supplier rejection data monthly,Operations director,2026-08-31,open
D-MR-3,2026-07-08,Decide whether the on-time closure measure counts against the original due date,Managing director,2026-07-31,done
```

### 8. Owner notes (typed by the owners)

```
Production manager: September yield dropped after we changed the bracket
material lot on 14 September. We need two weeks of overtime for a re-sort
of stock, about 120 hours. I need a yes or no on that.
Purchasing lead: The September supplier rejection figures are not in. The
supplier portal export failed. I expect them by 14 October.
```

## The output

**QUALITY MANAGEMENT REVIEW PACK: Quill Harbour Components, 2026-07 to 2026-09**

**For:** Managing director, Operations director. Review meeting 2026-10-14. Pack date 2026-10-07; every age and overdue count runs to that date. Previous review 2026-07-08.

**Inputs:** review settings, measure sheet, measure results, complaints and defects, audit results, action register, decisions from the previous review, owner notes: all supplied. Settings taken from defaults: none.

**This pack asserts no conformity with any standard or requirement. Managing director and Operations director decide.**

**1. Measures**

- **M1 First-pass yield** (percent, higher is better; owner Production manager). Latest 2026-09: 94.2; target 96.0: not met. Trend: Worse than the average of 2026-06 to 2026-08, 95.67 (−1.47). Not met in 3 periods in a row. Owner's account: "September yield dropped after we changed the bracket material lot on 14 September."
- **M2 Customer complaints per 1000 units shipped** (rate, lower is better; owner Quality lead). Latest 2026-09: 1.5; target 2.0: met. Trend: Better than the average of 2026-06 to 2026-08, 1.93 (−0.43). Owner's account: none supplied.
- **M3 Corrective actions closed by original due date** (percent, higher is better; owner Quality lead). Latest 2026-09: 80.0; target 90.0: not met. Trend not shown: the definition changed from v1 to v2 in 2026-08, and 2 periods sit on the current definition. Not met in 2 periods in a row. Owner's account: none supplied.
- **M4 Supplier incoming rejection rate** (percent, lower is better; owner Purchasing lead). Latest 2026-09: not reported. Last reported 2026-08: 1.6; target 1.5: not met. Not met in 2 periods in a row, counted to 2026-08. Owner's account: "The September supplier rejection figures are not in. The supplier portal export failed. I expect them by 14 October."

**2. Complaints and defects**

- **Records:** 14 in 2026-07 to 2026-09: 2026-07 4, 2026-08 4, 2026-09 6.
- **By category:** Dimensional 8 (2026-07 2, 2026-08 3, 2026-09 3). Finish 4 (2026-07 2, 2026-08 0, 2026-09 2). Packaging 1 (2026-07 0, 2026-08 1, 2026-09 0). Documentation 1 (2026-07 0, 2026-08 0, 2026-09 1).
- **Open at the pack date:** 6 (1 major). Open longer than 30 days: D-121, Dimensional, minor, 50 days. C-204, Dimensional, minor, 43 days. D-122, Dimensional, major, 35 days.

**3. Audit findings**

- **Audits in the period:** 2. A-2026-02, 2026-08-18, Internal audit of the bracket line. A-2026-03, 2026-09-22, Supplier approval review.
- **Findings:** 5: major 1, minor 3, observation 1. Open 4, closed 1.
- **Overdue:** F-01, major, 2026-09-30, 7 days.
- **Open findings:** F-01, major, Process control, due 2026-09-30, action AC-34. F-03, observation, Housekeeping, no due date, action AC-35. F-04, minor, Supplier records, due 2026-10-30, action AC-36. F-05, minor, Supplier records, due 2026-11-15, no action linked.

**4. Action status**

- **Actions:** 8: done 4, open 4.
- **Done late:** AC-37, due 2026-08-31, done 2026-09-05, 5 days.
- **Done with no evidence listed:** AC-32, AC-37.
- **Open and overdue:** AC-33, Purchasing lead, due 2026-09-15, 22 days. AC-34, Production manager, due 2026-09-30, 7 days.
- **Open, not yet due:** AC-35, Maintenance lead, due 2026-10-31. AC-36, Purchasing lead, due 2026-10-30.
- "Done" is the owner's report that the work was finished. It does not show that the action worked.

**5. Decisions from the previous review**

- **3 decisions made on 2026-07-08:** settled 2, not settled 1.
- **D-MR-2,** Decide whether purchasing reports supplier rejection data monthly. Operations director. Due 2026-08-31. Open, 37 days overdue.

**6. Gaps and changes**

- M4 has no figure for 2026-09.
- M3 changed definition from v1 to v2 in 2026-08; v1 values are not compared with v2 values.
- F-05 is open and has no action linked.
- AC-32 and AC-37 are marked done with no evidence listed.

**7. Decisions still open: 6**

1. **Previous decision not settled.** D-MR-2 (decide whether purchasing reports supplier rejection data monthly) was due 2026-08-31 and is open, 37 days overdue. Is it settled at this meeting? Decides: Operations director.
2. **Request for resources.** The Production manager writes: "We need two weeks of overtime for a re-sort of stock, about 120 hours. I need a yes or no on that." Is the request approved? Decides: Operations director.
3. **Measure not met, no open action.** M1 is 94.2 against 96.0. Its linked action AC-31 is done; no open action is linked to it. Is any further action wanted? Decides: Operations director.
4. **Measure not met, no open action.** M3 is 80.0 against 90.0 on the current definition. Its linked actions AC-32 and AC-38 are done; no open action is linked to it. Is any further action wanted? Decides: Operations director.
5. **Finding to settle.** F-01 (major, Process control) was due 2026-09-30 and is open, 7 days overdue. Its linked action AC-34 is open, 7 days overdue. What is needed to close it? Decides: Operations director.
6. **Overdue action.** AC-33 (agree supplier rejection reporting with purchasing), linked to M4, was due 2026-09-15 and is open, 22 days overdue, with the Purchasing lead. Is the date extended or is the action escalated? Decides: Operations director.

Every figure traces to the measure results, the complaints and defects export, the audit results, the action register and the decisions list supplied, as of 2026-10-07. The pack asserts no conformity with any standard, changes no record and sends nothing.
