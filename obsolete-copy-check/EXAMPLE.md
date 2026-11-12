# Obsolete copy check: an invented example

*Illustrative example with invented data.* The firm, the people, the documents, the locations, the dates and the references below are all invented. The firm is an invented 70-person precision-parts maker whose document controller runs the monthly review of controlled documents. First come the inputs the document controller supplied, in full, then the report the workflow template returned.

## The inputs

### 1. Settings

```
Review date: 2026-11-09
Organization or site: Firm A
Document control role: Document controller
Inventory age limit: 30 days
```

### 2. Master document list

```
doc_id,title,current_revision,effective_date,status,owner
WI-101,Cell 1 setup and first-off check,D,2026-09-14,Current,Production manager
WI-102,Torque check on final assembly,B,2026-06-01,Current,Production manager
WI-140,Manual deburring station,C,2025-08-12,Withdrawn,Production manager
WI-205,Goods-in inspection,F,2026-10-05,Current,Quality lead
WI-210,Gauge handling and storage,C,2026-03-20,Current,Inspection supervisor
WI-330,Despatch labelling,E,2026-11-16,Current,Despatch lead
FM-310,Nonconforming material tag,A,2025-11-02,Current,Quality lead
```

For WI-140, the effective date is the date the document was withdrawn.

### 3. Revision history

```
doc_id,revision,obsolete_from
WI-101,B,2025-11-17
WI-101,C,2026-09-14
WI-102,A,2026-06-01
WI-205,D,2026-04-20
WI-205,E,2026-10-05
WI-210,B,2026-03-20
WI-330,D,2026-11-16
```

### 4. Distribution list

```
doc_id,location,expected_copies
WI-101,Cell 1,1
WI-101,Cell 2,1
WI-102,Final Assembly,1
WI-205,Goods-In,1
WI-205,Inspection Bay,1
WI-210,Inspection Bay,1
WI-210,Gauge Store,1
FM-310,Quarantine Cage,1
WI-330,Despatch,2
```

### 5. Point-of-use inventories (seven locations, joined)

```
location,doc_id,revision,copy_type,count,date_checked,checked_by
Cell 1,WI-101,D,printed,1,2026-11-03,Cell 1 team leader
Cell 1,WI-101,C,printed,1,2026-11-03,Cell 1 team leader
Cell 1,WI-140,C,printed,1,2026-11-03,Cell 1 team leader
Final Assembly,WI-102,B,printed,1,2026-11-04,Final assembly lead
Final Assembly,WI-102,A,saved file,2,2026-11-04,Final assembly lead
Goods-In,WI-205,F,printed,1,2026-11-05,Goods-in supervisor
Goods-In,WI-205,E,printed,1,2026-11-05,Goods-in supervisor
Inspection Bay,WI-205,F,saved file,1,2026-11-05,Inspection supervisor
Inspection Bay,WI-210,D,printed,1,2026-11-05,Inspection supervisor
Gauge Store,WI-210,B,printed,1,2026-10-12,Gauge store keeper
Gauge Store,WI-210,C,printed,1,2026-10-12,Gauge store keeper
Quarantine Cage,FM-310,A,printed,1,2026-08-18,Quality technician
Despatch,WI-330,D,printed,2,2026-11-06,Despatch lead
Despatch,LBL-77,B,printed,1,2026-11-06,Despatch lead
```

### 6. Withdrawal records

```
doc_id,revision,location,withdrawn_date,withdrawn_by,evidence_ref
WI-101,B,Cell 1,2025-11-20,Cell 1 team leader,Return slip RS-0301
WI-102,A,Final Assembly,2026-06-03,Final assembly lead,Return slip RS-0412
WI-205,E,Inspection Bay,2026-10-12,Inspection supervisor,Return slip RS-0529
WI-210,B,Gauge Store,2026-10-20,Inspection supervisor,Return slip RS-0533
```

## The output

**OBSOLETE COPY CHECK: Firm A, review date 2026-11-09**

- **For:** Document controller. Inventories count if checked on or after 2026-10-10 (30 days before the review date).
- **Prepared:** 2026-11-09, from the master list (7 documents), revision history (7 rows), distribution list (9 lines), inventories (7 locations, 14 rows) and withdrawal records (4).

**Copies found:** 16 in 14 rows at 7 locations. Current 6. Out of date 5. Withdrawn document 1. Revision not recognised 1. Not on master list 1. Not yet due 2. Tie-out: 6 + 5 + 1 + 1 + 1 + 2 = 16.

**Locations:** 8 on the distribution list; 7 inventoried; 1 not inventoried; 1 inventory too old.

**Out of date: 5 copies**

- Gauge Store: WI-210 Gauge handling and storage, revision B found, 1 printed copy; current revision C; out of date since 2026-03-20 (234 days). Checked 2026-10-12 by Gauge store keeper. Withdrawal evidence: record 2026-10-20, Return slip RS-0533, inventory not later, location needs a new look.
- Final Assembly: WI-102 Torque check on final assembly, revision A found, 2 saved files; current revision B; out of date since 2026-06-01 (161 days). Checked 2026-11-04 by Final assembly lead. Withdrawal evidence: record 2026-06-03, Return slip RS-0412, copy found after it.
- Cell 1: WI-101 Cell 1 setup and first-off check, revision C found, 1 printed copy; current revision D; out of date since 2026-09-14 (56 days). Checked 2026-11-03 by Cell 1 team leader. Withdrawal evidence: no record.
- Goods-In: WI-205 Goods-in inspection, revision E found, 1 printed copy; current revision F; out of date since 2026-10-05 (35 days). Checked 2026-11-05 by Goods-in supervisor. Withdrawal evidence: no record.

**Copies of withdrawn documents: 1 copy**

- Cell 1: WI-140 Manual deburring station, revision C, 1 printed copy; document withdrawn 2025-08-12 (454 days). Checked 2026-11-03 by Cell 1 team leader. Withdrawal evidence: no record.

**Revision not recognised: 1 copy**

- Inspection Bay: WI-210 Gauge handling and storage, revision D found, 1 printed copy; current revision C; revision D is not in the history. Checked 2026-11-05 by Inspection supervisor.

**Not on master list: 1 copy**

- Despatch: LBL-77, revision B, 1 printed copy. Checked 2026-11-06 by Despatch lead.

**Coverage gaps**

- Not inventoried: Cell 2 (WI-101).
- Inventory too old: Quarantine Cage, checked 2026-08-18 (83 days before the review date).
- Expected copy: Inspection Bay, WI-210 Gauge handling and storage: none found.
- Distribution lines: 9. Met 6. Cannot say 2. Short 1. Tie-out: 6 + 2 + 1 = 9.

**Not yet due: 2 copies**

- Despatch: WI-330 Despatch labelling, revision D, 2 printed copies; still in force until 2026-11-16, replaced by revision E.

**Withdrawal records with no copy found: 2 of 4 records**

- WI-101 revision B, Cell 1, 2025-11-20, Return slip RS-0301: consistent, no copy in the inventory of 2026-11-03.
- WI-205 revision E, Inspection Bay, 2026-10-12, Return slip RS-0529: consistent, no copy in the inventory of 2026-11-05.

**Decisions for Document controller: 10**

1. **Gauge Store, WI-210 revision B.** A printed copy of a revision obsolete since 2026-03-20 was found on 2026-10-12. The record of removal, RS-0533, is dated 2026-10-20, after that inventory. Has the copy been removed since, and does the Gauge Store need a new look?
2. **Final Assembly, WI-102 revision A.** Two saved files of a revision obsolete since 2026-06-01 were found on 2026-11-04, although RS-0412 records withdrawal on 2026-06-03. The record and the inventory disagree. Which is wrong, and do you confirm the files as obsolete?
3. **Cell 1, WI-101 revision C.** One printed copy of a revision obsolete since 2026-09-14, with no withdrawal record. Do you confirm it as obsolete, and who removes it through the agreed process?
4. **Goods-In, WI-205 revision E.** One printed copy of a revision obsolete since 2026-10-05, with no withdrawal record. Do you confirm it as obsolete, and who removes it through the agreed process?
5. **Cell 1, WI-140 revision C.** One printed copy of a document withdrawn on 2025-08-12, with no withdrawal record. Do you confirm it as obsolete, and who removes it through the agreed process?
6. **Inspection Bay, WI-210 revision D.** One printed copy of a revision that is neither the current revision C nor in the history. Who establishes what this copy is, and does the history need to change?
7. **Despatch, LBL-77 revision B.** One printed copy of a document that is not on the master list. Is it a controlled document that should be added, or something that should not be in use?
8. **Cell 2.** No inventory was supplied, and WI-101 is expected there. Who inventories Cell 2, and by when?
9. **Quarantine Cage.** The inventory is 83 days old, and FM-310 is expected there. Who takes a new inventory, and by when?
10. **Inspection Bay, WI-210.** The one expected copy of the current revision C was not found, and a revision D copy is there instead (decision 6). Which revision should the Inspection Bay hold, and who supplies it?

**Not proven:** Cell 2 has not been inventoried and the Quarantine Cage inventory is 83 days old, so nothing can be said about old copies at those two locations. The one copy counted as Current at the Quarantine Cage (FM-310) comes from that old inventory and is not confirmed as current. The other six inventories show only what was found on the day each was taken.

Draft for Document controller's decision. No copy has been confirmed, removed, replaced or recorded, and no document has been changed.
