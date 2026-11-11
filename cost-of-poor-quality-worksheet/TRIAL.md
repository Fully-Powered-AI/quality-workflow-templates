# Trial of the cost of poor quality worksheet on its own invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (claude-sonnet-5-5)
- **Date:** 2026-11-10

The inputs for this trial are the invented example in `public/example.md` (Orrin Hollow Workshop, July to September 2026): the 15 failure rows, the 3 prevention and appraisal rows and the settings. No client data was used. The model that ran it did not write the template.

## How the trial was run

The model followed the fenced instruction block and the output format in `member/template.md` on those inputs and worked out every figure by hand from the rows. One flaw in the method: the file was printed in a single command, so the example's published output was on screen before the worksheet was written. The figures below were still recomputed from the rows, but the wording of the output was not produced blind.

## What came out

All ten sections and the closing line were produced. The figures were:

- Coverage: 14 failure rows in the period (F15 is dated 2026-06-28 and was left out); F07 held out as a possible duplicate of F06 (both cite SW-4 at $2,240.00); 13 counted, 12 with a known cost, 1 with none (F14).
- Rework: 5 rows, $1,392.00, all estimated (hours times $32.00); 1 row with no cost. Scrap: 3 rows, $4,850.00 recorded. Re-inspection: 1 row, $192.00 estimated. Internal total $6,434.00.
- Customer return $540.00, Credit or refund $1,710.00, Replacement $610.00. External total $2,860.00.
- No category: 1 row (F11), $380.00.
- Total known failure cost $9,674.00: $8,090.00 recorded, $1,584.00 estimated.
- By process or product: Wardrobe frames $3,298.00 (34%), Drawer units $2,934.00 (30%), Door line $2,092.00 (22%), not assigned $1,350.00 (14%). The shares add to 100.
- Estimates: F01 $384.00, F03 $304.00, F08 $448.00, F09 $192.00, F13 $256.00; total $1,584.00.
- Prevention and appraisal: $700.00 known, 1 row (P3) with no amount, shown beside the failure costs.
- Total if the held-out F07 were also counted: $11,914.00.
- Six questions: F07 and F06 duplicate or not; the split of INV-908; the products behind SW-9; the cost of F14; whether finance wants more than wages in the labor rate; the cost of P3.

## What was observed

- Every required part was produced and every total recomputed. Internal plus external plus no category equals the total; recorded plus estimated equals the known cost in every line; the product amounts add to the same total.
- The output matched the published example in every figure, count and percentage. The differences were in wording only, and the model's wording followed the example closely because it had been seen.
- Nothing in the instructions made the model stop. No header mismatch, repeated reference, malformed date or amount, second currency, name or account number was present.
- Every fact in the output is in the inputs. The example's closing "checks" paragraph is not part of the format and was not reproduced.

Ambiguities and weak points met:

1. The "Prepared from [n] failure rows" line does not say whether n counts rows read (15) or rows in the period (14). The example uses 15; the template should say so.
2. A row that is both a category gap and a product gap, or one that is a gap and a duplicate, has no stated order of treatment. It did not arise here.
3. The duplicate rule is mechanical: same `source_ref` and same amount. F07 is described as "offcut waste" and F06 as "frames binned", which may be two real costs. The template holds F07 out and asks, which is the intended result, but it relies on the question being read.
4. Section 5 says the row is "counted in the total as [where]". For F11 the model had to decide whether Drawer units should also appear, and chose to show it under both "No category" and its product, following the example. The procedure supports this but does not say it plainly.
5. Section 2 counts F14 (no cost) against Drawer units. Procedure step 7 says to count rows with no cost, so this is supported, but the format line is easy to misread as counting held-out rows too.
6. The currency is given as "dollars" in the settings, and the format uses "$". The template does not say how to render the symbol.
7. The procedure lists 12 steps and the instruction block 10. They agree in substance. The instruction block has one irregular line break in step 2 and is otherwise usable.
8. The "Acceptance tests" are marked proposed and none was run. This trial covers only the normal-quarter case, with the same-write-off, no-category, no-product, blank-amount and outside-the-period cases all present in one set of rows. The stop conditions were not exercised.

This is one run, by one model, on one invented example. It shows the template can be followed to the published result, not that it works on real exports.

## Edits after the independent review, 10 November 2026

The run above is unchanged. After an independent review the template and example were edited, and this section records what that did and did not involve.

- The "Prepared" line now says the counts are rows read, including any outside the period, and the example line was reworded to match (15 failure rows read, 3 prevention and appraisal rows read). Weak point 1 above is addressed. Only the wording of that line changed; the example's figures did not.
- The long line in step 2 of the instruction block (weak point 7) was re-wrapped.
- Rules that were in the procedure but not in the instruction block were added to it: the stop when no failure row falls inside the period, the "prevention and appraisal costs not supplied" line, and the "hours known, no approved rate" case with its question. Weak points 2 and 4 above are addressed with one sentence each: duplicates are checked before allocations and a held-out row is listed only in section 6; a row missing both category and product is listed once and appears under both; a row missing one still appears under the other.
- Step 10 of the procedure now says the treatment of rows with no basis is listed only if such a row was counted, and step 11 now covers a prevention or appraisal row with no amount, which is the kind of question the example's question 6 asks.

- After a second review pass: the settings now state the business name and the reader, and the instruction block and Inputs item 3 now say amounts are printed with the currency's usual symbol and two decimals (weak point 6 above). Step 9 of the instruction block now lists the kinds of question, matching procedure step 11. A short note under the output format says a held-out duplicate is never counted as a row with no cost (weak points 3 and 5). The example's worksheet text and figures are unchanged.

The template was not run again after these edits. The new rules cover cases the example does not contain (no rows in the period, a missing prevention and appraisal export, hours with no rate, a row missing both category and product, a duplicate with a gap), so a re-run on the example would not have exercised them. They have not been tried. A second run without the published output in view has not been done, and the first run remains the only one.
