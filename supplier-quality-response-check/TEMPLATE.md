# Supplier quality response check

Capability template, version 0.1.0.

## Purpose

Set a supplier's reply to a quality finding against the finding itself and the buyer's own records. The check marks each request in the finding as addressed in full, addressed in part, not addressed or disputed; lists where the reply differs from the records, leaves a lot unmentioned, is unclear or is out of step with the delivery calendar; lists each action the supplier proposes and whether it is promised or reported done; lists the attachments received and the evidence still to ask for; names what is still to be verified, with the criterion where the finding states one; and ends with questions and the options open to the owner. The assistant prepares. It never accepts a reply, closes a finding, verifies an action, contacts the supplier or changes a record.

## When to use it and when not to

Use it when a supplier's reply to an approved finding arrives, and again if a second reply follows. The finding must already be approved by its owner and must say what was found, what the requirement is and what was asked.

Do not use it:

- to raise a finding or write to a supplier. Use the supplier issue notice capability for that;
- to track a supplier's record over many findings. Use the supplier performance scorecard capability;
- to investigate a quality problem inside your own company. Use the incident investigation and corrective actions capability;
- to decide who is at fault, what the supplier owes, or whether commercial terms have been breached;
- to judge whether a cause is technically correct. The check can show that a cause leaves failures unexplained; a qualified person judges whether it is right.

## Roles

- **Runs it:** the quality technician, buyer or whoever handles the supplier's reply.
- **Decides whether the reply is accepted, and whether the finding closes:** the supplier-quality owner, a person the company names.
- **Verifies each action:** the person the agreed responsibilities name. The assistant never marks an action verified.
- **Contacts the supplier:** a person, using the evidence list as a starting point. The assistant writes nothing to the supplier.

## Inputs

1. **The approved finding,** as text with these labels: `Finding ref`, `Status`, `Supplier`, `Item`, `Requirement`, `Raised`, `Reply due`, `Found`, `Sample and failures`, `Lots in scope`, `Requested of the supplier` (numbered R1, R2 and so on) and `Verification criteria`. Add any further labelled facts the owner wants checked, such as `Cavity marks on the failed units`. If a label is missing, or the status does not say the finding is approved, stop and ask. Never guess a missing label.
2. **The supplier's reply,** pasted exactly as received, with the date received and the sender's role. If the date received is missing, stop and ask.
3. **The attachments list,** a spreadsheet export or typed list, one row per attachment. Default column headers: `attachment_ref, description, date`. If a header does not match, stop, show the expected and the found headers, and ask which column is which. Never guess. If nothing was attached, say "no attachments listed" and continue. The assistant reads only the descriptions and any attachment text the person pastes; it does not claim to have seen a file it was not given.
4. **The agreed quality responsibilities,** as pasted text: the reply period, what a reply must cover, who verifies, and any escalation route. If missing, write "responsibilities not supplied" and use only what the finding states.
5. **Settings:**
   - today's date. If missing, ask;
   - the working days of the week and any closed dates in the period. If the working days are missing, use Monday to Friday and say so;
   - the owner's role;
   - [your next scheduled delivery], the date of the supplier's next delivery of the item, if any. If missing, write "not supplied" and skip the timing check in step 9.

The assistant works only from what the person supplies. It needs no access to any system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Stop if a finding label is missing, if the status is not approved, if the reply has no received date, or if an attachments header does not match. Check that any counts in the finding add up (for example, failure counts by category against the failures stated). If they do not, stop and show the figures.
2. **Check the timing.** Take the reply due date from the finding. If the responsibilities give a reply period, count it in working days from the working day after the date raised (a period of 5 working days from Tuesday 27 October ends on Tuesday 3 November) and compare. If the two dates differ, show both and ask which stands. Then count the working days from the due date to the date received. Print "on time" or "[n] working days late". Count only the working days and closed dates supplied.
3. **Number the statements.** Read the reply once and give each separate claim or promise a number, S1, S2 and so on, in reading order. A sentence holding two claims becomes two statements. Greetings and thanks take no number. Keep the supplier's meaning; shorten the words, never change the facts. Give each statement a kind: action reported done, action promised, statement of cause, position on the finding, or other.
4. **Set each request against the reply.** For each numbered request in the finding, list the statements that answer it. Give the request one status:
   - **Addressed in full:** the reply covers every part of what the request asked, including any owner, date, quantity or evidence it asked for;
   - **Addressed in part:** the reply covers some parts and leaves others out. Say which are left out;
   - **Not addressed:** no statement answers it;
   - **Disputed:** the reply says the finding or the request is wrong. Give the grounds in the supplier's words, briefly, and do not rule on them.
   A status describes what the reply covers, never the quality of the answer. A request for a cause, a plan or a proposal is Addressed in full when one is stated and everything the request asked for with it is given, even if the cause leaves failures unexplained or the plan is thin; that gap goes in step 5, never in the status. "Addressed in full" does not mean accepted. A request for something that cannot exist yet, such as results for later lots, is Not addressed unless a statement answers it; step 10 asks when it is expected.
5. **Compare with the records.** Check every lot, quantity, date, part number and count in the reply against the finding. Check every lot and quantity in scope in the finding against the reply. List each difference, each lot in scope that the reply does not mention, each statement too vague to check (for example "the remaining stock", "soon", "all affected parts"), and anything the reply raises that the finding does not cover. A commercial remark such as "at our cost" stays with its statement and is listed as not in the finding, with no view on it. Give each a number, D1, D2 and so on, in this order of type: differs, not mentioned, unclear, timing, not in the finding. Where the finding records a breakdown of the failures (by cavity, line, shift, operator role or similar), check whether the stated cause accounts for all of it, and say which part it leaves out.
6. **List the actions proposed.** Every statement of kind action reported done or action promised becomes a line with its action, who is to do it, the date, and one state:
   - **Promised:** the action is stated as future;
   - **Reported done, no evidence:** the supplier says it is done and no attachment shows it;
   - **Reported done, evidence supplied:** the supplier says it is done and an attachment's description shows it. Name the attachment.
   A plan, a draft or a photo of the problem is not evidence that an action is done. A promised action is never described as completed, and no state ever reads "verified". Count the actions by state. List the statements that are not actions.
7. **List the attachments and the evidence to ask for.** For each attachment, say which statement it supports and what it does not show. Then list the evidence still worth asking for, E1, E2 and so on: one line each, naming the request or statement it belongs to and the fact that makes it necessary. Ask only for evidence tied to a gap found in steps 4 to 6. Ask for nothing outside the finding.
8. **List what is still to be verified.** For each request that involves an action or a result, V1, V2 and so on (a request that asks only for a statement or an explanation has none; its gaps are in D and E): what must be seen, the criterion exactly as the finding states it, or "not stated; owner to set", and the earliest date it can be checked, taken from the dates in the reply, or "now", or "no date given". Do not invent a criterion, and do not decide a test is passed.
9. **Check the delivery calendar.** If [your next scheduled delivery] was supplied, compare it with the dates of the actions that change the product or the process. Report each action dated after that delivery, and each dated before it but supported only by a plan, under D as timing. Say how many days apart they are, counted in calendar days. Do not decide whether that delivery should be inspected, held or counted toward any criterion; ask.
10. **Write the questions.** One for each difference, each unmentioned lot, each unclear statement and each timing point, and one for each request that is addressed in part or not addressed and has no question yet. Each question is one the owner settles, or decides whether to put to the supplier; the assistant puts none. A question asks. It does not recommend, rank urgency or say what a result means.
11. **Close.** Print the counts: requests not addressed in full out of all requests, and actions proposed, none verified by this check. List the owner's options, without recommending one. Use the closing line exactly. Return the check to the person who ran it, for the owner.

## Exceptions and stop conditions

- **A finding label missing, or the finding not approved:** stop and ask. A reply cannot be checked against a finding that has not been fixed.
- **The reply has no received date:** stop and ask.
- **An attachments header does not match:** stop, show the expected and the found headers, and ask.
- **Counts in the finding do not add up:** stop and show the figures.
- **The reply is not from the supplier named in the finding, or refers to a different part or finding reference:** stop and ask before comparing anything.
- **Two reply dates, or a second reply:** run the check on the reply the person names, and say which. Do not merge replies.
- **The reply disputes the finding:** record it as disputed with the supplier's grounds. Do not rule on them.
- **Asked to accept the reply, close or reopen the finding, mark an action verified, or say the supplier has complied:** decline. The owner decides.
- **Asked to write to the supplier, set a deadline, or state a consequence:** decline and point to the supplier issue notice capability for a notice a person will approve and send.
- **Asked about fault, charges, penalties, breach, or ending a supply relationship:** decline; those decisions belong to the people the company names.
- **Asked to judge whether the supplier's technical cause is correct:** decline; show only what the cause leaves unexplained in the records.

## Output format

```
SUPPLIER QUALITY RESPONSE CHECK: [finding ref], [supplier]

For: [owner role]. Prepared [today's date] from the finding, the reply and the records supplied.

Inputs checked: finding [ref], [status]; reply received [date] from [sender role]; [n] attachments listed (or "no attachments listed"); reply period [period, and whether the due date agrees with the finding] (or "responsibilities not supplied"); next scheduled delivery [date or "not supplied"]; escalation route [route or "none stated"]. [Any count in the finding that was checked, and its result.]
Timeliness: reply due [date], received [date], [on time / n working days late].

1. EACH REQUEST AGAINST THE REPLY
R[n]. [The request, in short.]
  Reply: [S refs and what they say, or "nothing".]
  Status: [Addressed in full / Addressed in part / Not addressed / Disputed]. [What is left out, or the supplier's grounds.]
  Evidence supplied: [A refs, or "none".]
Count: [n] requests: [n] addressed in full, [n] in part, [n] not addressed, [n] disputed.

2. WHERE THE REPLY DIFFERS FROM OUR RECORDS OR IS UNCLEAR
D[n]. [Differs / Not mentioned / Unclear / Timing / Not in the finding]. [The facts, with the S ref and the record they are set against.]
[If none: None.]

3. ACTIONS PROPOSED
S[n]. [Action]. By: [role or "not named"]. When: [date or "no date"]. State: [Promised / Reported done, no evidence / Reported done, evidence supplied: A refs]. [Note, if the evidence is a plan or draft.]
Count: [n] actions: [n] promised, [n] reported done with no evidence, [n] reported done with evidence supplied.
Not actions: [S refs and kind, or "none"].
[If no actions: None proposed.]

4. ATTACHMENTS AND EVIDENCE TO ASK FOR
Received:
A[n]. [Description]. Supports: [S ref and what it shows]. Does not show: [what].
[If none: No attachments.]
Evidence to ask for:
E[n]. [Evidence]. For [R or S refs]. Why: [the fact, with its D ref if any].
[If none: None.]

5. STILL TO BE VERIFIED
V[n]. [R ref]: [what must be seen]. Criterion: [as the finding states it, or "not stated; owner to set"]. Earliest check: [date, "now" or "no date given"].
[If none: None.]

6. FOR THE OWNER
Open: [n] of [n] requests are not addressed in full; [n] actions proposed, none verified by this check.
Questions:
[n]. [Question, with its D, E or R refs.]
[If none: None.]
Options, none recommended: (a) accept the response as it stands; (b) accept the actions proposed and keep the finding open until they are verified; (c) ask the supplier for the evidence in [E refs, or "none"]; (d) escalate by the route in the agreed responsibilities ([route or "none stated"]).

This check compares the reply with the finding and the records supplied. It does not accept the reply, close the finding, verify any action, or write to the supplier. The [owner role] decides, and nothing has been sent or changed.
```

## Reviewer checklist

1. Every request in the finding appears in section 1 under its own number, in short. (Quality technician)
2. Each status follows from the statements listed against it, and "Addressed in full" is used only where every part of the request is covered. A gap in the quality of an answer, such as a cause that leaves failures unexplained, is in section 2 and not in the status. (Owner)
3. The numbers recompute: working days late, days between dates, the totals in each count line, and the sum of the request statuses. (Quality technician)
4. No action is described as completed or verified unless the supplier says so and an attachment shows it, and none is described as verified. (Owner)
5. Every difference is set against a named record, and every lot in scope is either answered or listed as not mentioned. (Quality technician)
6. Every request for evidence is tied to a gap found in sections 1 to 3. (Owner)
7. Each criterion in section 5 is the finding's own wording, or says that it is not stated. (Owner)
8. The questions ask and recommend nothing, and no option is recommended. (Owner)
9. Nothing in the check accepts the reply, closes the finding, blames the supplier or writes to the supplier. (Owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal reply.** A finding with five requests and a reply that answers some of them. Expected: each request has exactly one status; the counts add up to five; nothing is marked accepted.
2. **Late reply.** Reply due on a Tuesday, received two working days later. Expected: "2 working days late", counted on the working days supplied.
3. **Lot not mentioned.** The finding puts a second lot in scope and the reply never names it. Expected: a "Not mentioned" difference, a request for evidence and a question.
4. **Promised, not done.** The reply says an insert "will be replaced by" a date. Expected: state "Promised", never described as done or verified.
5. **Plan offered as proof.** A draft checklist is attached for a check that starts next week. Expected: the attachment is listed as supporting the plan, with "does not show: that the check is in use".
6. **Cause leaves failures unexplained.** The finding records failures across two categories and the reply names one, with the evidence the request asked for. Expected: the request is "Addressed in full"; a "Differs" item names the category the cause leaves out, with no ruling on whether the cause is right.
7. **Vague statement.** The reply says "we sorted the remaining stock". Expected: an "Unclear" item asking which stock, how many and by what method.
8. **Counts that do not add up.** The finding's failure categories sum to a different number than the failures stated. Expected: stops and shows the figures.
9. **Renamed attachments header.** `description` exported as `details`. Expected: stops, shows both header lists, asks.
10. **Asked to accept.** The user asks the assistant to confirm the reply is satisfactory and close the finding. Expected: declines and names the owner.
11. **Asked to write to the supplier.** Expected: declines and points to the supplier issue notice capability.
12. **Disputed finding.** The reply says the part met the requirement. Expected: status "Disputed" with the supplier's grounds in short, and no ruling.
13. **Two claims in one sentence.** "We sorted the stock and found no defects." Expected: two numbered statements, the first an action reported done, the second of kind other.
14. **Request that cannot be answered yet, and a commercial remark.** The finding asks for results of the next three lots; the reply is silent and offers replacement "at our cost". Expected: the request is "Not addressed" with a question asking when; "at our cost" is listed as not in the finding, with no view.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a supplier quality response check for the owner of a quality
finding. You compare a supplier's reply with the finding and with the
records the person supplies. You never accept a reply, close a finding,
mark an action verified, write to the supplier, blame anyone or change a
record; a person approves and does all of that.

The user will supply: the approved finding with these labels: Finding
ref, Status, Supplier, Item, Requirement, Raised, Reply due, Found,
Sample and failures, Lots in scope, Requested of the supplier (numbered
R1, R2...), Verification criteria; the supplier's reply and the date it
was received; an attachments list with headers attachment_ref,
description, date; the agreed quality responsibilities; today's date,
working days, closed dates, the owner's role and the next scheduled
delivery. If a label is missing, the finding is not approved, the
received date is missing, or a header does not match, stop, say which,
and ask. If counts in the finding do not add up, stop and show them. If
the reply is from another supplier or about another item, stop and ask.
Never ask for a password or a login code.

1. Compare the reply due date with any reply period in the
   responsibilities, counting the period from the working day after the
   date raised. If the two dates differ, show both and ask which stands.
   Then count working days from the due date to the date received, using
   only the working days and closed dates supplied.
2. Number each separate claim or promise in the reply S1, S2... in
   reading order. A sentence holding two claims becomes two statements.
   Skip greetings. Keep the supplier's meaning. Give each a kind: action
   reported done, action promised, statement of cause, position on the
   finding, or other.
3. For each request, list the statements that answer it and give one
   status: Addressed in full (every part covered, including any owner,
   date, quantity or evidence asked for), Addressed in part (say what is
   left out), Not addressed, or Disputed (give the supplier's grounds
   briefly and do not rule on them). A status describes what the reply
   covers, never how good the answer is: a cause given with the evidence
   asked for is Addressed in full even if it leaves failures
   unexplained; put that gap in step 4. A request for something that
   cannot exist yet is Not addressed unless a statement answers it.
4. Compare every lot, quantity, date and count in the reply with the
   finding, and every lot in scope in the finding with the reply. List,
   as D1, D2..., in the order differs, not mentioned, unclear, timing,
   not in the finding. Where the finding records a breakdown of the
   failures, say which part the stated cause leaves unexplained. Do not
   judge whether a cause is technically right. List a commercial remark
   such as "at our cost" as not in the finding, with no view.
5. List each action with who, when, and one state: Promised; Reported
   done, no evidence; Reported done, evidence supplied (name the
   attachment). A plan, draft or photo of the problem is not evidence
   that an action is done. Never write that an action is complete or
   verified unless the supplier says it is done and an attachment shows
   it, and even then never write "verified".
6. List each attachment with what it supports and what it does not show.
   List evidence to ask for as E1, E2..., each tied to a gap and a
   request or statement. Ask for nothing outside the finding.
7. List what is still to be verified as V1, V2... for each request that
   involves an action or a result (none for a request that asks only for
   a statement or explanation), giving the criterion in the finding's
   own words or "not stated; owner to set", and the earliest check as a
   date from the reply, "now" or "no date given". Invent no criterion
   and decide no test.
8. If a next scheduled delivery was supplied, report actions dated after
   it, or before it but supported only by a plan, as timing items, with
   the days apart. Ask whether that delivery counts or is inspected;
   never decide.
9. Write numbered questions that ask only, each one for the owner to
   settle or to decide whether to put to the supplier; you put none.
   Never recommend, rank urgency or say what the reply means for the
   supplier.
10. Use the output format exactly. Print "None." for an empty section.
    Recompute every count, date and day before you print it.
11. Close with the counts (requests not addressed in full out of all
    requests; actions proposed, none verified by this check), the
    options with none recommended, and the closing line exactly. If a
    second reply follows, check only the reply the person names and
    never merge replies.

Decline to accept or reject the reply, close the finding, set deadlines,
state consequences, write to the supplier, or give a view on fault,
charges or the future of the supply relationship. The owner decides.
```

## What to customize

- The labels of your finding record and the numbering of the requests in it.
- The reply period, what a reply must cover, and the escalation route, in your agreed quality responsibilities.
- A verification criterion for each request that has one, such as how many later lots must pass and the sample size.
- [your next scheduled delivery] for each supplier, and the working days and closed dates.
- Who runs the check, who decides, and who verifies each kind of action.
- Where the check is kept, and who may see it.
- Which exports and files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
