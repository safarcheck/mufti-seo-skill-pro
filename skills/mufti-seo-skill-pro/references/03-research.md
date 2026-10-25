# Research

Keyword discovery, intent, SERP gaps, the prompts people type into AI engines, and the semantic term set a page must cover. Everything here feeds the topical map (`04-semantic-seo.md`).

## 1. Seeds

Start from the Brand Brief: primary entity, 5 commercial keywords, 5 buyer questions. Add seeds from the live site (navigation labels, product names, H1s), from GSC (queries at position 4 to 20), and from the 3 competitors' top pages.

## 2. Expansion

Expand each seed through, in order of trust:

1. Live SERP: People Also Ask, related searches, autocomplete, "Things to know", AI Overview follow-ups.
2. Competitor pages: their H2s and H3s are their keyword map.
3. Community language: Reddit, Quora, forums, support tickets, sales call notes. The words buyers use before they learn the industry term.
4. Tool data when available: DataForSEO, Ahrefs, Semrush, GSC (see `14-integrations.md`). Volumes are estimates; say so.

Record every keyword with: seed, keyword, intent, modifier type, estimated volume (or "unknown"), difficulty (or "unknown"), target cluster, source.

## 3. Intent, from the SERP not from the words

Classify by what Google already ranks for the query, because that is what it believes the intent is:

| Intent | SERP shows | Page type to build |
|---|---|---|
| Informational | Guides, definitions, PAA, videos | Guide or explainer with extractive answers |
| Investigative | Comparisons, "best", reviews, listicles | Comparison, "X vs Y", alternatives, buyer guide |
| Transactional | Product pages, pricing, local pack, ads | Product, service, pricing, location page |
| Navigational | One brand dominates | Do not target unless it is your brand |

If the SERP is mixed, note the split (for example "60% guides, 40% product pages") and pick the majority page type or split the keyword across two nodes. A well-written page that is the wrong type does not rank; see SXO in `09-aeo-geo-llm.md` § 6.

## 4. Long-tail keywords

Long-tail is where new and mid-authority sites win first. Build them from modifiers:

- Question: how, what, why, when, can, does, is, should
- Qualifier: best, cheap, free, fast, small business, for beginners, enterprise
- Comparison: vs, alternative, like, compared to, or
- Location: city, region, "near me", country
- Format: template, checklist, example, calculator, tool
- Time: 2026, this year, latest, updated
- Problem: not working, error, fix, slow, failed

Rule: one long-tail cluster per page section (H2), not one page per long-tail keyword, unless the SERP shows a dedicated page type for it.

## 5. AI prompts people actually type

AI engines are a second search surface. Collect the prompts a buyer would type into ChatGPT, Perplexity, Gemini, Claude, or Copilot about the category:

- "What is the best {category} for {situation}?"
- "Compare {brand} and {competitor} for {use case}"
- "Is {brand} worth it?" / "{brand} pricing" / "{brand} alternatives"
- "How do I {job the product does} without {pain}?"
- "Which {category} tools do {role}s use?"

Test 10 to 50 of them in at least 2 engines. Log: prompt, engine, date, whether the brand is mentioned, who is cited, which URLs are cited. This log is the baseline for `12-measurement.md` § 5. If `geo-content-research` from gtm-engineer-skills is installed, use it to produce `prompts.csv`.

## 6. The semantic term set (what people call LSI, NLP terms, entities)

"LSI keywords" is a marketing name; Google does not use latent semantic indexing. What works, and what this section produces, is the set of terms a complete page on this topic naturally contains. Build it in four layers for every target page:

1. **Entities**: the named things (products, people, organisations, places, standards, laws, technologies) a knowledgeable page must mention. Each entity carries its attributes (size, cost, date, version, classification). Source: SERP top 10, Wikipedia and Wikidata for the topic, Google's Knowledge Graph when visible.
2. **Attributes and values**: the measurable properties readers ask about (price, time, dimensions, limits, compatibility). A page that states values outranks a page that states adjectives.
3. **Co-occurring terms**: words and phrases that appear across most top-ranking pages but not in yours. Collect by reading the top 10, not from a tool's "LSI" list. Keep only terms that make the page more complete; drop any you would have to force in.
4. **Question terms**: the PAA and forum questions, phrased as they are asked, to become H2s and H3s.

Deliver as a table: term, layer, where it goes (H2 name, answer block, body, FAQ, schema), already present (yes or no). Coverage target: every entity and attribute the top 3 pages share, plus at least 2 the top 10 miss (information gain, `05-content-writing.md` § 4).

Relevancy is coverage of this set with correct relationships (X causes Y, X requires Y, X costs Y), not repetition of the head term. Keyword density is not a target.

## 7. Clustering and mapping

Cluster by SERP overlap: two keywords belong on one page when 3 or more of their top-10 URLs match. One cluster, one URL. Record the cluster's primary keyword, its secondary keywords, its intent, its page type, and the URL (existing or planned). Flag cannibalisation when two existing URLs share a cluster; send to `05-content-writing.md` § 7 for consolidation.

If claude-seo is installed, `/seo cluster <seed>` does the overlap math; use it and then apply the rules above to its output.

## 8. Deliverable

`keywords.csv` (or markdown table) with the fields in § 2 and § 7, plus:

- Top 10 opportunities by score (impact × confidence ÷ effort)
- Semantic term set per planned page (§ 6)
- AI prompt log (§ 5)
- Gaps: questions nobody on page 1 answers, page types the SERP wants that nobody built well
