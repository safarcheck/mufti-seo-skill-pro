# Ready prompts

Prompts this skill runs on itself when a command is invoked, and prompts a user can paste directly. Replace the bracketed fields. Every output passes `06-humanizer.md` before delivery.

## 1. SEO landing pages (10 prompts)

| # | Job | Prompt |
|---|---|---|
| 1 | Landing page audit | Audit [landing page URL] for SEO issues, search intent match, content gaps, and conversion problems. Fetch the page and the SERP for [target keyword] first. Return the 5 highest-impact fixes with the expected effect of each. |
| 2 | Search intent research | Analyze [target keyword] from the live SERP: identify the dominant intent, the page type the top 10 share, the audience's needs from PAA and related searches, and the landing page structure that would match. |
| 3 | Landing page keyword research | Find primary, secondary, and long-tail keywords for [product or service] targeting [audience] in [location]. Cluster by SERP overlap, label intent, and map each cluster to one page. Mark volumes as estimates with the source. |
| 4 | Title and meta | Write 5 title tags (50 to 60 characters) and 5 meta descriptions (140 to 155 characters) for [landing page topic] using [target keyword], each with a specific benefit and no banned words. State which one you would ship and why. |
| 5 | Landing page copy | Write the landing page copy for [product or service] targeting [audience], following the 8-section structure in `07-on-page.md` § 9. Use the Brand Brief's proof only. Simple words, one benefit per sentence, numbers where they exist, natural keyword placement, no fabricated claims. |
| 6 | Heading structure | Build the H1 to H3 structure for [target keyword] that matches search intent and covers the questions in PAA and the semantic term set. Mark which headings get a 30 to 40 word answer block. |
| 7 | Conversion review | Review [landing page URL] and give specific improvements to copy, calls to action, trust signals, form length, and mobile layout. Quote the current text next to the proposed text for each change. |
| 8 | Internal linking | Analyze [website URL] and propose internal links to [landing page URL]: source URL, paragraph, and entity-precise anchor text for each, plus the links the landing page should send out. |
| 9 | AI search optimization | Improve [landing page URL] for AI Overviews and answer engines: add extractive answers under question headings, dated facts with sources, entity clarity in the first paragraph, FAQ with visible answers, and the schema graph. Check robots.txt and CDN rules for AI crawler access first. |
| 10 | Performance plan | Analyze [landing page URL] using [Search Console data] and [analytics data]. Build a prioritized action plan from impressions, CTR by position, conversions, and user behaviour, with one owner and one metric per action. |

## 2. Strategy and research

- Build a Brand Brief for [URL]. Read the site, fill the template in `01-brand-brief.md`, mark unknowns, and ask me only the questions you could not answer from the site.
- Create a topical map for [niche] with core, mid-tier, and spoke nodes, intent per node, page type, link directions, and build order. Use PAA, related searches, competitor H2s, and the prompts buyers type into AI engines.
- Run keyword research for [topic] and return keywords.csv with intent, modifier type, cluster, estimated volume with source, and the semantic term set per planned page.
- Compare [my URL] with [competitor URL 1], [competitor URL 2], [competitor URL 3]: what they rank for that I don't, which page types they have that I lack, which sources link to 2 or more of them and not to me.
- Build the 6-month AI SEO plan for [business] following `09-aeo-geo-llm.md` § 8, adjusted for a team of [n] people.

## 3. Technical

- Run a technical SEO audit of [URL]: crawlability, indexability, rendering without JavaScript, Core Web Vitals field data, schema validity, sitemaps, mobile, security, hreflang. Severity per finding and the one fix to ship first.
- Generate the JSON-LD graph for [URL]: Organization, WebSite, WebPage, BreadcrumbList, and [Article / Product / LocalBusiness / FAQPage] with `@id` links, using only facts visible on the page. Validate and report errors.
- Check whether AI crawlers can reach [URL]: robots.txt rules per bot, CDN or WAF bot settings, raw HTML content without JavaScript, llms.txt presence. Draft llms.txt from the sitemap.

## 4. Content

- Write a content brief for [topic] targeting [keyword]: competitor summary, outline with word budgets and answer-block markers, semantic term set with placement, 3 depth sections, internal links, schema, 5 titles, 5 metas, visuals, and the claims we must not make.
- Write the article for [brief or topic] following the drafting order in `05-content-writing.md` § 3, then run both edit passes and report the AI garbage score.
- Refresh [URL]: pull its GSC trend, decide keep, refresh, merge, or delete, suggest exactly 5 new sections with the reason competitors miss each, update dated facts, and re-run both edit passes on the result.
- Rewrite the copy for [page] using the outcome rule in `05-content-writing.md` § 6: one benefit per sentence, a moment in the reader's day, proof next to each claim.

## 5. Humanizer

- Humanize this text without changing what it says. List the tells you found, then return the final version. No em dashes, no reframes, no tier-1 words, no chatbot residue. Add nothing that is not in the source.
- Score this draft for AI garbage using the table in `06-humanizer.md` § 10 and show the first example of each failing row.
- Here is a 150-word sample of my writing: [sample]. Rewrite [text] in this voice, matching sentence length, punctuation, and openings.

## 6. AEO and GEO

- For [URL], list the PAA questions for [keyword], mark which have a heading and an answer block, draft the missing 30 to 40 word answers, and recommend the snippet format from the SERP.
- Audit [brand] for AI citations: run these 20 buyer prompts in ChatGPT, Perplexity, and Gemini, log mentions and cited URLs, list the third-party pages cited most, and give the outreach targets.
- Make [URL] more citable: quotable sentences with numbers and dates, entity clarity in the first paragraph, sources named, comparison table, update log, FAQ with visible answers.

## 7. Authority

- Analyze the backlink profile of [URL] from [source]: referring domains, anchor distribution, toxic signals, and the domains linking to 2 or more of [competitors] but not to us. Label all metrics as estimates with the date.
- Find unlinked mentions of [brand] and draft a 3-sentence request for each with the exact sentence, the suggested link target, and the editor contact.
- Find the top 20 "best [category]" and "[competitor] alternatives" pages, check whether [brand] is listed and described accurately, and draft the paragraph each editor could paste.

## 8. Local and ecommerce

- Audit the local SEO of [URL] for [city]: GBP, NAP consistency across the top directories, review velocity and responses, LocalBusiness schema, location page quality. Output the mismatch list and the JSON-LD.
- Audit [category URL]: copy, facet indexation rules, pagination, internal links, breadcrumb schema. Then audit [product URL]: unique copy, Product schema with offers, variants, images, reviews.

## 9. Measurement

- From this GSC export (16 months), find: position 4 to 15 opportunities, high-impression low-CTR pages, decaying pages, cannibalised queries, and new queries with no page. One action per finding.
- Write the monthly SEO report for [site] in the order in `12-measurement.md` § 8, with date ranges and sources on every number, under one page, in human voice.
- Create a drift baseline for the top 50 URLs of [site] (status, canonical, robots, title, meta, H1, word count, internal links, schema types, LCP image) and the compare script to run after each deploy.
