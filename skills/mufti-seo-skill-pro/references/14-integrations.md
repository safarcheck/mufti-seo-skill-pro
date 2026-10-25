# Integrations: tools and skills this skill uses when they are installed

Mufti SEO Skill Pro is the strategy and quality layer. It delegates data collection to installed tools and applies its rules to their output. Check availability before relying on one; never claim a tool ran when it did not. When nothing is installed, fetch pages directly, read the SERP, and say which data is unavailable.

## 1. claude-seo (plugin by AgriciDaniel)

Detect: skill `seo` or `claude-seo:seo` in the skill list; launcher at `"$HOME/.claude/skills/seo/scripts/claude-seo"` or the plugin root.

Use its commands for evidence, then apply this skill's rules on top:

| Need | Run |
|---|---|
| Full site crawl and scored audit | `/seo audit <url>` |
| Single page | `/seo page <url>` |
| Technical, 9 categories | `/seo technical <url>` |
| Schema detect, validate, generate | `/seo schema <url>` |
| Sitemap analysis or generation | `/seo sitemap <url>` |
| Content quality, EEAT | `/seo content <url>` |
| Competitive content brief data | `/seo content-brief <topic>` |
| AI Overviews, GEO | `/seo geo <url>` |
| Agent readiness, llms.txt, Lighthouse agentic | `/seo agentic audit <url>` |
| Keyword clustering by SERP overlap | `/seo cluster <seed>` |
| SXO page-type mismatch | `/seo sxo <url>` |
| Drift baseline and compare | `/seo drift baseline <url>`, `/seo drift compare <url>` |
| GSC, PageSpeed, CrUX, GA4 | `/seo google <command> <url>` |
| Backlinks (Moz, Bing, Common Crawl, DataForSEO) | `/seo backlinks <url>` |
| Local, maps, ecommerce, hreflang | `/seo local`, `/seo maps`, `/seo ecommerce`, `/seo hreflang` |
| Runtime check | `/seo doctor`; `/seo setup` only when the user asks |

Its reports are evidence. This skill's deliverable adds the Brand Brief context, the topical map position, the prioritisation, and the humanized write-up.

## 2. gtm-engineer-skills (onvoyage-ai)

Detect: skills `research-brand`, `research-keywords`, `geo-content-research`, `geo-content-planning`, `write-seo-geo-content`, `audit-website-aeo`, `improve-aeo-geo`, `build-backlinks`, `build-resource-pages`, `create-geo-charts`, `reddit-opportunity-research`, `audit-content`.

Pipeline mapping:

| Mufti step | gtm skill |
|---|---|
| Brand Brief | `research-brand` (Brand DNA) then fill the SEO fields in `01-brand-brief.md` |
| Research § 2 | `research-keywords` → keywords.csv |
| Research § 5 (AI prompts) | `geo-content-research` → prompts.csv |
| Topical map build order | `geo-content-planning` → plan.csv |
| Draft | `write-seo-geo-content`, then this skill's two-pass edit |
| AEO/GEO audit | `audit-website-aeo` (scored A to F), fixes via `improve-aeo-geo` |
| Charts AI engines can cite | `create-geo-charts` |
| Authority § 6 | `reddit-opportunity-research` |
| Authority § 2 to § 4 | `build-backlinks` |
| Fact check before publishing | `audit-content` |

## 3. humanizer (blader) and humanrank (Anthropic)

Detect: skill `humanizer` (project or user skills) or `anthropic-skills:humanrank`. `06-humanizer.md` already contains the merged rule set, so this skill does not need them. When they are present, run `humanizer` as a second independent pass on long drafts; two passes catch what one misses. If humanrank is present and the user asks for a full article, its workflow and this skill's `write` command agree; use either, apply this skill's Brand Brief and measurement layers.

## 4. Scrapling (MCP server `ScraplingServer`, skill `scrapling-official`)

Use for fetching pages that block simple requests, rendering JavaScript to compare raw vs rendered HTML (`08-technical.md` § 3), capturing SERPs, pulling competitor H2s at scale, and crawling a site for the audit. Tools: `make_request` for plain HTTP, `browser_fetch_once` for JavaScript pages, `browser_open` + `browser_fetch` for sessions, `browser_screenshot` for mobile checks. Respect robots.txt and rate limits; scraping is for analysis, never for republishing content.

## 5. python-seo-analyzer (`python-seo-analyzer` CLI)

`python-seo-analyzer <site> -f json --analyze-headings --analyze-extra-tags` crawls a site and reports titles, descriptions, headings, word counts, duplicates, and warnings per page. Good first pass for the on-page audit of a small or medium site. `--run-llm-analysis` needs `ANTHROPIC_API_KEY`. On this machine the executable lives in the Python user scripts folder; use the full path if it is not on PATH.

## 6. hallmark, impeccable, ui-ux-pro-max (design skills)

When a landing page needs to be built, not only written: `hallmark` builds new pages that do not look AI-generated; `impeccable` audits and polishes existing UI; `ui-ux-pro-max` supplies styles, palettes, and fonts. This skill supplies the structure (`07-on-page.md` § 9), the copy, and the schema; the design skill supplies the visual system. Run this skill's edit passes on the final copy in the built page.

## 7. Search Console, Bing, analytics

- GSC: API through claude-seo (`/seo google`), or a CSV export the user provides. Always state the date range.
- Bing Webmaster Tools: indexation and links for the Bing index that ChatGPT search and Copilot use; IndexNow for instant URL submission.
- GA4 or Matomo: organic landing page conversions; AI referrer channel group (`12-measurement.md` § 4).

## 8. Paid data (optional)

DataForSEO, Ahrefs, Semrush, SE Ranking, Profound, Firecrawl: use through their MCP servers or claude-seo extensions when the user has keys. Label every third-party metric with the source and date. Never block a deliverable on a paid tool; say what the free path gives and what the paid tool would add.

## 9. Detection snippet

Before a command runs, check once per session which of the above are present (skill list, `claude mcp list`, `which` on the CLIs) and record the result in the reply's "what I checked" block. Do not re-check on every step.
