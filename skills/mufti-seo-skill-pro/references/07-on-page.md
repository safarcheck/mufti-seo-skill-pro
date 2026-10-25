# On-page: titles, meta, headings, URLs, links, answer blocks, images, landing pages

Everything on the page that search engines, answer engines, and readers see first. Evidence standard: fetch the live page and report what is there before proposing changes.

## 1. Title tags

- One per page, 50 to 60 characters (under about 580 px), primary entity first, the specific promise second, brand last if room: "Payroll software for Indian SMEs: 12-minute setup | Acme".
- Matches the SERP's intent and page type (a guide title for a guide query, a product title for a product query).
- Unique across the site. Duplicate titles are a cannibalisation signal.
- No clickbait the page does not deliver; CTR gains vanish when pogo-sticking rises.
- Deliver 5 options per page with the reasoning for each (intent match, entity, promise, length).

## 2. Meta descriptions

- 140 to 155 characters. The outcome for the reader, one proof, one reason to click now. Written in human voice (`06-humanizer.md`), no "Discover", "Unlock", "Explore".
- Google rewrites about 60% of descriptions; write the one it would want to keep: it contains the words the query uses and the answer the searcher wants.
- Unique per page. Deliver 5 options.

## 3. Headings

See `04-semantic-seo.md` § 4. Checklist: one H1 that matches the title's entity; H2s as attributes or questions; question H2s each carry a 30 to 40 word extractive answer; no skipped levels; sentence case; no decorative headings; each heading survives the deletion test.

## 4. URL structure

- Lowercase, hyphens, no stop words unless needed for meaning, no dates unless the content is dated, no parameters on indexable pages.
- Entity first: `/payroll-software/india/`, not `/blog/2024/05/post-123/`.
- Stable. Changing a URL costs equity; when unavoidable, 301 and update internal links the same day.
- Folder structure mirrors the topical map: hub at `/topic/`, spokes at `/topic/spoke/`.

## 5. Internal links

See `04-semantic-seo.md` § 7. Per page, deliver: links in (count, anchors), links out (count, anchors), missing hub or spoke links, generic anchors to replace, orphan status. Money pages receive contextual links from every relevant informational page.

## 6. Answer blocks (quotable answers)

Build the page so an engine can lift a complete answer from one passage:

- Extractive answer under each question heading (30 to 40 words, definitive).
- Definitions as "X is a Y that Z" in the first sentence of the relevant section.
- Steps as a numbered list with one action per item.
- Comparisons as a table with the attributes in the header row.
- Numbers with units and dates ("₹21,000 per month, as of March 2026").
- FAQ section at the end for questions that did not earn an H2, each answered in 2 to 3 sentences, marked up with FAQPage schema only when the answers are visible on the page.

## 7. Images

- Descriptive file names (`payroll-dashboard-overdue-clients.webp`), alt text that states what is shown and why it matters to the section, under 125 characters, no keyword stuffing.
- Modern formats (WebP or AVIF), width and height attributes (prevents CLS), lazy loading below the fold, never on the LCP image.
- One image per 300 to 500 words where it adds information: annotated screenshot, comparison table rendered as an image only if a real table is also present, diagrams for 3 or more decision points.
- OG image per key page (1200 × 630), with the page's promise in large text.

## 8. On-page audit output (`onpage` command)

Per URL:

```
URL:
Title:             current | issue | 5 options
Meta:              current | issue | 5 options
H1:                current | issue
Headings:          hierarchy issues | drift | missing answer blocks
URL:               issue
Internal links:    in / out / missing / generic anchors
Answer blocks:     present / missing per question heading
Images:            missing alt / oversized / wrong format / CLS risk
Schema:            present types / errors / recommended (see 08 § 5)
Fix first:         one item, with the expected effect
```

## 9. SEO landing page structure (`landing` command)

A landing page ranks when it is the page type the SERP wants and converts when it answers the buyer's next question in order. Default order:

1. **Hero**: H1 with the entity and the outcome; one sentence of proof; primary CTA that says what happens next. The product or result visible without scrolling.
2. **The problem in the buyer's words** (2 to 3 sentences, from the brief's reader).
3. **How it works** in 3 to 5 steps with real screenshots or numbers.
4. **Proof**: named customers, specific results, reviews with sources, certifications.
5. **Comparison or "who it's for / not for"** (investigative intent).
6. **Pricing or the next step** with the second CTA.
7. **FAQ** answering the PAA questions for the keyword, each 2 to 3 sentences.
8. **Schema**: Organization or LocalBusiness, Product or Service with offers, FAQPage, BreadcrumbList.

Rules: one keyword cluster per landing page; copy follows `05-content-writing.md` § 6; every claim has proof next to it; mobile hero fits one screen; forms ask for the minimum; the page passes both edit passes. Use the 10 landing page prompts in `13-prompts.md` § 1 to run each step.
