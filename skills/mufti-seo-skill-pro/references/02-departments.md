# Departments

Ten departments, fifty specialised jobs. The six functions (Research, Technical, Content, On-page, Authority, Measurement) are the same jobs grouped for small teams. Every job reads the Brand Brief first.

## 1. SEO strategy and planning

| # | Job | Delivers |
|---|---|---|
| 1 | SEO strategy builder | Goals, target entities, money pages, 90-day and 12-month targets |
| 2 | SEO audit planner | Which audits to run, in what order, with what tools |
| 3 | SEO roadmap creator | Quarter-by-quarter plan with owners and dependencies |
| 4 | Opportunity prioritisation | Every opportunity scored: impact × confidence ÷ effort |
| 5 | Competitor strategy analysis | What each competitor ranks for, how, and the gaps you can take |

Scoring rule for 4: impact (traffic or revenue potential, 1 to 5), confidence (evidence you can win, 1 to 5), effort (hours or cost, 1 to 5). Score = impact × confidence ÷ effort. Sort descending. Top 5 go on the roadmap first.

## 2. Keyword research and search intent

| # | Job | Delivers |
|---|---|---|
| 6 | Keyword research | Seed → expanded list with volume, difficulty, intent, long-tail variants |
| 7 | Search intent analysis | Intent per keyword from the live SERP, not from guesses |
| 8 | Keyword clustering | Groups by SERP overlap; one page per cluster |
| 9 | Difficulty and opportunity assessment | Where a new or mid-authority site can realistically rank |
| 10 | Keyword-to-page mapping | Every cluster mapped to one URL (existing or planned); no cannibalisation |

See `03-research.md`.

## 3. Technical SEO

| # | Job | Delivers |
|---|---|---|
| 11 | Technical SEO audit | 9-category audit with severity and fix per finding |
| 12 | Crawlability and indexability | robots, canonicals, noindex, redirects, crawl budget, orphan pages |
| 13 | Site architecture optimisation | Click depth, silos, hub and spoke, URL structure |
| 14 | Core Web Vitals analysis | LCP, INP, CLS with field data (CrUX) and lab diagnosis |
| 15 | Structured data and schema markup | Detection, validation, generation, rich result eligibility |

See `08-technical.md`.

## 4. On-page SEO

| # | Job | Delivers |
|---|---|---|
| 16 | On-page SEO audit | Per-URL checklist with before and after |
| 17 | Title tag and meta description optimisation | 5 options each, intent-matched, under pixel limits |
| 18 | Heading structure optimisation | One H1, question H2s, no skipped levels, one macro context |
| 19 | Internal linking optimisation | Hub up, spoke down, lateral across; entity-precise anchors |
| 20 | URL and page structure optimisation | Short, entity-first, lowercase, hyphenated, stable |

See `07-on-page.md`.

## 5. SEO content strategy and production

| # | Job | Delivers |
|---|---|---|
| 21 | SEO content strategy | What to publish, why, in what order, for which cluster |
| 22 | Content gap analysis | Topics competitors cover and you do not; questions nobody answers |
| 23 | Content brief builder | Brief with outline, terms, links, depth sections, word budget per section |
| 24 | Search-optimised content creation | Full draft through the two-pass edit |
| 25 | Topical authority and cluster planning | Topical map with build order |

See `04-semantic-seo.md` and `05-content-writing.md`.

## 6. Content optimisation and refresh

| # | Job | Delivers |
|---|---|---|
| 26 | Existing content audit | Keep, refresh, merge, redirect, or delete per URL |
| 27 | Content refresh planner | Decay detection from GSC, refresh queue by lost clicks |
| 28 | Content consolidation analysis | Cannibalising pages merged into one stronger page with redirects |
| 29 | Content quality and helpful content review | Helpful-content and EEAT review per page |
| 30 | Content performance optimisation | CTR, dwell, scroll, conversion fixes for pages that rank but do not perform |

See `05-content-writing.md` § 7.

## 7. AI search, AEO and GEO

| # | Job | Delivers |
|---|---|---|
| 31 | AI search visibility audit | Where the brand appears (or not) in AI Overviews, ChatGPT, Perplexity, Gemini, Copilot |
| 32 | Answer engine optimisation | Extractive answers, snippet targets, PAA coverage, FAQ schema |
| 33 | Generative engine optimisation | Citability, entity clarity, brand mentions, source quality |
| 34 | AI-friendly content structuring | Passage-level structure, tables, definitions, dated facts |
| 35 | Brand and entity visibility analysis | Knowledge panel, consistent facts, sameAs, Wikipedia and Wikidata presence |

See `09-aeo-geo-llm.md`.

## 8. Off-page SEO and authority

| # | Job | Delivers |
|---|---|---|
| 36 | Backlink profile analysis | Referring domains, anchors, toxic signals, gaps |
| 37 | Link building opportunity research | Prospects ranked by relevance and reachability |
| 38 | Digital PR campaign planning | Data story, assets, target journalists and publications |
| 39 | Unlinked brand mention analysis | Mentions without links, with outreach drafts |
| 40 | Competitor backlink gap analysis | Domains linking to competitors and not to you |

See `10-authority.md`.

## 9. Local and ecommerce SEO

| # | Job | Delivers |
|---|---|---|
| 41 | Local SEO audit | GBP, NAP, citations, reviews, local schema |
| 42 | Google Business Profile optimisation | Categories, services, posts, Q&A, photos, review replies |
| 43 | Local landing page strategy | One real page per location with unique local proof |
| 44 | Ecommerce category page optimisation | Category copy, facets, pagination, internal links |
| 45 | Product page SEO optimisation | Product schema, unique descriptions, reviews, variants |

See `11-local-ecommerce.md`.

## 10. SEO analytics, reporting and automation

| # | Job | Delivers |
|---|---|---|
| 46 | SEO performance reporting | Monthly report: what moved, why, what next |
| 47 | Google Search Console analysis | Queries, pages, CTR gaps, position 4 to 15 opportunities, decay |
| 48 | Organic traffic and conversion analysis | Landing page revenue and assisted conversions |
| 49 | SEO experiment and testing planner | Hypothesis, test and control pages, duration, success metric |
| 50 | SEO workflow automation | Scheduled checks: drift, indexation, CWV, rankings, AI citations |

See `12-measurement.md`.

## The six-function view

| Function | Jobs | Weekly output |
|---|---|---|
| Research | 6 to 10, 22, 31 | Keyword and prompt lists, gaps |
| Technical | 11 to 15 | Fix list with severity |
| Content | 21, 23 to 30, 34 | Briefs, drafts, refreshes |
| On-page | 16 to 20, 32 | Titles, meta, links, answer blocks |
| Authority | 36 to 40, 33, 35 | Prospects, outreach, PR assets |
| Measurement | 46 to 50 | GSC analysis, rank and citation tracking, report |

## Full audit scoring (`audit` command)

Score each department 0 to 10 from observed evidence. Report the 5 lowest scores first with the single fix that moves each most. Never report a department you did not inspect; mark it "not checked" with the reason (no access, tool missing, out of scope).

```
Technical      __/10   top fix:
On-page        __/10   top fix:
Content        __/10   top fix:
AEO / GEO      __/10   top fix:
Authority      __/10   top fix:
Local / Ecom   __/10   top fix:   (or n/a)
Measurement    __/10   top fix:
```

Then: "Fix this first", one item, with what happens if it is skipped.
