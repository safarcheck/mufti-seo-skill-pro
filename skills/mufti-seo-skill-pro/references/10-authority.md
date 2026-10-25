# Authority: backlinks, mentions, digital PR, citations

Links still rank pages. Brand mentions on the sources AI engines cite now decide whether the brand appears in answers. Both are earned with assets worth referencing and outreach a person would actually reply to.

## 1. Backlink profile analysis

From whatever source is available (GSC Links report, Bing Webmaster Tools, Moz, Common Crawl, DataForSEO, Ahrefs; see `14-integrations.md`), report:

- Referring domains (count, trend), top linked pages, anchor text distribution (brand, naked URL, generic, exact match; exact-match above 10% is a risk signal).
- Link quality: relevance to the topic, traffic of the linking page, placement (in-content vs footer or sidebar), follow vs nofollow or UGC or sponsored.
- Toxic signals: link networks, paid link footprints, foreign-language spam, hacked sites. Disavow only for manual actions or clear negative SEO; Google ignores most spam on its own.
- Gaps: domains linking to 2 or more competitors and not to you (highest-probability prospects).

Label all third-party metrics as estimates with the source and date.

## 2. Link-worthy assets (build before outreach)

Nobody links to a service page. They link to:

- Original data: a survey, an index, a benchmark, a price tracker, a yearly report with a stable URL that updates.
- Tools: calculators, checkers, templates, generators tied to the topic.
- Definitive guides that answer the cluster better than anything on page 1 (`05-content-writing.md` § 4).
- Visuals: charts and diagrams others embed with credit (`create-geo-charts` from gtm-engineer-skills produces AI-citable charts when installed).
- Expert commentary: a named person with credentials who answers journalists fast.

Pick one asset per quarter and build it properly instead of five thin ones.

## 3. Unlinked brand mentions

Search for the brand name, product names, founders, and unique data points without a link to the site (web search, Google Alerts, Mention, Bing). For each: URL, context, author or editor contact, the exact sentence, the requested link target, a 3-sentence request. Conversion on unlinked mentions is the highest of any tactic because the author already chose to mention you.

## 4. Listicles and "best of" pages (the GEO lever)

AI engines build recommendations from the "best {category}" and "{competitor} alternatives" pages that already rank. For the category:

1. Collect the top 20 listicles and alternatives pages ranking for the category's investigative keywords.
2. For each: are you listed, at what position, with what description, and is the description accurate?
3. Outreach to be added or corrected: give the editor the exact paragraph (accurate, specific, in their style), a product screenshot, pricing, and a reason the inclusion helps their readers.
4. Review platforms (G2, Capterra, Trustpilot, Product Hunt, app stores, industry directories): complete profiles with consistent facts, real reviews requested from real customers, no incentives that violate platform rules.

## 5. Digital PR

A campaign needs a story a journalist can publish: new data, a counter-intuitive finding, a timely angle, a named expert. Plan: hypothesis → data collection (own data, survey, public datasets) → the 3 headline findings → assets (chart, press page, methodology) → target list (publications and writers who covered the topic in the last 12 months, with their past article URLs) → pitch (subject line under 8 words; the finding in the first sentence; why their readers care; the asset link; 5 sentences total) → follow-up once after 4 business days.

Never fabricate data, quotes, or survey sizes. A retracted story costs more than no story.

## 6. Community: Reddit, Quora, forums, Hacker News

- Find threads where buyers ask the category's questions (search `site:reddit.com {question}`, Quora, niche forums). `reddit-opportunity-research` from gtm-engineer-skills automates this when installed.
- Answer the question fully in the thread, with specifics, before mentioning the product. Disclose affiliation. Link only when the link is the best answer.
- These threads rank, get cited by AI engines, and shape the language buyers use. Log the ones where the brand is now mentioned.

## 7. Outreach writing rules

Every outreach email passes `06-humanizer.md`. Additionally: one request per email; the recipient's name and the exact page or sentence you refer to; what is in it for their readers; no "I hope this email finds you well"; no "I'm reaching out because"; no flattery paragraph; under 120 words; a subject line that says what the email is.

## 8. What this department refuses

Paid links without `rel="sponsored"`, PBNs, link exchanges at scale, automated directory submissions, comment spam, fake reviews, expired-domain redirects for equity, and any scheme that trades money for follow links. These earn manual actions and lose AI trust. Say so, and offer the asset route.

## 9. Deliverable (`links` command)

Backlink summary (§ 1), the asset to build (§ 2), unlinked mention list with drafts (§ 3), listicle coverage table and outreach drafts (§ 4), PR angle if data exists (§ 5), community thread list (§ 6). Prioritised by expected citations and links per hour of work.
