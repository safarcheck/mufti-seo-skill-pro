# Content: briefs, drafts, depth, EEAT, copywriting, refresh

Content here means anything a reader sees: articles, landing pages, product copy, FAQs, comparison pages, outreach emails. Structure rules come from `04-semantic-seo.md`; sentence rules from `06-humanizer.md`. This file covers the work between them.

## 1. Intake for any piece

Confirm before outlining:

- Macro context in one sentence (propose it if the request is vague, then confirm).
- Query intent and page type from the SERP (`03-research.md` § 3).
- The one reader: "a founder who ran payroll in a spreadsheet for 2 years and just hired employee number 12", not "business owners".
- Position in the topical map: hub or spoke; what it links up to, down to, laterally.
- Proof available from the Brand Brief: numbers, cases, screenshots, named authors.
- CTA and where intent puts it (soft and late for informational; early and repeated for transactional).

## 2. Content brief (`brief-content` command)

A brief lets anyone, human or model, write the page right the first time. Include:

1. Primary keyword, secondary keywords, intent, page type, target URL, map node.
2. The macro context sentence and the reader.
3. Competitor summary: top 5 URLs, what each covers, word count, what all of them repeat, what all of them miss.
4. Outline: H1, H2s, H3s in order, with per-section purpose and word budget. Mark question headings that get an extractive answer.
5. Semantic term set with placement (`03-research.md` § 6).
6. Depth sections (§ 4): at least 3, named.
7. Internal links in and out with anchor text; external sources to cite (real, with URLs).
8. Proof to include: which numbers, which case, which author.
9. Schema to add (Article, FAQPage, HowTo, Product, Organization as fits).
10. Title and meta description options (`07-on-page.md` § 1 and § 2).
11. Visual placements as `[VISUAL: description]`.
12. What the piece must not say (from the brief's "never claim" list).

If claude-seo is installed, `/seo content-brief <topic>` produces the competitive data for items 3 and 5; apply this structure on top.

## 3. Drafting order

Per section:

1. The extractive answer under a question heading (clinical, 30 to 40 words).
2. Body in human voice: paragraphs of 1 to 3 sentences, varied rhythm, contractions, direct address, digits for numbers, a specific within two sentences of every strong claim.
3. Entities with attributes, relationships explicit.
4. The internal link where the paragraph earns it.

Write the page in order from top to bottom; a reader should get 80% of the value in 30 seconds of scrolling: front-loaded answers, bold on the first 2 to 4 words of key bullets, warnings and formulas in callouts, tables for anything with 3 or more attributes to compare.

## 4. Depth and information gain

Google rewards what page 1 does not already say. Before drafting, read the top results and note what every one of them repeats. Then add at least 3 of:

- A section 95% of competitors skip: the edge case, the exception, when the standard advice backfires and which variable flips it.
- Myth vs reality: specific misconceptions, outdated advice, overhyped tactics, each answered with evidence.
- One advanced section explicitly not for beginners: scaling problems, expert workflows, the second-order effects.
- Original data: a test you ran, numbers you own, a small survey, real budgets. One real data point outranks 500 words of restated consensus.
- A real case with names, numbers, and outcome (with permission).
- A decision tool: a table, decision tree, calculator, or checklist that resolves the reader's actual choice.

If none of these exist, ask the user for one. Never invent the data to fill the slot.

## 5. EEAT signals that can be shown, not claimed

- Named author with a real bio, credentials, and a link to profiles (schema `author` and `sameAs`).
- First-hand phrasing only when the hands were there: "In our test of 4 payroll tools over 30 days, 2 miscalculated PF" is allowed only if the test happened.
- Documented mistakes: what went wrong, what it cost, what changed.
- Dated facts with sources: "As of March 2026, the limit is ₹21,000 (EPFO circular, link)".
- Update log on the page: what changed and when.
- Citations to primary sources (laws, standards, vendor docs, studies by name), never "studies show".

## 6. Copywriting rule for anything that sells

Write the outcome in the reader's day, not the feature in your product.

| Weak (feature, adjective) | Strong (outcome, specific) |
|---|---|
| Our tax service is fast. | File your taxes without spending your entire Sunday on paperwork. |
| Powerful reporting dashboard. | See which 3 clients are late before you open your inbox on Monday. |
| Easy to use. | Your first payroll run takes 12 minutes; the second takes 4. |

Rules: one benefit per sentence; a number or a moment in time whenever one exists; the reader's word for the problem, not the industry's; proof next to the claim (customer count, result, screenshot); CTA text says what happens next ("See the 12-minute setup"), not "Submit".

## 7. Refresh, consolidation, and decay (`refresh` command)

Audit the existing URL with the same evidence standard as a new page:

1. **Decay check** (GSC, last 16 months): clicks and impressions trend, queries lost, position drops. A page losing 30% of clicks year over year goes on the refresh queue.
2. **Decision per URL**: keep, refresh, merge (consolidate cannibalising pages into the strongest URL with 301s), redirect, or delete (noindex then remove when nothing links in).
3. **Refresh protocol**: do not rewrite what works. Suggest exactly 5 new sections, each with heading, why competitors miss it, why Google rewards it (name the signal), 4 to 5 points to cover, the reader's takeaway, and the best format (table, checklist, decision tree, case, framework). Reject any suggestion that could be pasted into a competitor's article unchanged.
4. **Update the facts**: dates, prices, versions, screenshots, broken links, outdated claims. Add the update note and date.
5. **Re-run both passes** (Pass A in 04 § 8, Pass B in 06 § 9) on the merged result; older content is where AI phrasing and metronome rhythm hide.
6. **Performance fixes** for pages that rank but do not earn: title and meta for CTR (position 4 to 15 with low CTR), answer block for snippet capture, CTA placement by intent, page speed.

## 8. Delivery

Markdown file with front matter (title, description, slug, date, author, primary keyword, map node, schema types). Then a short block: proof used, sources cited, what was skipped or not verified, and the one next article in the map to link to.
