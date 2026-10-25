# Brand Brief

The one document every department reads. Build it once, update it when the business changes, never ask the user to repeat it.

## 1. Where it lives

Look for an existing brief before asking anything, in this order: `BRAND-BRIEF.md`, `brand-dna.md`, `PRODUCT.md`, `DESIGN.md`, `README.md` of the site repo, the homepage and About page of the live site. If `research-brand` from gtm-engineer-skills is installed, its Brand DNA output is a valid brief; read it and fill only the SEO fields below.

Save the result as `BRAND-BRIEF.md` in the project root (or where the user asks). Date it.

## 2. Intake (ask only what you cannot find)

Ask at most 6 questions, in one message, and only the ones the sources did not answer:

1. What do you sell, to whom, and what happens after they buy or sign up? (one sentence each)
2. Who are the 3 competitors a buyer compares you against?
3. Which pages make money today, and which traffic do you already get? (GSC export or top 10 queries if available)
4. What must never appear in copy? (claims, words, competitor names, pricing, regulated statements)
5. What real proof exists? Numbers, customers, case studies, certifications, years in business, team credentials.
6. Markets and languages: countries, cities, languages, currencies.

If the user answers with "just do it", proceed with what the live site shows and mark every unknown as `[UNKNOWN]` in the brief. Never fill an unknown with a plausible guess.

## 3. Template

```markdown
# Brand Brief: {Company}
Updated: {YYYY-MM-DD}

## Business
- What we sell:
- Who buys it (one specific person, their job, their trigger):
- Business model (SaaS, ecommerce, local service, publisher, agency, marketplace):
- Price range and buying cycle:
- Markets, languages, currencies:

## Positioning
- The one sentence a buyer should repeat about us:
- Category we want to own (the entity Google and AI engines should attach us to):
- 3 competitors and the honest difference against each:
- Claims we can prove (with the proof):
- Claims we must never make:

## Proof and EEAT
- Named authors and their credentials:
- Real numbers we can publish (customers, revenue range, years, volume):
- Case studies, reviews, certifications, awards (with links):
- First-hand experience we can show (screenshots, tests, data we own):

## Voice
- 3 adjectives for the voice, with an example sentence for each:
- Words we use / words we avoid:
- Reading level and formality:
- A 150-word sample of writing the founder likes (paste it):

## Site
- CMS and framework, rendering (SSR, SSG, CSR):
- Money pages (URL + what it converts to):
- Current top queries and pages (from GSC, with dates):
- Known technical constraints:

## Search goals
- Primary entity and macro topic:
- Top 5 commercial keywords:
- Top 5 questions buyers ask AI engines about this category:
- Success metric for the next 90 days (one number):
```

## 4. How departments use it

- Research reads Business, Positioning, Search goals.
- Content and On-page read Voice, Proof, Claims we must never make.
- Technical reads Site.
- Authority reads Proof (what is worth linking to) and Competitors.
- Measurement reads Money pages and the 90-day metric.

A department that needs a field the brief lacks asks for that field, adds it to the brief, and continues. The brief grows; the user never repeats themselves.
