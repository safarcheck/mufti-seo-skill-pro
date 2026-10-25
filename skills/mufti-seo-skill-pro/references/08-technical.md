# Technical SEO

If a page cannot be crawled, rendered, and indexed, nothing else in this skill matters. Audit from observed evidence: fetch the page, read robots.txt and sitemaps, run the tools in `14-integrations.md`, and report what you saw. Severity: critical (blocks indexing or loses revenue now), high (costs rankings), medium (costs efficiency), low (hygiene).

## 1. Crawlability

- `robots.txt`: no accidental `Disallow: /`; CSS, JS, and images allowed; sitemap declared. AI crawler rules: see `09-aeo-geo-llm.md` § 4.
- Crawl budget on large sites: faceted URLs, parameters, session IDs, calendar pages, and internal search results blocked or canonicalised; no infinite spaces.
- Redirects: no chains longer than 1 hop, no loops, 301 for permanent, no 302 for moved pages, no soft 404s (200 status on empty pages).
- Status codes on every linked URL: 200 for live pages, 404 or 410 for removed, 301 for moved. Internal links never point at redirects or errors.
- Click depth: every important page within 3 clicks of the homepage; orphans (pages with no internal links) listed and linked or removed.

## 2. Indexability

- `noindex` only where intended (thank-you pages, filters, staging). Check meta robots and `X-Robots-Tag` headers.
- Canonicals: self-referencing on indexable pages; cross-domain or parameter canonicals correct; no canonical to a noindexed or redirected URL; no conflicting signals (canonical says A, sitemap says B, hreflang says C).
- Duplicate content: http vs https, www vs non-www, trailing slash, uppercase, print versions, UTM pages. One version resolves; the rest redirect.
- Pagination: `rel=next/prev` is ignored by Google; use self-canonical paginated pages, link them, and keep the first page as the hub.
- Index coverage: compare sitemap URLs to GSC's indexed count; investigate "Crawled, currently not indexed" (quality or thinness) and "Discovered, not indexed" (crawl budget or internal links).

## 3. Rendering (SSR vs CSR)

- Primary content, links, and metadata must exist in the initial HTML or be rendered server-side. Client-side rendered content is indexed late, partially, or not at all, and most AI crawlers do not execute JavaScript.
- Test: fetch the raw HTML without JavaScript and confirm the H1, body copy, internal links, canonical, and schema are present. Then compare with the rendered DOM.
- Fixes by stack: SSR or SSG for Next.js, Nuxt, SvelteKit; prerendering for SPAs; hydration must not replace server content with different content.
- Lazy-loaded content that requires scroll or click (tabs, accordions, infinite scroll) needs a crawlable fallback.

## 4. Core Web Vitals

Use field data first (CrUX via PageSpeed Insights or GSC) and lab data for diagnosis. Targets at the 75th percentile:

| Metric | Good | Common causes when poor |
|---|---|---|
| LCP (Largest Contentful Paint) | ≤ 2.5 s | Unoptimised hero image, render-blocking CSS or JS, slow server (TTFB > 800 ms), client-side rendering, no preload on the LCP image |
| INP (Interaction to Next Paint) | ≤ 200 ms | Long JavaScript tasks, heavy third-party scripts, hydration on interaction, layout thrash |
| CLS (Cumulative Layout Shift) | ≤ 0.1 | Images without width and height, late-loading fonts, injected banners and ads, dynamic content above the fold |

Fix order: TTFB and server caching; LCP image (correct format, size, `fetchpriority="high"`, no lazy-load); remove or defer third-party scripts; reserve space for everything that loads late; font-display swap with size-adjust.

## 5. Structured data (schema)

- Format: JSON-LD in the `<head>` or body, one graph per page with `@id` references between nodes (Organization ↔ WebSite ↔ WebPage ↔ Article ↔ Person).
- Types by page: Organization (sitewide, with `sameAs` to real profiles), WebSite with SearchAction when site search exists, BreadcrumbList, Article or BlogPosting (author as Person with credentials, datePublished, dateModified), Product with Offer and AggregateRating (only from real reviews), FAQPage (only for visible Q&A), HowTo (only for real step content), LocalBusiness (with NAP, hours, geo), Service, VideoObject, Event.
- Rules: markup describes only what is visible on the page; no fake ratings; no FAQ markup on pages without FAQs; every required property present; validate with the Rich Results Test or Schema.org validator and report errors and warnings separately.
- Entity consistency: the same name, URL, logo, address, and `sameAs` on every page; this feeds the knowledge panel and AI engines' entity understanding (`09-aeo-geo-llm.md` § 5).
- Deliverable: the JSON-LD block, ready to paste, plus the validation result.

## 6. XML sitemaps

- Only indexable 200 URLs with self-canonicals; no noindex, redirected, or 404 URLs; `lastmod` real (changes when content changes), not the generation time.
- Under 50,000 URLs and 50 MB per file; a sitemap index for larger sites; separate sitemaps per type (pages, posts, products, images, video, news) help diagnosis.
- Declared in robots.txt and submitted in GSC and Bing Webmaster Tools. Report: URLs in sitemap vs indexed vs excluded, with reasons.

## 7. Mobile and accessibility

- Responsive layout, no horizontal scroll at 375 px, tap targets 44 px or more, readable font size (16 px body), no intrusive interstitials.
- Accessibility affects rankings indirectly and AI agents directly: semantic HTML (nav, main, article, headings in order), labelled forms, alt text, focus states, keyboard navigation, sufficient contrast. The accessibility tree is what agent browsers read (`09-aeo-geo-llm.md` § 7).

## 8. Security and hygiene

- HTTPS everywhere, HSTS, no mixed content, valid certificate, http → https 301.
- Security headers present (Content-Security-Policy, X-Content-Type-Options, Referrer-Policy); they do not rank pages but their absence flags a site to reviewers and some crawlers.
- No hacked content, spam injections, or cloaking; check GSC Security Issues.

## 9. International (hreflang)

- `hreflang` on every language or region variant, reciprocal (every page lists all variants including itself), with `x-default`; language codes ISO 639-1, region codes ISO 3166-1 alpha-2; no hreflang to redirected or noindexed URLs.
- One URL per language and region (subfolder preferred: `/en-in/`, `/hi-in/`); no automatic IP redirects that block crawlers.
- Translate the semantic term set, do not transliterate the English keywords; intent differs by market.

## 10. Technical audit output (`technical` command)

```
Crawlability:   findings with severity, URL examples, fix
Indexability:   coverage numbers, canonical conflicts, duplicates, fix
Rendering:      raw HTML vs rendered diff, fix by stack
CWV:            LCP / INP / CLS field values, top 3 causes, fix order
Schema:         types present, errors, recommended graph
Sitemaps:       in / indexed / excluded with reasons
Mobile & a11y:  failures with examples
Security:       failures
Hreflang:       errors (or n/a)
Fix first:      the one critical item and what it costs per week if skipped
```
