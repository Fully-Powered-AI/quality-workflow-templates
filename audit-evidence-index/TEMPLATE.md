# Audit evidence index

Workflow template, version 0.1.0.

## Purpose

Build the index a quality lead needs before an internal or customer audit: every item the auditors have requested, linked to the controlled document that answers it, the revision and owner the register shows, the records supplied behind it, the earlier findings on the same ground, and the gaps, each with a named person to close it. The assistant prepares the index from four lists the person supplies. It opens no document, judges no content, certifies nothing about readiness, contacts no one and changes no record. The quality owner decides what is shared with the auditors.

## When to use it and when not to

Use it when an audit request list has arrived and the documents and records are held in different places and by different owners. It suits an internal audit or a customer audit. Run it again when requests are added or records are found.

Do not use it to plan the audit programme, to prepare a finance audit (use the audit preparation workflow template), to find stale copies at points of use (use the obsolete copy check), or to reorganise folders (use the shared folder filing plan). Do not use it to answer an auditor's finding, or to say whether the quality system conforms.

## Roles

- **Runs it:** the quality lead or the office lead.
- **Reviews the index, decides what is shared and when, and settles the open items:** the quality owner.
- **Owns each document and answers for its records:** the owner named in the register.
- **Evaluates the evidence:** the auditors, independently.

## Inputs

Four lists, plus the settings. Each list is a table with a header row. The assistant expects these default headers and reads nothing else into them. If a header differs, is missing or is not recognised, the assistant stops and asks which column is which before it does anything else.

1. **Audit request list.** Required headers: `request_id`, `request_text`. Optional headers: `asks_for` (document, records or both), `reference` (a document number the requester named), `period_from`, `period_to` (dates, year-month-day). A blank `asks_for` is treated as both, and the index says so. If the list is missing, stop.
2. **Document register.** Headers: `doc_id`, `title`, `revision`, `status`, `effective_date`, `owner`, `next_review_date`. If missing, stop.
3. **Records selected for the audit.** Headers: `record_id`, `title`, `doc_id`, `procedure_revision`, `record_date`, `location`. If missing, say so; every Records line then reads "None supplied for [period]" and the Part missing flag is raised for each request that asks for records and has a linked document.
4. **Last cycle's findings.** Headers: `finding_id`, `finding_text`, `related_ref`, `status`, `action_ref`. If missing, write "Prior findings not supplied" in place of each finding line and in the findings sections.
5. **Settings.** The audit name and date, today's date, the lead time in calendar days (default 7), the quality owner's role, which register status means in force (default Effective), and what a blank owner means (default not assigned). If the audit date is missing, stop.

## The procedure

1. **Check the inputs.** Confirm headers, that dates are readable, that `request_id` and `doc_id` values are unique, and that the audit date is given. Stop on any failure (see the stop conditions).
2. **Set the hand-off date:** the audit date minus the lead time. Every date the index names for an owner is this date.
3. **Link each request to a document, using the first rule that applies.**
   - **Reference.** If `reference` is filled and equals a `doc_id`, link that document. If it is filled but equals no `doc_id`, link nothing, note that the reference is not in the register, and go no further for this request.
   - **Named in the text.** If `reference` is blank and the request text contains exactly one `doc_id`, or exactly one full register title, link that document. If it contains more than one, link none and list each as a candidate.
   - **Overlap.** Otherwise, a register title that shares at least two significant words with the request text is a candidate. Words are matched whole, not by stem, so "inspector" does not match "inspection". Ignore small words (words of three letters or fewer) and the words document, procedure, records, record, instruction and policy. A candidate is shown but never linked.
4. **Select records.** Only for a request that asks for records or both, and only from a linked document: take records whose `doc_id` equals the linked document. If the request has a period, keep records whose `record_date` falls inside it, ends included. A record outside the period is not linked. For a candidate document, list the in-period records of that document as "candidate, not linked". A record may be linked to more than one request. The period is always tested against `record_date`, even when the request speaks of a report being closed or completed; the index does not use any other date.
5. **Raise flags on linked documents and linked records only.** A flag is a question for a person, not a finding.
   - **Not in force:** the register status is not the in-force status.
   - **No owner:** the owner is blank.
   - **Review overdue:** a `next_review_date` is given and falls before the audit date.
   - **Revision mismatch:** only when the document is in force. A record dated on or after the document's effective date whose `procedure_revision` differs from the register's revision is flagged; so is a record whose `procedure_revision` is blank. A record dated before the effective date is not flagged. If the document is not in force, skip this flag and say it was skipped.
   - **No location:** a linked record has a blank `location`.
   - **Part missing:** the request asks for records or both, a document is linked, and no record is in the period.
6. **Link prior findings.** A finding is linked to a request when its `related_ref` equals the request's `request_id` or the `doc_id` of the request's linked document. Never link by topic or by guessing from the wording. Print the finding's status and `action_ref` as given. Do not say whether the action worked. A finding with a blank `related_ref`, or one that matches no request, goes to the unlinked list. An open linked finding is added to the request's items to settle.
7. **Give each request one status.**
   - **Linked:** everything the request asks for is found and no flag is raised.
   - **Check first:** a document or records are linked and at least one flag is raised.
   - **Possible match only:** nothing is linked, but there is at least one candidate.
   - **Nothing found:** nothing is linked and there is no candidate.
8. **Write the items to settle.** One numbered item per flag, question or open finding. Each names the person who acts (the document owner, or the quality owner when there is no owner) and the hand-off date. For a Possible match only, the item asks the quality owner to confirm the candidate by the hand-off date. For Nothing found, the item says nothing matched (or that the reference is not in the register) and names the quality owner and the hand-off date.
9. **Count and tie out.** Count the requests in each status; the four counts must add up to the number of requests. Count the records supplied, those linked to at least one request, and those linked to none. A record linked to two requests counts once as linked.
10. **List what links to nothing:** records linked to no request, each with its reason (outside a period, candidate only, document not requested); findings linked to no request. When a record has two reasons, give the period reason first, then the candidate reason.
11. **Close.** List the decisions for the quality owner and print the closing line. "Prepared for" prints the quality owner setting exactly as given, whether it is a role or a name. Return the index to the person who started the work only.

## Exceptions and stop conditions

- **A required header is missing, renamed, or an unknown header appears:** stop and ask which column is which. Do not guess.
- **A `doc_id`, `request_id` or `record_id` appears twice with different details:** stop and name the duplicate rows.
- **The audit date is missing or a date cannot be read:** stop.
- **A request asks for something that sounds like a whole system ("all quality records"):** do not link by guesswork. Give it Nothing found or Possible match only, and ask the quality owner to narrow it.
- **Asked to say the evidence is ready, sufficient, compliant or certified:** decline. State what is linked and what is missing, and leave the judgment to the quality owner and the auditors.
- **Asked to read a document, to say what it proves, or to infer content from a file title:** decline. The index uses the supplied fields only.
- **Asked to contact owners, send the index, change the register or a record, or move or rename a file:** decline. A person does that.

## Output format

```
AUDIT EVIDENCE INDEX: [audit name], audit date [date]

Prepared for: [quality owner]. Owners respond by [hand-off date]. Register and records as supplied on [date].

Count: [n] requests. Linked [n]. Check first [n]. Possible match only [n]. Nothing found [n]. Tie-out: [n] + [n] + [n] + [n] = [n]. Records supplied [n]: linked [n], not linked [n].

Index

[request id]: [request text]
  Status: [Linked | Check first | Possible match only | Nothing found]
  Document: [doc id], [title], revision [rev], [register status], effective [date or "date not recorded"], review due [date or "date not recorded"]; owner [name or "not assigned"]
    (a candidate reads "Candidate, not linked: ..."; none reads "None found", with the reason if the reference is not in the register)
  Records: [record id], [title], [date], held at [location] (or "location not recorded" in place of "held at [location]"); ...
    (or "Not requested", "None supplied for [period]", "None linked: no document linked" when records are requested and neither a document nor a candidate is linked, or "Candidate, not linked: ...")
  Prior findings: [finding id], [status], action [action ref]; ... (or "None")
  To settle: [numbered items, each naming who acts and the hand-off date] (or "Nothing")

(repeat the block for every request, in request order)

Supplied but not linked to any request: [record id (reason); ...] (or "None.")

Prior findings not linked to any request: [finding id, status, text; action [ref] or "action not recorded"; ...] (or "None.")

Decisions for the quality owner
1. Possible matches to confirm: [request ids] (or "None.")
2. Requests with nothing found: [request ids] (or "None.")
3. Prior findings to link to a request: [finding ids] (or "None.")
4. What is shared with the auditors, in what form and when.

This index, built from the lists supplied for [audit name], shows where each item is held and what the register says about its revision. It does not show that a document's content is right, that a record proves the procedure worked, or that anything is ready for audit. The auditors judge the evidence themselves. The index changes no records and sends nothing.
```

Write dates as day, month name, year. Where a date is missing, use the wording given in the format above ("date not recorded", "location not recorded").

## Reviewer checklist

1. The tie-out adds up and matches the number of requests in the auditors' list. (Quality owner)
2. Each request appears once, in the order received. (Quality owner)
3. Each linked document and revision matches the register row. (Quality lead)
4. No candidate has been treated as linked. (Quality owner)
5. Each record's date and location match the supplied list, and each record outside a period is listed as not linked. (Quality lead)
6. Each prior finding is linked only by an explicit reference. (Quality owner)
7. Every item to settle names a person and the hand-off date. (Quality owner)
8. Nothing in the index says ready, sufficient, compliant or certified. (Quality owner)
9. The files the index points to have been opened by a person and are what the register says they are. (Document owners)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean request.** A request naming a registered document in force, asking only for the document. Expected: Linked, records "Not requested", nothing to settle.
2. **Reference not in the register.** A request with a document number the register lacks. Expected: Nothing found, with the reason in the Document line.
3. **Candidate only.** A request with no reference whose text shares two significant words with one register title. Expected: Possible match only; the candidate and its in-period records marked not linked.
4. **Two documents named.** Request text containing two document numbers and no reference. Expected: neither linked; both listed as candidates.
5. **Record outside the period.** A document linked, one record before the period start. Expected: record not linked, listed under "Supplied but not linked" with its reason.
6. **Revision mismatch.** A record dated after the effective date citing the previous revision. Expected: flag raised. A record dated before the effective date citing the previous revision raises none.
7. **Document not in force.** Register status In review. Expected: Not in force flag; revision mismatch skipped and the skip stated.
8. **Missing records.** A request for records with a linked document and none in the period. Expected: Check first; "None supplied for [period]".
9. **Finding with no reference.** A finding with a blank related reference whose wording matches a request. Expected: listed as not linked and offered for the quality owner to link; not linked by the assistant.
10. **Header changed.** A register column renamed. Expected: stops and asks.
11. **Asked if ready.** "Are we ready for the audit?" Expected: declines to judge; states what is linked and missing.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare an audit evidence index for the quality lead. You link what
the auditors requested to what the organization has listed. You never
open or judge a document, never say anything is ready, sufficient,
compliant or certified, never contact anyone, and never send, change or
move a record or file. A person approves anything that is sent or
changed; the quality owner decides what is shared.

The user will supply four lists with header rows (audit requests;
document register; records selected; last cycle's findings) and
settings (audit name and date, today, lead time in days, quality owner,
which register status means in force, what a blank owner means).
Expected headers: requests request_id, request_text, optional asks_for,
reference, period_from, period_to; register doc_id, title, revision,
status, effective_date, owner, next_review_date; records record_id,
title, doc_id, procedure_revision, record_date, location; findings
finding_id, finding_text, related_ref, status, action_ref. If a header
differs or is missing, stop and ask which column is which. If the
request list, the register or the audit date is missing, stop. Stop on a
duplicate id with different details. If the records list is missing,
say so; every Records line reads "None supplied for [period]" and the
Part missing flag is raised for each request that asks for records and
has a linked document. If the findings list is missing, write "Prior
findings not supplied" in place of each Prior findings line and in the
unlinked findings section.

1. Hand-off date = audit date minus lead time.
2. Link each request to a document by the first rule that applies: a
   reference equal to a doc_id; a reference not in the register links
   nothing and is noted; otherwise exactly one doc_id or full title in
   the text links it; more than one links none and lists candidates;
   otherwise a register title sharing at least two significant words
   with the text is a candidate only. Match whole words, not stems
   ("inspector" does not match "inspection"). Ignore words of three
   letters or fewer and document, procedure, records, record, instruction and policy. A
   candidate is never linked. A request that sounds like a whole system
   ("all quality records") links nothing: give it Nothing found or
   Possible match only and ask the quality owner to narrow it.
3. For requests asking for records or both, take the records of the
   linked document, inside the period if one is given. Records outside
   the period are not linked. For a candidate, show its in-period
   records as "candidate, not linked". A blank asks_for means both;
   say so.
4. Flag only linked documents and records: status not in force; no
   owner; next review before the audit date; revision mismatch (only if
   the document is in force: record on or after the effective date with
   a different or blank procedure_revision; skip and say so when not in
   force); no location; records requested and none in the period. Test
   a period against record_date only.
5. Link a finding only when related_ref equals the request_id or the
   linked doc_id. Print its status and action as given; never say if
   the action worked. Others go to the unlinked list. An open linked
   finding is added to the request's items to settle.
6. Status: Linked (found, no flag); Check first (found, at least one
   flag); Possible match only (candidate, nothing linked); Nothing
   found.
7. Each item to settle is numbered, one per flag, question or open
   linked finding, and names who acts and the hand-off date: the
   document's owner, or the quality owner when there is none. For
   Possible match only, the item asks the quality owner to confirm the
   candidate. For Nothing found, the item says nothing matched (or that
   the reference is not in the register) and names the quality owner.
8. Count the statuses; they must sum to the number of requests. Count
   records supplied, linked, not linked; a record linked to two
   requests counts once. List unlinked records with reasons (period
   reason first, then candidate reason) and unlinked findings.
9. Use the output format exactly, with dates as day, month name, year.
   A missing date reads "effective date not recorded" or "review due
   date not recorded"; a missing location reads "location not
   recorded" in place of "held at". Records reads "None linked: no
   document linked" when records are requested and neither a document
   nor a candidate is linked. Print the quality owner setting exactly
   as given after "Prepared for". Print "None." for an empty list and
   keep the closing paragraph.

Use only the supplied fields. A file title is not evidence of content.
If asked whether the audit is ready or the evidence adequate, decline
and report what is linked and what is missing.
```

## What to customize

- The four files and their column names, so each audit starts from the same exports.
- The lead time, and which register status means a document is in force.
- The number of significant words that makes a candidate (the template uses two), and the small words ignored.
- What a blank owner means, and who answers for a document with none.
- The period rule for records. The template tests the supplied `record_date` against the request's period; if a request means another date, such as the date a report was closed, add that column and say so.
- How the approved index reaches the auditors, and who sends it.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Tried on its invented example in Claude on 10 November 2026, twice: after an independent review changed the instruction block, the output format and the example, it was run again, and the second run is the one recorded in the published trial. A later review added small clarifying rules (words of three letters or fewer ignored; missing records or findings list; the period tested on the record date; a record linked twice counts once; reason order in the unlinked list; the printing of the quality owner setting). They change nothing in the example's output, and the template was not run again after them. Not yet tested in a client environment.
