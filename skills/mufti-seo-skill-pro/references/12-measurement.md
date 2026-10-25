# Measurement: track citations, not just rank

Measure what the business feels (revenue, leads, signups) and what predicts it (impressions, clicks, positions, citations). Report what changed, why, and what to do next. Never report a metric without its date range and source.

## 1. Google Search Console (the primary source)

Pull 16 months when possible. Analyses that produce actions:

- **Position 4 to 15 with impressions**: queries one push away from page 1; map each to its page and pick the fix (answer block, title, links, depth).
- **High impressions, low CTR** (below the expected CTR for the position): rewrite title and meta for intent; check whether the SERP has features that take the clicks (zero-click; then the goal shifts to citation).
- **Decay**: pages losing clicks year over year; refresh queue (`05-content-writing.md` § 7).
- **Cannibalisation**: one query served by 2 or more URLs with swapping positions; consolidate.
- **New queries**: terms appearing in the last 28 days that no page targets; add to the topical map.
- **Pages with impressions and zero clicks**: wrong page type for the intent (`09-aeo-geo-llm.md` § 6).
- **Index coverage and Page experience**: excluded pages by reason; CWV failures by URL group.
- **AI Overviews**: GSC does not separate AI Overview impressions; use the search appearance filters available and track queries known to trigger AI Overviews manually.

If claude-seo is installed, `/seo google gsc <url>` fetches this through the API; otherwise use a CSV export. Bing Webmaster Tools gives the same for Bing, which feeds ChatGPT search and Copilot.

## 2. Rank tracking

Track the cluster's primary keyword per URL, weekly, from the target country and device. Watch the trend, not the daily number. Record SERP features present (AI Overview, snippet, PAA, local pack, shopping) because they change what a position is worth. Local businesses: geo-grid tracking (claude-seo `/seo maps` when installed).

## 3. Traffic and conversions

GA4 (or Matomo): organic landing pages → sessions → conversions and revenue; assisted conversions for informational pages that start journeys; engagement rate and scroll depth on key pages. Tie each money page to a number the founder recognises.

## 4. AI-referred traffic

Create a channel group for AI referrers: `chatgpt.com`, `chat.openai.com`, `perplexity.ai`, `gemini.google.com`, `copilot.microsoft.com`, `claude.ai`, `you.com`, `bing.com/chat`. Report sessions, landing pages, and conversions from this group monthly. Many AI visits arrive with no referrer; treat the number as a floor.

## 5. AI visibility and citation tracking

The prompt log from `03-research.md` § 5 is the baseline. Weekly or bi-weekly:

1. Run the same 10 to 50 buyer prompts in the same engines (ChatGPT, Perplexity, Gemini, Copilot, Google AI Mode or AI Overviews).
2. Log per prompt and engine: brand mentioned (yes or no), position in the answer, sentiment or accuracy of the description, which competitors were mentioned, which URLs were cited (yours and others).
3. Metrics: mention rate (prompts where the brand appears ÷ prompts), citation rate (prompts citing your URL ÷ prompts), share of voice vs competitors, and the list of third-party URLs cited most often (these become outreach targets in `10-authority.md`).
4. Record who got cited and what got quoted; the quoted passages show what format engines prefer, so copy the format on your pages.

Paid trackers (SE Ranking AI visibility, Profound, DataForSEO AI visibility) automate this when available; the manual log is enough to start.

## 6. Drift monitoring (did a deploy break SEO?)

Before and after any release, snapshot the SEO-critical elements of the top 50 URLs: status code, canonical, meta robots, title, meta description, H1, word count, internal link count, schema types, hreflang, LCP image. Diff them and classify changes by severity. claude-seo's `/seo drift baseline` and `/seo drift compare` do this when installed; otherwise a script with the fields above and a CSV per snapshot.

## 7. Experiments

Hypothesis ("adding answer blocks under question H2s on guide pages raises CTR by 10%"), test group and control group of comparable URLs, one change, 4 to 8 weeks, success metric from GSC, and the decision rule written before the test starts. Report what happened even when the test failed.

## 8. The monthly report

One page. In this order:

1. The 90-day metric from the Brand Brief: current vs target, trend.
2. What moved (top 5 gains and top 5 losses, with the cause when known).
3. AI visibility: mention rate, citation rate, share of voice, notable new citations.
4. What shipped last month and its measured effect.
5. What ships next month, ranked by expected impact.
6. Risks: decay, technical regressions, lost links, crawler blocks.

Numbers with date ranges and sources. No vanity metrics (total keywords, "domain authority") unless the client asks. The report passes `06-humanizer.md`; a report that says "we leveraged holistic optimisation" says nothing.

## 9. Automation

Schedule: weekly GSC pull and decay check, weekly rank and citation log, daily indexation check on money pages, CWV check after each deploy, drift compare after each deploy, monthly backlink gain and loss. Alerts on: money page returning non-200, noindex or canonical change on a money page, robots.txt change, CWV dropping below good, clicks down 20% week over week on a top-20 page, a brand mention disappearing from a tracked prompt.
