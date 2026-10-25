# Semantic SEO: topical maps, topical authority, entities, internal links

These rules govern the document: what a page covers, how it is ordered, where answers live, how pages connect. They follow the algorithmic authorship approach popularised by Koray Tuğberk Gübür, reduced to what a writer can actually check. Sentence style is in `06-humanizer.md`.

## 1. Topical map

Never write a page before the map exists. A map is the plan to cover a topic completely enough that Google treats the site as an authority on it (topical authority), and AI engines treat it as a source worth citing.

```
                 [ Core topic (the entity you want to own) ]
                                  │
            ┌─────────────────────┼─────────────────────┐
            ▼                     ▼                     ▼
   [ Mid-tier concept A ] [ Mid-tier concept B ] [ Mid-tier concept C ]
      │        │              │        │              │        │
      ▼        ▼              ▼        ▼              ▼        ▼
  [Spoke]  [Spoke]        [Spoke]  [Spoke]        [Spoke]  [Spoke]
```

Build it:

1. **Core topic**: the entity from the Brand Brief. "Payroll software for Indian SMEs", not "software".
2. **Niche breakdown**: split into the sub-domains a complete authority covers. "Payroll" is compliance, salary structure, tax deductions, leave and attendance, payslips, integrations, pricing, migration.
3. **Spokes**: the specific questions and jobs under each mid-tier node, taken from `03-research.md` (PAA, long-tail, AI prompts, community questions).
4. **Intent label per node**: informational, investigative, or transactional. This decides page type, depth, and where the CTA goes.
5. **One node, one page.** If a draft covers two nodes, split it. If two pages cover one node, merge them.
6. **Build order**: core and money pages first, then the spokes that support them, then breadth. Mark each node planned, drafted, published, or refreshed.

Deliver the map as a table (node, parent, intent, page type, URL, status, links up, links down, links lateral) plus the diagram.

## 2. Topical authority

Authority is earned by coverage, consistency, and connection:

- **Coverage**: every mid-tier node has its spokes published, including the unglamorous ones (edge cases, errors, limits, pricing, comparisons).
- **Consistency**: the same entity names, the same facts, the same attributes across every page and in schema. Contradictions between pages cost trust with both Google and AI engines.
- **Connection**: every page links up to its hub, hubs link down to every spoke, and overlapping spokes link laterally. No orphan pages, no dead ends.
- **Depth over breadth early**: 15 excellent pages on one mid-tier node beat 60 thin pages across five. Finish a node before opening the next.

## 3. Macro and micro context

- One **macro context** per page: its single purpose in one sentence. "How to clean a mechanical keyboard" never drifts into "the history of mechanical switches".
- **Micro contexts** are the H2s and H3s. Test for each: "If I delete this heading, does the answer to the page's core question get weaker?" If no, cut it or move it to its own node.

```
WRONG (diluted)                           RIGHT (unified)
H1: How to clean a mechanical keyboard    H1: How to clean a mechanical keyboard
  H2: Tools needed                          H2: Tools needed for keyboard cleaning
  H2: Step-by-step cleaning                 H2: Step-by-step deep clean
  H2: The invention of keyboards  ← drift   H2: Reassembly and testing after cleaning
```

## 4. Heading hierarchy

- One H1 stating the primary entity and the macro context.
- H2s are the attributes of the entity or the questions users ask, in logical or chronological order (prerequisites before steps, basics before advanced, problem before fix).
- H3 and H4 break an H2 into specifics. Never skip a level.
- Question phrasing for any H2 that maps to a real query ("How long does a payroll run take?").
- Sentence case. No decorative headings ("The moment everything changed"); a heading names what the section holds.

## 5. Extractive answers (the AEO block)

Directly under every question-style H2 or H3, before anything else, place a 30 to 40 word definitive answer:

- Format: [Entity] + [definitive verb] + [attribute or value] + [condition if needed].
- Clinical style is correct here and only here: is, causes, requires, takes; exact numbers; no first person; no hedging; no contractions needed.
- Bold the key value, not the keyword.

Example under "How long should espresso extraction take?": "Espresso extraction takes **25 to 30 seconds** for an 18 gram double shot yielding 36 grams. Under 20 seconds tastes sour and under-extracted; over 35 seconds turns bitter."

Everything after the block returns to human voice.

## 6. Entity discipline

- Every entity gets its attributes and values at first mention: exact size, cost, date, version, material, classification. "The dual-boiler machine holds brew water at 93°C and steam at 125°C", not "this machine makes great coffee fast".
- Connect entities with explicit relationships: X causes Y, X requires Y, X replaces Y, X costs Y. Co-mention is not a relationship.
- State a count, then list the counted items immediately. "3 methods" is followed by the 3 methods.
- Repeat the entity's name. Do not rotate synonyms to sound varied; consistent naming is a ranking signal and a human-writing signal at the same time. Use this alignment.
- Keep facts identical across pages and schema (name, address, price, version, date). Fix the source of truth when they differ.

## 7. Internal linking

```
          [ Hub / pillar ]
            ▲           ▲
   in-text  │           │  in-text
            ▼           ▼
       [ Spoke 1 ] ◄──► [ Spoke 2 ]
              lateral (same silo)
```

- Spokes link up to their hub; the hub links down to every spoke; spokes in one silo link laterally where content overlaps.
- Anchor text states the destination's entity or macro context ("payroll tax deduction rules in India"). Never "click here", "read more", "this post".
- Links sit inside relevant paragraphs, not in a dump at the end. One link per destination per page.
- Money pages receive links from every relevant informational page with a reason ("the calculator on the pricing page shows the exact deduction").
- Deliver link changes as a matrix: from URL, to URL, anchor text, paragraph where it goes.

## 8. Pass A: structure audit (mandatory before delivery)

1. One macro context; every H2 passes the deletion test.
2. One H1; H2s in logical order; no skipped levels; sentence case.
3. Every question H2 or H3 has a 30 to 40 word extractive answer directly beneath it.
4. Every entity has attributes and values at first mention; relationships are explicit.
5. Every count is followed by the counted items.
6. Semantic term set (`03-research.md` § 6) covered; coverage gaps listed.
7. Internal links present in all three directions with entity-precise anchors; no generic anchors; no orphan.
8. Page maps to exactly one topical map node; no cannibalisation with an existing URL.
9. Facts match the Brand Brief and the site's other pages.
