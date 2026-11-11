# Cost of poor quality worksheet: an invented example

*Illustrative example with invented data.* Orrin Hollow Workshop, its products, documents and figures below are all invented. The inputs come first, then the worksheet.

## What the owner supplies

**Failure cost export.** One row per failure cost, July to September 2026.

```
record_ref,date,category,process_or_product,description,quantity,hours,cost_amount,cost_basis,source_ref
F01,2026-07-08,Rework,Door line,Re-sanded doors after a finish flaw,40,12,,Estimated,TS-1
F02,2026-07-15,Scrap,Door line,Warped panels binned,18,,1260.00,Recorded,SW-3
F03,2026-07-22,Rework,Drawer units,Re-drilled runner holes,25,9.5,,Estimated,TS-2
F04,2026-07-29,Customer return,Drawer units,Return freight and handling for 6 units,6,,540.00,Recorded,RT-11
F05,2026-08-03,Credit or refund,Drawer units,Credit note for 6 returned units,6,,1710.00,Recorded,CN-204
F06,2026-08-05,Scrap,Wardrobe frames,Frames binned after a wrong cut list,4,,2240.00,Recorded,SW-4
F07,2026-08-12,Scrap,Wardrobe frames,Offcut waste after a wrong cut list,,,2240.00,Recorded,SW-4
F08,2026-08-19,Rework,Wardrobe frames,Recut and reassembled 3 frames,3,14,,Estimated,TS-5
F09,2026-08-26,Re-inspection,Door line,Second inspection of 60 doors after the finish flaw,60,6,,Estimated,TS-6
F10,2026-09-02,Replacement,Wardrobe frames,Replacement frame shipped to a customer,1,,610.00,Recorded,RP-7
F11,2026-09-09,,Drawer units,Courier invoice covering returns and replacements; not split,,,380.00,Recorded,INV-908
F12,2026-09-16,Scrap,,Month-end scrap write-off; not split by product,,,1350.00,Recorded,SW-9
F13,2026-09-23,Rework,Door line,Repainted doors,22,8,,Estimated,TS-8
F14,2026-09-25,Rework,Drawer units,Rework on returned units,6,,,,
F15,2026-06-28,Scrap,Door line,Trim offcuts binned,30,,700.00,Recorded,SW-1
```

**Prevention and appraisal costs.**

```
cost_ref,date,category,description,cost_amount,cost_basis,source_ref
P1,2026-07-10,Prevention,Operator training day on finishing,480.00,Recorded,TR-2
P2,2026-08-14,Appraisal,Gauge calibration service,220.00,Recorded,CAL-5
P3,2026-09-12,Appraisal,Inspector time on final checks,,,
```

**Settings.** Business: Orrin Hollow Workshop. For: Owner. Period 2026-07-01 to 2026-09-30. Currency: dollars (printed with the $ symbol). Today: 10 November 2026. Categories: the defaults. Approved costing basis, in the finance contact's words: labor at \$32.00 an hour, wages only; a credit note is counted at its credited value; a return is counted as freight and handling only, without the value of the returned stock.

## The worksheet

```
COST OF POOR QUALITY WORKSHEET: Orrin Hollow Workshop, 2026-07-01 to 2026-09-30

For: Owner. Prepared 2026-11-10 from 15 failure rows read, including any outside the period, and 3 prevention and appraisal rows read. Currency: dollars.
Coverage: 14 failure rows in the period; 1 held out as a possible duplicate; 13 counted, of which 12 have a known cost and 1 has none.

1. Known failure cost by category
Internal failure
Rework: 5 rows, known cost $1,392.00 ($0.00 recorded, $1,392.00 estimated); 1 row with no cost.
Scrap: 3 rows, known cost $4,850.00 ($4,850.00 recorded, $0.00 estimated); 0 rows with no cost.
Re-inspection: 1 row, known cost $192.00 ($0.00 recorded, $192.00 estimated); 0 rows with no cost.
Internal total: $6,434.00
External failure
Customer return: 1 row, known cost $540.00 ($540.00 recorded, $0.00 estimated); 0 rows with no cost.
Credit or refund: 1 row, known cost $1,710.00 ($1,710.00 recorded, $0.00 estimated); 0 rows with no cost.
Replacement: 1 row, known cost $610.00 ($610.00 recorded, $0.00 estimated); 0 rows with no cost.
External total: $2,860.00
No category: 1 row, $380.00.
Total known failure cost: $9,674.00 ($8,090.00 recorded, $1,584.00 estimated). Rows with no cost: 1.

2. Where the known cost sits
Wardrobe frames: $3,298.00, 34% of the known total; 0 rows with no cost.
Drawer units: $2,934.00, 30% of the known total; 1 row with no cost.
Door line: $2,092.00, 22% of the known total; 0 rows with no cost.
Not assigned to a process or product: $1,350.00, 14%.
Shares are of known cost only. The order is not a priority.

3. Estimated costs
F01, Rework, Door line: 12 hours x $32.00 = $384.00.
F03, Rework, Drawer units: 9.5 hours x $32.00 = $304.00.
F08, Rework, Wardrobe frames: 14 hours x $32.00 = $448.00.
F09, Re-inspection, Door line: 6 hours x $32.00 = $192.00.
F13, Rework, Door line: 8 hours x $32.00 = $256.00.
Estimated total: $1,584.00.

4. Rows with no cost
F14, Rework, Drawer units: Rework on returned units. Missing: no amount, no hours and no basis.

5. Unresolved allocations
F11, $380.00: no category; the description says the courier invoice covers returns and replacements and is not split. Counted in the total as "No category" and under Drawer units.
F12, $1,350.00: no process or product; the description says the write-off is not split by product. Counted in the total under Scrap and as "Not assigned to a process or product".

6. Possible duplicates held out
F07, $2,240.00: shares SW-4 with F06. Counted once. Total known cost if the held-out row were also counted: $11,914.00.

7. Prevention and appraisal costs, as supplied
P1, Prevention, Operator training day on finishing: $480.00.
P2, Appraisal, Gauge calibration service: $220.00.
P3, Appraisal, Inspector time on final checks: no amount.
Known total: $700.00. Rows with no amount: 1. Shown beside the failure costs, not netted against them.

8. Assumptions used
Period 2026-07-01 to 2026-09-30, in dollars.
Labor is estimated at $32.00 an hour, wages only, as supplied by the finance contact.
A credit note is counted at its credited value. A return is counted as freight and handling only.
When two rows share a source reference and an amount, the lower record reference is counted and the other is held out.

9. Rows left out of the period
F15, 2026-06-28, $700.00.

10. Questions
1. F07 and F06 both cite SW-4 for $2,240.00. Is this one write-off entered twice, or two separate write-offs?
2. F11, $380.00: how is the courier invoice INV-908 split between returns and replacements, and which category does each part take?
3. F12, $1,350.00: which products does write-off SW-9 cover?
4. F14: what did the rework on the 6 returned units cost, in hours or in an amount?
5. The estimated labor in section 3 is wages only at $32.00 an hour. Does finance want any other labor cost included before the figures are used?
6. P3: what did the inspector time cost?

Draft for the Owner's review. Nothing has been changed, sent or recorded. The cost basis needs the finance contact's confirmation. No saving is claimed, and no priority is set.
```

Every figure in the worksheet comes from the rows and settings above. The checks: the 15 rows less F15 outside the period give 14 in the period; F07 is held out, leaving 13 counted, of which F14 has no cost. Recorded: $1,260 + $540 + $1,710 + $2,240 + $610 + $380 + $1,350 = $8,090. Estimated: 49.5 hours x $32.00 = $1,584. Together $9,674, which is also $6,434 internal + $2,860 external + $380 with no category, and also $3,298 + $2,934 + $2,092 + $1,350 by product. With F07 added, $9,674 + $2,240 = $11,914.
