---
name: "cost-of-poor-quality-worksheet"
description: "Prepare one worksheet of the failure costs a business already has on record for a period: rework, scrap, re-inspection, customer returns, credits and replacements. Each cost is sorted into the company's own category, shown with how it is known (recorded, or estimated from hours and an approved rate), and totalled. Costs nobody has put a figure on stay unknown. Costs that cannot yet be placed in a category or a product are listed as unresolved allocations, rows that look counted twice are held out, and every assumption used is written down. Prevention and appraisal costs, if supplied, are shown beside the failure costs and are not netted against them. The assistant prepares; it invents no cost, claims no saving, ranks nothing as a priority and certifies nothing. The owner decides what to fix first, after finance has confirmed the cost basis."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Cost of poor quality worksheet"
---

# Cost of poor quality worksheet

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
