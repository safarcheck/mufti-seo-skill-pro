# Mufti SEO Skill Pro

A complete SEO + AI SEO department in one agent skill. Ten departments, fifty specialised jobs, one shared Brand Brief, and a strict humanizer that strips AI phrases from every draft before a reader sees it.

Works with Claude Code and any host that reads Agent Skills (Codex, Cursor, OpenCode, Gemini CLI, Copilot, Windsurf, Cline).

## What it does

| Department | Jobs |
|---|---|
| Strategy and planning | Strategy, audit planning, roadmap, opportunity scoring, competitor analysis, 6-month AI SEO plan |
| Research | Keywords, intent from the live SERP, long-tail, clustering by SERP overlap, keyword-to-page mapping, the prompts buyers type into AI engines, semantic term set (entities, attributes, co-occurring terms, question terms) |
| Semantic SEO | Topical maps, topical authority, macro and micro context, heading hierarchy, extractive answers, entity discipline, internal linking |
| Technical | Crawlability, indexability, rendering (SSR vs CSR), Core Web Vitals, schema, sitemaps, mobile, security, hreflang |
| On-page | Titles, meta, headings, URLs, internal links, answer blocks, images, SEO landing page structure |
| Content | Briefs, drafts, depth and information gain, EEAT, outcome-first copywriting, refresh and consolidation |
| AI search (AEO, GEO, AIO, SXO) | Snippet and PAA coverage, AI citations, crawler access, llms.txt, entity and brand visibility, agent readiness |
| Authority | Backlinks, link-worthy assets, unlinked mentions, listicles and review sites, digital PR, Reddit and Quora |
| Local and ecommerce | GBP, NAP, location pages, category and product pages |
| Measurement | GSC analysis, rank and citation tracking, AI-referred traffic, drift monitoring, experiments, monthly report |
| Humanizer | Hard-ban vocabulary in 3 tiers, the reframe ban, structural tells, rewrite rules, a 2-pass edit, and an AI garbage score |

## The four laws

1. Brief first. Nothing starts without a Brand Brief, so you never re-explain your business.
2. Structure obeys the algorithm. Sentences obey the human.
3. Never fabricate. No invented statistics, studies, quotes, or reviews.
4. Humanize before delivery. Zero tier-1 words, zero reframes, zero em dashes, zero chatbot residue.

## Install

Claude Code, as a plugin (two separate prompts):

```
/plugin marketplace add safarcheck/mufti-seo-skill-pro
```
```
/plugin install mufti-seo-skill-pro@mufti-seo-skill-pro
```

Any host that reads Agent Skills, with the Skills CLI:

```bash
npx skills add safarcheck/mufti-seo-skill-pro -g
```

From a clone: copy `skills/mufti-seo-skill-pro/` into your agent's skills folder (`~/.claude/skills/` for Claude Code).

## Use

```
/mufti-seo-skill-pro brief https://example.com
/mufti-seo-skill-pro map "payroll software for Indian SMEs"
/mufti-seo-skill-pro research "payroll compliance"
/mufti-seo-skill-pro audit https://example.com
/mufti-seo-skill-pro write "how to run payroll for 12 employees"
/mufti-seo-skill-pro landing "Acme payroll" + "payroll software India"
/mufti-seo-skill-pro humanize draft.md
/mufti-seo-skill-pro geo https://example.com
/mufti-seo-skill-pro plan https://example.com
```

Or describe the job in plain words; the skill triggers on SEO, AEO, GEO, topical map, topical authority, entities, LSI, NLP terms, long-tail, LLM optimization, humanize, AI slop.

Full command table: [`skills/mufti-seo-skill-pro/SKILL.md`](skills/mufti-seo-skill-pro/SKILL.md).

## Files

```
skills/mufti-seo-skill-pro/
  SKILL.md                      router, the four laws, workflow, output rules
  references/
    01-brand-brief.md           shared brief template and intake
    02-departments.md           10 departments, 50 jobs, audit scoring
    03-research.md              keywords, intent, long-tail, AI prompts, semantic term set
    04-semantic-seo.md          topical map, topical authority, entities, internal links
    05-content-writing.md       briefs, drafts, depth, EEAT, copywriting, refresh
    06-humanizer.md             AI phrase and pattern removal, 2-pass edit, AI garbage score
    07-on-page.md               titles, meta, headings, URLs, answer blocks, landing pages
    08-technical.md             crawl, index, rendering, CWV, schema, sitemaps, hreflang
    09-aeo-geo-llm.md           AEO, GEO, crawler access, llms.txt, SXO, 6-month plan
    10-authority.md             links, mentions, listicles, digital PR, community
    11-local-ecommerce.md       GBP, NAP, location, category, product pages
    12-measurement.md           GSC, tracking, AI visibility, drift, reporting
    13-prompts.md               ready prompts, including 10 for SEO landing pages
    14-integrations.md          claude-seo, gtm-engineer-skills, humanizer, Scrapling, and more
```

## Works with

The skill is the strategy and quality layer. When these are installed it uses them for data and applies its rules to their output: [claude-seo](https://github.com/AgriciDaniel/claude-seo), [gtm-engineer-skills](https://github.com/onvoyage-ai/gtm-engineer-skills), [humanizer](https://github.com/blader/humanizer), [Scrapling](https://github.com/D4Vinci/Scrapling), [python-seo-analyzer](https://github.com/sethblack/python-seo-analyzer), [hallmark](https://github.com/nutlope/hallmark). None of them is required.

## Sources and credit

Semantic structure rules follow the algorithmic authorship approach of Koray Tuğberk Gübür. AI-writing patterns draw on Wikipedia's "Signs of AI writing" (WikiProject AI Cleanup) and the MIT-licensed humanizer skill by blader. The 10 landing page prompts are adapted from Sunny Grewal's list. The 6-month plan, the SEO/AEO/GEO split, and the department structure are adapted from widely shared practitioner frameworks and rewritten for this skill.

## Licence

MIT.
