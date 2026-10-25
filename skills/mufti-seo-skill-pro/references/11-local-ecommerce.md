# Local and ecommerce SEO

## 1. Local SEO audit (`local` command)

- **Google Business Profile**: correct primary category (the one competitors in the map pack use) and secondary categories; services and products listed with descriptions; hours including holidays; photos (exterior, interior, team, work) updated monthly; posts weekly; Q&A seeded with the real top 5 questions; every review answered within 48 hours, specifically, without templates.
- **NAP consistency**: name, address, phone identical (format included) on the site, GBP, Apple Maps, Bing Places, Facebook, and the top directories for the industry and country. List every mismatch with the URL.
- **Reviews**: count, rating, velocity (new reviews per month), response rate, keywords inside reviews. Ask every satisfied customer at the moment of satisfaction, with a direct link; never incentivise; never gate.
- **Local schema**: LocalBusiness (or the specific subtype) with NAP, geo, openingHours, priceRange, `sameAs` to GBP and profiles; on the location page, not only the homepage.
- **Local content signals**: city and neighbourhood names in natural places (service areas, case studies, directions, local events), embedded map, local proof (photos of real jobs, local customers).
- **Citations**: the industry directories that matter, complete and consistent. Quantity beyond the top 20 to 30 adds little.

Deliver: a findings table (item, observed, issue, fix, priority), the NAP mismatch list, the review request process, and the LocalBusiness JSON-LD.

## 2. Location pages

One page per real location or service area, each with content that could not be on another location's page: the local team, local photos, local reviews, local pricing or availability, directions and parking, nearby landmarks, the services offered at that location specifically. Template pages with only the city name swapped are thin content; Google will index one and ignore the rest. Service-area businesses: one page per primary area with real local proof, not one per town in the region.

Structure: H1 "{Service} in {City}", answer block for "how much does {service} cost in {city}" or the local PAA, proof, map, FAQ, LocalBusiness schema, breadcrumb back to the locations hub.

## 3. Multi-location

Locations hub page linking to every location; each location linking up; consistent schema; a store locator that renders without JavaScript; a GBP per location with the same NAP as its page.

## 4. Ecommerce category pages

- Category pages are the money pages for most stores; they rank for the head and investigative keywords. Give each one: an H1 with the category entity, 150 to 400 words of real guidance above or below the grid (how to choose, what the differences are, who each sub-category is for), the top sub-categories linked in text, FAQ, and BreadcrumbList schema.
- Facets and filters: index the few combinations with real search demand (colour, size, brand when searched); noindex or canonicalise the rest; never let sort orders and price ranges create indexable URLs.
- Pagination: self-canonical paginated pages linked in sequence; the category root stays the hub; "view all" only when the page stays fast.
- Internal links: category ↔ sub-category ↔ product; buying guides link to categories with entity anchors.

## 5. Product pages

- Unique titles, descriptions, and copy per product (manufacturer text is duplicated across every reseller); copy follows `05-content-writing.md` § 6 (outcome, specifics, proof).
- Product schema with name, image, description, sku, brand, offers (price, priceCurrency, availability, url), aggregateRating and review only from real reviews on the page; shippingDetails and hasMerchantReturnPolicy when known.
- Variants: one canonical product URL with variant selection, or separate URLs only when the variants have their own search demand; never both indexed with the same copy.
- Out of stock: keep the URL live with a restock date or alternatives; 404 only when the product is gone for good, then 301 to the parent category if links exist.
- Images: multiple angles, descriptive file names and alt text, WebP, width and height set.
- Reviews with Q&A on the page; they add the long-tail language buyers search.
- Marketplace presence (Google Shopping via Merchant Center, Amazon where relevant) with the same prices and titles; price and availability mismatches get listings suppressed.

## 6. Deliverable

Local: § 1 table plus JSON-LD. Ecommerce: category and product audits with per-URL findings, the facet indexation rules, and the Product JSON-LD template filled for one real product. If claude-seo is installed, `/seo local <url>`, `/seo maps`, and `/seo ecommerce <url>` collect the evidence; apply these rules to their output.
