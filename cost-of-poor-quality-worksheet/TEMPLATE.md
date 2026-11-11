# Cost of poor quality worksheet

Capability template, version 0.1.0.

## Purpose

Prepare one worksheet of the failure costs a business already has on record for a period: rework, scrap, re-inspection, customer returns, credits and replacements. Each cost is sorted into the company's own category, shown with how it is known (recorded, or estimated from hours and an approved rate), and totalled. Costs nobody has put a figure on stay unknown. Costs that cannot yet be placed in a category or a product are listed as unresolved allocations, rows that look counted twice are held out, and every assumption used is written down. Prevention and appraisal costs, if supplied, are shown beside the failure costs and are not netted against them. The assistant prepares; it invents no cost, claims no saving, ranks nothing as a priority and certifies nothing. The owner decides what to fix first, after finance has confirmed the cost basis.

## When to use it and when not to

Use it when failures recur and nobody can say what they add up to, before a planning or pricing round, or at a set rhythm such as each quarter. Run it again when a late export arrives or finance changes the cost basis.

Do not use it:

- to work out why a failure happened or what to do about it. Use repeat incident pattern review for patterns across events; the cause belongs to a person who investigates;
- to cost an imported product. Use product landed cost worksheet instead;
- to explain why spending differs from the budget. Use budget versus actual variance commentary instead;
- to forecast savings or the return on a fix. A proposal is not a cost on record;
- when there are no failure records at all. The worksheet cannot guess what was never written down.

## Roles

- **Runs it:** the owner, operations lead or quality lead.
- **Confirms the cost basis** (labor rate, how credits and returns are counted, which costs belong): the finance contact.
- **Knows the work and resolves unresolved allocations and possible duplicates:** the process owner or whoever keeps the records.
- **Decides what to fix first:** the owner or quality lead, after finance has confirmed the basis.

## Inputs

1. **The failure cost export for the period,** one row per failure cost, with these default headers: `record_ref, date, category, process_or_product, description, quantity, hours, cost_amount, cost_basis, source_ref`.
   - `record_ref` is unique. `date` is YYYY-MM-DD. `category` is one of the company's categories, spelled exactly. `process_or_product` names the process or product the cost belongs to. `quantity` is the count of items affected, if known. `hours` is labor time, if known. `cost_amount` is a number in the one currency, or blank when not known. `cost_basis` is Recorded (taken from the books, an invoice, a credit note or a write-off) or Estimated (worked out by someone), or blank. `source_ref` is the document the figure came from, such as a credit note number.
   - If a header does not match, stop, show the expected and the found headers, and ask. If the export is missing, stop.
2. **Prevention and appraisal costs,** optional, with the default headers: `cost_ref, date, category, description, cost_amount, cost_basis, source_ref`. The category is Prevention or Appraisal. Header mismatch: stop and ask. If the export is missing, write "prevention and appraisal costs not supplied" in section 7 and continue.
3. **The settings.** The business or site name, who the worksheet is for, the period start and end, the currency, and today's date. If the period is missing, stop and ask. Print every amount with the currency's usual symbol before the figure and two decimals (for dollars, "$9,674.00"); in the "Currency:" line, print the currency as it was given.
4. **The category list,** in two groups. Default internal failure: Rework, Scrap, Re-inspection. Default external failure: Customer return, Credit or refund, Replacement. Use the company's list if supplied.
5. **The approved costing basis,** in the finance contact's words: the hourly labor rate (a single number, with what it covers), how a credit note is counted, how a return is counted, and anything else agreed. If no hourly rate is supplied, no cost is worked out from hours. The assistant never chooses a rate, never supplies an industry average and never asks for access to any system.

## The procedure

1. **Check the headers and the data.** Compare each export's headers with the defaults above and stop on a mismatch. Stop on a repeated `record_ref` or `cost_ref`, on a date that is not YYYY-MM-DD, on a `cost_amount` that is not a plain number, or on more than one currency. A blank `cost_amount` is not an error; it means the cost is unknown.
2. **Set the period.** Rows dated inside the period are in scope. List the others in section 9 with their reference, date and amount, and leave them out of every total. Never move a row into the period.
3. **Resolve each cost.** For each in-scope row:
   - if `cost_amount` is present, the cost is that amount, counted as recorded when the basis is Recorded and as estimated when the basis is Estimated. A present amount with a blank basis is counted as estimated, the weaker reading, and raised as a question. If the row also has hours, the amount is used and the hours are not added;
   - if `cost_amount` is blank, `hours` is present and an approved hourly rate was supplied, the cost is hours times the rate, marked Estimated, and written out as "[hours] hours x [rate] = [amount]";
   - otherwise the cost is unknown. List the row in section 4 with what is missing. An unknown cost is never counted as zero and never filled with a typical value.
4. **Find possible duplicates.** Rows that share a non-blank `source_ref` and the same `cost_amount` are a possible duplicate. Count the row with the lowest `record_ref` and hold the others out of every total, listed in section 6 with the amount they would add. Rows that share a `source_ref` but differ in amount are both counted, with a question. Do not merge rows that merely look alike. Run this check before step 5. A row held out as a possible duplicate is listed only in section 6, and its question also names any category or product it lacks.
5. **Find unresolved allocations.** A row with a blank category, a category not on the list, or a blank `process_or_product` is an unresolved allocation. Its amount stays in the total known cost. It appears in the category table as "No category" when its category is the gap, and under "Not assigned to a process or product" in section 2 when its product is the gap. List each in section 5 with what is missing. Never guess a category or a product from the description. A row missing both is listed once in section 5, naming both gaps, and appears under "No category" and under "Not assigned to a process or product". A row missing only one still appears under the other: a row with no category is shown under its product in section 2, and a row with no product is shown under its category in section 1.
6. **Total by category.** For each category on the list, in the order given, count the counted rows and add the known cost, shown as recorded plus estimated. Count the rows with no cost separately. Add the internal group, the external group, the "No category" amount and the total known failure cost. A category with no rows is printed with "no rows".
7. **Show where the known cost sits.** Add the known cost for each `process_or_product`, with its share of the total known cost, rounded to a whole percent, and the number of rows with no cost. Order from the largest known cost to the smallest, with the unassigned amount last. Say that the shares are of known cost only and that the order is not a priority. If the rounded shares do not add to 100, say so.
8. **List the estimates.** One line for each estimated row, and the estimated total. A row worked out from hours is written as hours times the rate; a row whose estimate was supplied is written as "estimate supplied". Name any row that has both hours and an amount, since the amount already stands for that labor.
9. **Show prevention and appraisal.** List each row as supplied, add the known amounts, and count rows with no amount. Do not subtract them from failure costs, do not compare them with failure costs and do not say what the right balance is.
10. **List the assumptions.** Every assumption actually used: the period, the currency, the hourly rate and what it covers, how credit notes and returns are counted, the treatment of rows with no basis (only if such a row was counted), and the rule for duplicates. State only what was supplied or defaulted here.
11. **Write the questions.** One numbered question for each possible duplicate, unresolved allocation, unknown cost, estimate that needs a rate confirmed, basis that needs confirming, and prevention or appraisal row with no amount. Each gives its facts and references. Questions ask. They never recommend, rank, or say what a cost means.
12. **Return the draft** to the person who ran it. The finance contact confirms the basis, and the owner decides what to do. The assistant changes nothing in the books or the exports.

## Exceptions and stop conditions

- **A header does not match, a reference repeats, a date or amount is malformed, or there is more than one currency:** stop; show the problem and ask.
- **No failure rows fall inside the period:** stop and say so; there is nothing to total.
- **Hours are present, no rate was supplied:** list the row as unknown with "hours known, no approved rate"; work out nothing.
- **A name, account number or contact detail appears in a description:** do not repeat it; say which column held it and ask for it to be removed.
- **Asked to guess a missing cost, pick a rate, claim a saving, say which fix to make first, call a cost avoidable, or send the worksheet to anyone:** decline. The owner decides; finance confirms the basis; a person sends.
- **Asked to certify that a total is correct or complete:** decline. The worksheet is only as complete as the records supplied, and the coverage line says what that was.

## Output format

```
COST OF POOR QUALITY WORKSHEET: [business or site], [period start] to [period end]

For: [owner or lead]. Prepared [today's date] from [n] failure rows read, including any outside the period, and [n] prevention and appraisal rows read. Currency: [currency].
Coverage: [n] failure rows in the period; [n] held out as possible duplicates; [n] counted, of which [n] have a known cost and [n] have none.

1. Known failure cost by category
Internal failure
[Category]: [n] rows, known cost [amount] ([amount] recorded, [amount] estimated); [n] rows with no cost.
Internal total: [amount]
External failure
[Category]: [n] rows, known cost [amount] ([amount] recorded, [amount] estimated); [n] rows with no cost.
External total: [amount]
No category: [n] rows, [amount].
Total known failure cost: [amount] ([amount] recorded, [amount] estimated). Rows with no cost: [n].

2. Where the known cost sits
[Process or product]: [amount], [share]% of the known total; [n] rows with no cost.
Not assigned to a process or product: [amount], [share]%.
Shares are of known cost only. The order is not a priority.

3. Estimated costs
[record_ref], [category], [process or product]: [hours] hours x [rate] = [amount], or estimate supplied.
Estimated total: [amount].

4. Rows with no cost
[record_ref], [category], [process or product]: [description]. Missing: [what].

5. Unresolved allocations
[record_ref], [amount]: [what is missing]. Counted in the total as [where].

6. Possible duplicates held out
[record_ref], [amount]: shares [source_ref] with [record_ref]. Counted once. Total known cost if the held-out rows were also counted: [amount].

7. Prevention and appraisal costs, as supplied
[cost_ref], [category], [description]: [amount] or no amount.
Known total: [amount]. Rows with no amount: [n]. Shown beside the failure costs, not netted against them.

8. Assumptions used
[Each assumption, one line.]

9. Rows left out of the period
[record_ref], [date], [amount].

10. Questions
1. [Question, with the facts and references.]

Draft for [owner or lead]'s review. Nothing has been changed, sent or recorded. The cost basis needs the finance contact's confirmation. No saving is claimed, and no priority is set.
```

Print "None." under any section with nothing to list. In section 1, print "no rows" for a category with no rows. A row held out as a possible duplicate is never counted in a "rows with no cost" figure, even if its description differs from the row it is held against; question 1 in such a case asks the person.

## Reviewer checklist

1. Every category total recomputes from the counted rows, and internal plus external plus no category equals the total known failure cost. (Finance contact)
2. Recorded plus estimated equals the known cost in every line. (Finance contact)
3. Every estimate is hours times the approved rate, and no estimate exists without a rate. (Finance contact)
4. No row with a blank amount was counted as zero or given a typical value. (Record keeper)
5. Held-out rows are real duplicates of a counted row, and their total is correct. (Record keeper)
6. Every unresolved allocation is a real gap in the export, and none was filled by guessing. (Process owner)
7. The shares in section 2 recompute from the known total, and the unassigned amount is last. (Finance contact)
8. Prevention and appraisal costs are shown beside, not netted against, the failure costs. (Finance contact)
9. The assumptions list contains only what was supplied or defaulted. (Finance contact)
10. The questions ask and recommend nothing, and no name or account number from the exports was repeated. (Owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal quarter.** Failure rows with recorded amounts, estimated hours and one blank amount. Expected: each category total recomputes, recorded and estimated are split, the blank is listed in section 4 and not counted as zero.
2. **Renamed column.** `process_or_product` exported as `product`. Expected: stops, shows both header lists, asks.
3. **Hours, no rate.** A row with hours and no amount, and no approved rate in the settings. Expected: listed as unknown with "hours known, no approved rate"; nothing worked out.
4. **Same write-off twice.** Two rows with one `source_ref` and one amount. Expected: the lower `record_ref` counted, the other held out and listed, with the total if both were counted.
5. **Same reference, different amounts.** Two rows with one `source_ref` and different amounts. Expected: both counted, with a question; neither held out.
6. **No category.** A row with a blank category and a product. Expected: counted under "No category" and listed in section 5; no category guessed from the description.
7. **No product.** A row with a category and a blank product. Expected: in its category total, shown as "Not assigned to a process or product", and listed in section 5.
8. **Outside the period.** A row dated the day before the period starts. Expected: in section 9 only, in no total.
9. **Two currencies.** Expected: stops and asks.
10. **Asked what to fix first.** Expected: declines, shows where the known cost sits, and says the owner decides.
11. **Asked to estimate a saving.** Expected: declines; no saving is stated.
12. **Name in a description.** Expected: not repeated; the column is named and a person is asked to remove it.

## Instructions for the AI assistant

```
You prepare a cost of poor quality worksheet for an owner or operations
lead. You gather failure costs that are already on record. You invent no
cost, choose no labor rate, claim no saving, rank no priority and certify
nothing. You never change a record or an export, send anything, or pay
anything; a person approves and does all of that. You never ask for a
password or a login code.

The user will supply: a failure cost export with headers record_ref, date,
category, process_or_product, description, quantity, hours, cost_amount,
cost_basis, source_ref; optionally a prevention and appraisal export with
headers cost_ref, date, category, description, cost_amount, cost_basis,
source_ref; the business or site name and who the worksheet is for; the period, the
currency and today's date; the category list
(default internal: Rework, Scrap, Re-inspection; default external:
Customer return, Credit or refund, Replacement); and the approved costing
basis, including any hourly labor rate. If a header does not match, stop,
show expected and found, and ask. If the failure export or the period is
missing, stop and ask. Stop on a repeated reference, a date not in
YYYY-MM-DD, an amount that is not a plain number, or more than one
currency. If no failure row falls inside the period, stop and say so. If
the prevention and appraisal export is missing, write "prevention and
appraisal costs not supplied" in section 7 and continue.

Print every amount with the currency's usual symbol before the figure and
two decimals, such as $9,674.00 for dollars.

1. Rows dated inside the period are in scope. List the others in section 9
   and leave them out of every total.
2. Resolve each cost. A present cost_amount is the cost, with its stated
   basis; a blank basis is counted as estimated and raised as a question.
   If the row also has hours, use the amount and add nothing for the
   hours. A blank cost_amount with hours and an approved rate is hours
   times the rate, marked Estimated and written out. A blank cost_amount
   with hours and no approved rate is an unknown cost, listed in section
   4 as "hours known, no approved rate" and raised as a question; work
   out nothing. Anything else is an unknown cost, listed in section 4.
   Never count an unknown cost as zero and never fill it with a typical
   value or an average.
3. Rows that share a non-blank source_ref and the same cost_amount are a
   possible duplicate: count the row with the lowest record_ref, hold the
   others out of every total, and list them. Rows that share a source_ref
   with different amounts are both counted, with a question. Do this
   before step 4. A held-out row is listed only in section 6, and its
   question names any category or product it lacks.
4. A blank or unlisted category, or a blank process_or_product, is an
   unresolved allocation. Keep its amount in the total, place it under "No
   category" or "Not assigned to a process or product", and list it. Never
   guess either from the description. A row missing both is listed once,
   naming both gaps, and appears under both. A row missing one still
   appears under the other: shown under its product when the category is
   missing, under its category when the product is missing.
5. Total by category in the order given: rows, recorded, estimated, known
   cost, rows with no cost. Add the internal group, the external group, the
   no-category amount and the total known failure cost. Print "no rows" for
   an empty category.
6. Show the known cost by process_or_product with its share of the known
   total as a whole percent, largest first, the unassigned amount last.
   State that shares are of known cost only and the order is not a priority.
7. List the estimates and the estimated total, writing a worked-out row as
   hours times the rate and a supplied estimate as "estimate supplied".
   Name any row that has both hours and an amount.
8. List prevention and appraisal rows as supplied with the known total and
   the rows with no amount. Never net them against failure costs or say
   what balance is right.
9. List only the assumptions actually used. Then write numbered questions
   with their facts and references: one for each possible duplicate,
   unresolved allocation, unknown cost, estimate whose rate needs
   confirming, basis needing confirmation, and prevention or appraisal
   row with no amount. Questions ask; they never recommend or say what a
   cost means.
10. Use the output format exactly. Print "None." for an empty section.
    In the "Prepared" line, count the rows read, including any outside
    the period. Recompute every total, count and percentage before you
    print it.

Never repeat a name, account number or contact detail from a description;
say which column held it. Decline to guess a missing cost, pick a rate,
name a saving, call a cost avoidable, say which fix comes first, certify a
total, or send the worksheet. The owner decides what to fix first, and the
finance contact confirms the cost basis.
```

## What to customize

- Your category list, agreed with finance and kept stable.
- The costing basis finance approves: the labor rate and what it covers, how credits and returns are counted, and which costs belong.
- The period and how often it runs.
- The headers of your own exports, if you change the defaults here, in the instructions and the checks together.
- Who keeps the records, who reads the worksheet and where it is kept.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
