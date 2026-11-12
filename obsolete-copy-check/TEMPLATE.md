# Obsolete copy check

Workflow template, version 0.1.0.

## Purpose

Compare one organization's master document list with the inventories of copies found at its points of use, and report where an instruction is in use that should not be. Every copy found is sorted into one class. Each out-of-date copy is set beside the withdrawal evidence on file, and each place that has not been inventoried, or was inventoried too long ago, is named as a gap. The assistant prepares the comparison; it never confirms that a copy is obsolete, removes or replaces a copy, edits a master list or records a withdrawal. Document control decides, and the document owner withdraws and replaces copies through the organization's agreed process.

## When to use it and when not to

Use it when the agreed document-control review is due, after a batch of revisions has been released, before an audit, or when an area owner reports an old instruction in use. Run it again after copies have been removed, with fresh inventories, to see what is left.

Do not use it:

- to write or revise a procedure. Write an SOP from how the work is done does that;
- to tidy or rename electronic folders. Shared folder filing plan does that;
- to judge whether a revision is correct, compare two versions of a document or decide what a change requires;
- when no inventory has been taken. The assistant cannot look in a cabin, a drawer or a tablet; people take the inventories.

## Roles

- **Runs it:** the document controller or the quality lead.
- **Supplies an inventory:** the owner of each location, who looks at what is actually there.
- **Confirms obsolete copies and decides each finding:** document control.
- **Withdraws and replaces copies:** the document owner, through the agreed process.
- **Records the withdrawal and its evidence:** whoever the process names. The assistant records nothing.

## Inputs

All lists are files or pasted tables. Dates are written year-month-day. Default column headers are given; if a required header does not match, stop and ask which column is which. Do not guess.

1. **The master document list.** Required. Headers: `doc_id,title,current_revision,effective_date,status,owner`. Status is Current or Withdrawn. For a withdrawn document, the effective date is the date it was withdrawn. If a document id appears twice, stop and ask.
2. **The point-of-use inventories.** Required. One table, or several joined, with headers: `location,doc_id,revision,copy_type,count,date_checked,checked_by`. The copy type is printed or saved file. If the `count` column is missing, each row is one copy and the report says so; if the column is present and a cell is blank, stop and ask. A blank `date_checked` is treated as older than any limit.
3. **The revision history.** Optional. Headers: `doc_id,revision,obsolete_from`. The date from which a revision is no longer valid, which is the effective date of its replacement. If missing, every revision that differs from the current one is reported as not recognised, and the report says the history was not supplied.
4. **The distribution list.** Optional. Headers: `doc_id,location,expected_copies`. If missing, write "distribution list not supplied" and skip the expected-copy check and the not-inventoried check.
5. **The withdrawal records.** Optional. Headers: `doc_id,revision,location,withdrawn_date,withdrawn_by,evidence_ref`. If missing, write "withdrawal records not supplied" against every out-of-date copy.
6. **The settings.** The organization or site name, the review date, the name of the role in document control, and [your inventory age limit], default 30 days. If the review date is missing, stop and ask; if the organization or site name is missing, ask for it. The cut-off for an inventory to count is the review date minus the limit.

The assistant works from what the person supplies. It needs no connection to a document system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers of each table, the date format and the review date. Count the documents, the distribution lines, the inventory rows and the copies (the sum of `count`), the locations and the withdrawal records. Compare document ids and revisions after trimming spaces and ignoring capital letters; "Rev D" and "D" are different revisions, and that is reported, not corrected.
2. **Date each location's inventory.** A location's inventory date is the latest `date_checked` among its rows. It is too old if that date is before the cut-off.
3. **Sort every inventory row,** using the first rule that fits:
   - the document id is not on the master list: **Not on master list**;
   - the master status is Withdrawn: **Withdrawn document**;
   - the revision is the current revision: **Current**, unless the master effective date is after the review date, in which case **Not yet due** (a copy issued early);
   - the revision is in the history with an `obsolete_from` on or before the review date: **Out of date**;
   - the revision is in the history with an `obsolete_from` after the review date: **Not yet due** (still in force until that date);
   - otherwise: **Revision not recognised**.
   A history row with a blank date: stop and ask.
4. **Tie out.** The copies in all six classes must add up to the copies found. If they do not, stop and report the figures.
5. **Match withdrawal evidence** for every Out of date and Withdrawn document copy, on document id, revision and location. If several records match, use the latest date. Name one state:
   - **no record:** nothing matches;
   - **record, copy found after it:** the inventory date is after the withdrawal date, so the record and the finding disagree;
   - **record, inventory not later:** the inventory date is on or before the withdrawal date, so the inventory may predate the removal and the location needs a new look.
   Never treat a record as proof that a copy is gone.
6. **Account for the records that matched no copy.** For each withdrawal record with no copy found at its location: if that location has an inventory that is not too old and dated on or after the withdrawal date, it is **consistent**; otherwise it is **not confirmed by any inventory**. A record for a document not on the master list is reported as such, whether or not it matched a copy.
7. **Check coverage,** when the distribution list is supplied. For each line, count the copies at that location in the classes Current and Not yet due. Then name the result: **met** (at least the expected number), **none found** or **fewer than expected** (with the numbers), or **cannot say** when the location has no inventory or its inventory is too old. A Not yet due copy counts toward the expected number, so a line can read "met" while its copies are about to be replaced. List every location on the distribution list with no inventory, and every location whose inventory is too old, with its date and the days before the review date.
8. **Order each section.** Out of date: the oldest `obsolete_from` first, then location, then document id. Every other section: location in alphabetical order, then document id.
9. **Write the decisions.** One numbered decision for each item listed under Out of date, Copies of withdrawn documents, Revision not recognised, Not on master list, and Coverage gaps, in that order. Each is a question for document control with its facts. Recommend nothing unless asked. Items under Not yet due and the consistent withdrawal records get no decision.
10. **State what is not proven,** including that copies counted as Current at a location whose inventory is too old are not confirmed as current, and return the draft to the person who ran it. Document control decides each finding; a person who owns the process removes copies.

## Exceptions and stop conditions

- **A required header does not match, a document id is duplicated in the master list, a date is not year-month-day, a count cell is blank, or the review date is missing:** stop and ask.
- **The copies in the six classes do not add up to the copies found:** stop and report the figures.
- **An inventory that is incomplete or does not cover a location:** report the gap. An incomplete inventory cannot show that every old copy has gone, and the report must say so.
- **Asked to confirm a copy as obsolete, to say a copy has been removed, to edit a record, to write a withdrawal record or to tell a location to remove a copy:** decline and name the role that does it.
- **Asked to judge which revision is right, or to compare the content of two revisions:** decline; that is the document owner's work.
- **The inputs contain a password, a login code or personal details beyond a name and role:** do not repeat them; tell the person to remove them from the source.

## Output format

```
OBSOLETE COPY CHECK: [organization or site], review date [date]

For: [document control role]. Inventories count if checked on or after [cut-off date] ([n] days before the review date).
Prepared: [today's date], from the master list ([n] documents), revision history ([n] rows / not supplied), distribution list ([n] lines / not supplied), inventories ([n] locations, [n] rows[; one copy per row, no count column]), withdrawal records ([n] / not supplied).

Copies found: [n] in [n] rows at [n] locations. Current [n]. Out of date [n]. Withdrawn document [n]. Revision not recognised [n]. Not on master list [n]. Not yet due [n]. Tie-out: [n] + [n] + [n] + [n] + [n] + [n] = [n].
Locations: [n] on the distribution list; [n] inventoried; [n] not inventoried; [n] inventory too old.

Out of date: [n] copies
[Location]: [doc_id] [title], revision [x] found, [count] [copy type]; current revision [y]; out of date since [date] ([n] days). Checked [date] by [name]. Withdrawal evidence: [no record / record [date], [evidence_ref], copy found after it / record [date], [evidence_ref], inventory not later, location needs a new look / withdrawal records not supplied].
(none)

Copies of withdrawn documents: [n] copies
[Location]: [doc_id] [title], revision [x], [count] [copy type]; document withdrawn [date] ([n] days). Checked [date] by [name]. Withdrawal evidence: [as above].
(none)

Revision not recognised: [n] copies
[Location]: [doc_id] [title], revision [x] found, [count] [copy type]; current revision [y]; revision [x] is not in the history. Checked [date] by [name].
(none)

Not on master list: [n] copies
[Location]: [doc_id], revision [x], [count] [copy type]. Checked [date] by [name].
(none)

Coverage gaps
Not inventoried: [location] ([documents expected there]).
Inventory too old: [location], checked [date] ([n] days before the review date).
Expected copy: [location], [doc_id] [title]: [none found / [n] found of [n] expected].
(none)
Distribution lines: [n]. Met [n]. Cannot say [n]. Short [n]. Tie-out: [n] + [n] + [n] = [n].

Not yet due: [n] copies
[Location]: [doc_id] [title], revision [x], [count] [copy type]; [still in force until [date], replaced by revision [y] / issued before its effective date of [date]].
(none)

Withdrawal records with no copy found: [n] of [n] records
[doc_id] revision [x], [location], [date], [evidence_ref]: [consistent, no copy in the inventory of [date] / not confirmed by any inventory / document not on master list].
(none)

Decisions for [document control role]: [n]
[n]. [Item.] [The facts.] [The question.]
(none)

Not proven: [A sentence stating what the supplied inventories cannot show, naming any location not inventoried or too old and saying that copies counted as Current there are not confirmed as current, or "every location on the distribution list was inventoried in time" when so.]

Draft for [document control role]'s decision. No copy has been confirmed, removed, replaced or recorded, and no document has been changed.
```

Print "(none)" under any section with no items, and "none" for a count of zero. Under Coverage gaps, "(none)" stands in place of the three kinds of gap lines when there are none, and the "Distribution lines" line is always printed after it; if no distribution list was supplied, write "distribution list not supplied" in its place.

Section headings count copies; each line is one inventory row, so a line can hold more than one copy. In a heading write "1 copy" or "[n] copies". On a line write the copy type with its noun: "1 printed copy" or "[n] printed copies", "1 saved file" or "[n] saved files". "Inventoried" counts every location with at least one inventory row, whether or not it is on the distribution list; "not inventoried" counts locations on the distribution list with none. Withdrawal evidence is matched on document, revision and location, so a record for the same revision at another location reads "no record" here.

## Reviewer checklist

1. Every row of every inventory appears once, in one class, and the tie-out is correct. (Document controller)
2. Each revision is classed as the master list and history say, and no revision was compared as "older" or "newer" by anything but those lists. (Document controller)
3. Each out-of-date copy names the right withdrawal state, and no record is presented as proof of removal. (Quality lead)
4. The coverage section names every location with no inventory or an old one, and the "Not proven" line says so. (Quality lead)
5. Every item that needs action has a decision, and the numbers match. (Document controller)
6. Nothing in the report says a copy has been removed, confirmed obsolete or recorded. (Quality lead)
7. A sample of findings, including at least one of each class, has been checked against the physical copy. (Area owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean location.** All copies are the current revision. Expected: all Current; no decisions for that location.
2. **Out of date, no record.** An old revision with an `obsolete_from` in the past and no withdrawal record. Expected: Out of date, evidence "no record", one decision.
3. **Record, copy found after it.** A withdrawal record dated before the inventory, copy still listed. Expected: the disagreement is stated and the decision asks which is wrong.
4. **Inventory predates the record.** Inventory dated before the withdrawal date. Expected: "location needs a new look"; the record is not accepted as proof.
5. **Still in force.** An old revision whose `obsolete_from` is after the review date. Expected: Not yet due, no decision.
6. **Revision not on the history.** A revision that is neither current nor listed. Expected: Revision not recognised; the assistant does not decide whether it is older or newer.
7. **Withdrawn document held.** A copy of a document marked Withdrawn. Expected: its own section.
8. **Not inventoried.** A location on the distribution list with no inventory rows. Expected: a coverage gap, "cannot say" for its distribution lines.
9. **Header does not match.** An inventory with `doc` where `doc_id` is expected. Expected: stops and asks.
10. **Asked to confirm.** "Mark these as obsolete and tell the areas to remove them." Expected: declines and names document control.

## Instructions for the AI assistant

```
You prepare an obsolete copy check for document control. You never
change a record, send anything or contact anyone, and you never confirm
that a copy is obsolete, remove or replace a copy, edit a document, or
tell anyone to remove a copy. A person in
document control decides every finding; the document owner withdraws
and replaces copies.

The user will supply: a master document list (doc_id, title,
current_revision, effective_date, status, owner); point-of-use
inventories (location, doc_id, revision, copy_type, count, date_checked,
checked_by); and, if available, a revision history (doc_id, revision,
obsolete_from), a distribution list (doc_id, location, expected_copies),
withdrawal records (doc_id, revision, location, withdrawn_date,
withdrawn_by, evidence_ref) and the settings: organization or site name,
review date, the document control role, and [inventory age limit],
default 30 days.

If the master list, the inventories or the review date is missing, stop
and say so; if the organization or site name is missing, ask for it. If
a required header does not match, a document id is duplicated, a date is
not year-month-day, a count cell is blank or a history date is blank,
stop and ask; do not guess. If the count column is missing, treat each
inventory row as one copy and say so in the report. A blank date_checked
is older than any age limit. If an optional table is missing, say so
where it is used and continue.

1. Count documents, rows, copies, locations and records. Compare ids and
   revisions after trimming spaces and ignoring capitals.
2. A location's inventory date is the latest date_checked among its rows.
   It is too old if before the review date minus the age limit.
3. Sort each row by the first rule that fits: id not on the master list,
   Not on master list; master status Withdrawn, Withdrawn document;
   revision equals current, Current (Not yet due if the effective date is
   after the review date); revision in the history, Out of date if its
   obsolete_from is on or before the review date, otherwise Not yet due;
   anything else, Revision not recognised. Never judge a revision older
   or newer except by these lists.
4. The six classes must add up to the copies found. If not, stop and
   report the figures.
5. For Out of date and Withdrawn document copies, match a withdrawal
   record on id, revision and location (latest date). State: no record;
   record with the copy found after it (inventory date after the record);
   or record with the inventory not later (the location needs a new
   look). A record is never proof of removal.
6. Records matching no copy: consistent if the location's inventory is
   not too old and is dated on or after the record, otherwise not
   confirmed by any inventory. A record for a document not on the master
   list is reported as such.
7. If a distribution list is given, count Current and Not yet due copies
   at each line's location: met, none found, fewer than expected, or
   cannot say (no inventory or one that is too old). Not yet due copies
   count toward the expected number. List locations with no inventory
   and locations with an old one.
8. Order Out of date by the oldest obsolete_from first, then location,
   then document id; order every other section by location in
   alphabetical order, then document id. Write one numbered decision for
   each item under Out of date, withdrawn documents, not recognised, not
   on the master list and coverage gaps, in that order. Recommend
   nothing unless asked.
9. Use the output format exactly, with "(none)" for an empty section
   (under Coverage gaps, "(none)" replaces the gap lines and the
   "Distribution lines" line is still printed). Section headings count
   copies, each line is one inventory row; in a heading write "1 copy"
   or "n copies", on a line write "1 printed copy" or "n printed
   copies", "1 saved file" or "n saved files". End with a "Not proven"
   line stating what the inventories cannot show, including that Current
   copies at a location whose inventory is too old are not confirmed as
   current, and then the closing line: "Draft for [document control
   role]'s decision. No copy has been confirmed, removed, replaced or
   recorded, and no document has been changed."

If asked to confirm a copy as obsolete, say a copy is gone, write a
withdrawal record, edit a list, judge which revision is right or tell a
location to remove a copy, decline and name the role that does it. If
the inputs contain a password, a login code or personal details beyond
a name and role, do not repeat them; tell the user to remove them. An
incomplete inventory cannot prove that every old copy has gone; say so.
```

## What to customize

- The files and column names your master list, history, distribution list, inventories and withdrawal records use, and how revisions are written.
- [your inventory age limit], and how often each location is inventoried.
- What counts as evidence of withdrawal in your business, and who keeps it.
- Which copy types you inventory: printed, saved files, tablets, binders, vehicles.
- Which locations belong on the distribution list, and how many copies each should hold.
- Who confirms an obsolete copy, who removes it and who replaces it.
- Whether a current document held in a location that is not on its distribution line is reported. As written, the copy is counted as Current and appears nowhere else, and a location with an inventory but no distribution line counts as inventoried but gets no coverage line.
- Whether a Not yet due copy should count toward an expected number. As written it does, so a line can read "met" while its copies are about to be replaced.
- Whether a withdrawal record for the same revision at another location should be mentioned. As written, records match on document, revision and location, so such a record reads "no record" at the location where the copy was found.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried once on its invented example in Claude on 10 November 2026; the record is published with it. After the independent review the same day, and without a rerun, the points that run and the review found open were settled in the template and the pasted instructions: an organization or site name in the settings, singular and plural forms and what headings count, what "inventoried" means, the ordering rule and the withdrawal-record case in the pasted instructions, and a note on copies counted as Current from an old inventory. Later, still without a rerun, a printed copy was given its noun in the format and the example ("1 printed copy"), the pasted instructions gained the rules for a missing count column and a blank date_checked, the empty Coverage gaps section was made explicit, and two decision questions in the example stopped offering explanations. Not yet tested in a client environment.
