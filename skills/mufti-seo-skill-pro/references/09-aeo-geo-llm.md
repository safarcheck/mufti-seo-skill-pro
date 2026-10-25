# AEO, GEO, AIO, SXO: ranking, getting extracted, getting cited

SEO is three jobs now. Earn the ranking (SEO), become the answer (AEO), get cited and recommended by AI engines (GEO). A fourth, access, decides whether the other three can happen at all.

## 1. The three jobs

| Job | Goal | What it takes |
|---|---|---|
| SEO: earn the ranking | Page 1 for the cluster | Keyword and intent research, technical health, site structure, topical authority, links, EEAT (`03`, `04`, `08`, `10`) |
| AEO: become the answer | Featured snippet, PAA, AI Overview passage, voice answer | Answer the question in the first 30 to 40 words under a question heading; question-style H2s; lists and tables; FAQ, Article, Organization schema (`04` § 5, `07` § 6) |
| GEO: get cited by AI | Mentioned and linked in ChatGPT, Perplexity, Gemini, Claude, Copilot, AI Overviews | Brand mentions on third-party sites, presence in "best of" lists in the niche, quotable stats and sources, consistent entity facts, crawler access (§ 4, § 5, `10`) |

AIO (AI optimisation) is the umbrella term; SXO (search experience optimisation) is § 6.

## 2. AEO: becoming the answer

- Every question heading gets an extractive answer (entity + definitive verb + value + condition, 30 to 40 words). Google lifts these for snippets and AI Overviews; AI engines quote them.
- Cover the PAA set for the cluster as H2s, H3s, or FAQ items. A page that answers 8 of the 10 PAA questions beats one that answers 2 with more words.
- Use the format the SERP already shows for the query: paragraph snippet → definition sentence; list snippet → numbered steps; table snippet → HTML table with header row.
- Passage-level structure: one idea per paragraph, the claim in the first sentence, the evidence after it. Engines index and rank passages, not just pages.
- Dated facts with sources beat undated claims. "As of March 2026" plus a link is quotable; "recently" is not.
- Schema: Article with author, FAQPage for visible FAQs, HowTo for real step content, Organization with `sameAs`.

## 3. GEO: getting cited

AI engines cite sources they trust and sources that make quoting easy. Work both sides:

**On the page**
- Quotable sentences: one clear fact per sentence, with the number and the unit. "Payroll errors cost Indian SMEs an average of ₹1.2 lakh per year (source, 2025)".
- Original data, named studies, first-hand tests: engines prefer primary sources to restatements.
- Entity clarity: the brand's name, category, and what it does stated plainly in the first paragraph of key pages and in Organization schema. "Acme is payroll software for Indian companies with 10 to 500 employees."
- Comparison and "best of" pages on your own site that are honest about competitors; engines pull from comparison pages heavily.
- Freshness: dateModified real, update log visible.
- Markdown or clean HTML delivery: no content locked behind JavaScript, tabs, or accordions.

**Off the page**
- Brand mentions on third-party sites the engines already cite for the category: review sites, directories, industry publications, Reddit and Quora threads, Wikipedia (only when notable), Wikidata entry with consistent facts.
- Presence in the "best {category}" and "{competitor} alternatives" listicles that rank for the niche; see `10-authority.md` § 4.
- Consistent facts everywhere (name, founding year, pricing range, headquarters, founders); engines down-weight entities whose facts conflict across sources.
- Digital PR with a data story engines want to cite.

**Platform notes**
- Google AI Overviews and AI Mode: draw from pages that already rank well and from structured, passage-level answers. Technical SEO and AEO are the entry ticket.
- ChatGPT (with search) and Copilot: lean on Bing's index. Verify Bing indexation (Bing Webmaster Tools, IndexNow).
- Perplexity: cites frequently and visibly; favours pages with clear headings, dates, and sources.
- Gemini: strong tie to Google's index and knowledge graph; entity consistency matters most.

## 4. Access: do not block the bots

One robots.txt line can remove 100% of AI visibility. Check this before optimising anything else.

- Allow (unless the business decides otherwise): `GPTBot`, `OAI-SearchBot`, `ChatGPT-User`, `PerplexityBot`, `Perplexity-User`, `ClaudeBot`, `Claude-SearchBot`, `Claude-User`, `Google-Extended` (controls AI training, not Search or AI Overviews), `Bingbot`, `Applebot-Extended`, `CCBot` (Common Crawl, used by many engines), `Amazonbot`, `Bytespider`, `DuckAssistBot`, `meta-externalagent`.
- Distinguish training bots from search and user-triggered bots. Blocking `GPTBot` stops training; blocking `OAI-SearchBot` removes you from ChatGPT search; blocking `ChatGPT-User` blocks live fetches when a user asks about your page. Decide per bot and document the decision in the Brand Brief.
- Check the CDN and WAF (Cloudflare, Akamai, Vercel) for bot rules that block AI crawlers even when robots.txt allows them; many have an "AI bots" toggle on by default.
- Verify with server logs or the CDN's bot analytics: are the AI user agents actually fetching pages and getting 200s?
- `llms.txt` at the site root: a markdown index of the site's most important pages with one-line descriptions, plus `llms-full.txt` with the content when practical. Google ignores it; some engines and agents read it. Low cost, no downside.
- Content-Signal and similar directives: set them deliberately, document them.

## 5. Entity and brand visibility

- Knowledge panel: Organization schema with `sameAs` to every real profile; consistent NAP; a Wikidata item when the organisation qualifies; the same logo and name everywhere.
- Author entities: Person schema with `sameAs`, `jobTitle`, `worksFor`, `knowsAbout`; author pages with real bios.
- Brand SERP: the first page for the brand name should be yours (site, profiles, reviews, news). Fill gaps with owned profiles.
- Monitor mentions: brand name without a link (`10-authority.md` § 3) and brand name in AI answers (`12-measurement.md` § 5).

## 6. SXO: why a well-optimised page still fails

Search experience optimisation finds the mismatch between what the SERP wants and what the page is:

1. **Page-type check**: the top 10 are guides and the page is a product page (or the reverse). Fix: build the page type the SERP shows, link to the money page from it.
2. **User stories**: from the SERP features and PAA, write 3 to 5 "As a {reader}, I want {thing}, so that {outcome}" stories; score the page against each.
3. **Persona scoring**: read the page as the beginner, the expert, and the buyer; where one of them leaves, the page loses the query.
4. **Zero-click reality**: for queries where the SERP answers in place, the goal is the citation and the brand impression, not the click; optimise the extractive answer and the brand mention, and measure impressions.

## 7. Agent readiness (agentic browsing)

AI agents now browse sites to compare, book, and buy. Make the site usable by them: semantic HTML and a clean accessibility tree, forms with labels, no critical content behind JavaScript-only interactions, structured data for products and offers, clear pricing and availability text, `/.well-known/` discovery files where a standard exists, and a documented API or WebMCP tools when the business wants agents to transact. If claude-seo is installed, `/seo agentic audit <url>` runs the Lighthouse agentic checks.

## 8. The 6-month AI SEO plan (`plan` command default)

| Phase | Days | Work |
|---|---|---|
| 1. AI audit | 1 to 30 | Test 50 buyer prompts across 3+ engines (7 d); allow AI crawlers in robots.txt and CDN (4 d); find prompts where competitors are cited and you are not (7 d); map buyer questions to intent and pages (6 d); list the sources AI already cites for the category (6 d) |
| 2. Entity SEO | 31 to 60 | Make brand name, bio, and facts consistent everywhere (7 d); add Organization, Product, Article, Person schema (6 d); update About, pricing, and comparison pages (9 d); make key pages load without JavaScript (8 d) |
| 3. Answer content | 61 to 100 | Build topic clusters around real prompts (7 d); direct answers in the first two lines of each section (6 d); publish comparison and "best of" pages (10 d); add original data, stats, examples (10 d); refresh old posts with dates and sources (7 d) |
| 4. Citations and PR | 101 to 140 | Get listed on the top listicles and review sites (12 d); earn brand mentions through digital PR (10 d); show up in Reddit and Quora threads with real help (10 d); repurpose content for YouTube and LinkedIn (8 d) |
| 5. Track and scale | 141 to 180 | Track AI visibility, citations, and AI-referred traffic (20 d); fix gaps and scale the prompts that win (20 d) |

Adapt the day counts to team size; keep the order. Phase 1's crawler check happens in week 1 no matter what.

## 9. Deliverables

- `aeo`: per page, question coverage table (PAA question, heading present, answer block present, format match, schema), with the missing blocks drafted.
- `geo`: crawler access report (robots, CDN, log evidence), llms.txt draft, citability score per key page (quotable facts, dates, sources, entity clarity), brand mention gaps, prompt log results, prioritised fixes.
