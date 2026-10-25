# Humanizer: remove AI phrases and AI garbage

This is the most important file in the skill. Every draft passes through it before a reader sees it. The job: make the text read like the one person who wrote it, without changing what it says and without adding anything that is not in the source.

## 1. Why AI text sounds like AI

A model picks the most probable next words, so by default it chooses what fits the widest audience and the most subjects. A person writes for one reader about one thing, so their choices are uneven and specific. Every tell below is one form of the default choice:

- **Staging**: signalling importance instead of adding a fact (contrasts, one-line closers, run-ups).
- **Rhythm by rule**: triads, dashes, and medium-length sentences everywhere.
- **Inflation**: ordinary facts dressed as pivotal, expert-backed, or transformative.
- **Formatting by rule**: bold and title case on every item, an emoji on every heading.
- **Leftovers**: chat wrappers and drafting notes that were never meant for the reader.
- **Wrong reader**: re-explaining what the reader already knows, so the point arrives last.

Word lists change with every model release; the structural habits above persist. Fix structure first, then words.

## 2. The one clinical exception

The 30 to 40 word extractive answer under a question heading (`04-semantic-seo.md` § 5) is written in definitive, entity-first style: is, requires, costs, takes; exact numbers; no "I think"; no fragments. It targets featured snippets and AI citations. Everything after it returns to human voice. Never mark the seam.

## 3. Hard-ban vocabulary

If a tier-1 word appears, the draft fails. Tier 2 fails when stacked or decorative. Three or more tier-3 words in one piece means the writing is sliding into mush. (Escape hatch: a banned word may stay only when it is the one exact technical term, such as "optimize" in a page-speed sentence. It never stays for style.)

**Tier 1, near-absolute tells:** delve, realm, harness, unlock, tapestry, paradigm, synergy, game-changer, game-changing, cutting-edge, revolutionize, revolutionary, future-proof, groundbreaking, trailblazing, pioneering, disruptive, supercharge, leverage (verb), holistic, transformative, reimagine, unprecedented, state-of-the-art, mission-critical, visionary, unleash, landscape (abstract), crucial, pivotal, elevate, empower, embark, navigate (abstract), testament, beacon, treasure trove, in the ever-evolving, in the fast-paced world, in today's digital age, a world where.

**Tier 2, tells when stacked:** intricate, intricacies, vibrant, seamless, seamlessly, robust (figurative), dynamic, immersive, captivate, enduring, meticulous, meticulously, commendable, unparalleled, frictionless, scalable (figurative), turnkey, plug-and-play, breakthrough, accelerate, democratize, interplay, versatile, redefine, innovative, comprehensive, ultimate, essential, powerful, effortless, streamline, foster, nuanced, multifaceted, invaluable, remarkable, notably, arguably, undoubtedly.

**Tier 3, context check:** highlight (verb), emphasize, valuable, integrated, transparent, optimize, insightful, proactive, data-driven, adaptive, intuitive, align, garner, accentuate, showcase, enhance, boast, underscore, utilize (say use), facilitate (say help), key (adjective), actually, quietly, deep dive, bolster, cultivate, encompass, ensure (when decorative).

**Bloated verb shapes:** never "serves as", "stands as", "functions as", "marks a", "represents a", "boasts a", "features a", "offers a", "refers to" to dodge is and has. Say is. Say has.

## 4. Dead openings, transitions, bait, hype

**Dead openings:** "In today's...", "In the world of...", "It's important to note", "It's worth noting", "In order to" (say to), "Let's dive in", "Let's explore", "Let's unpack", "Let's break this down", "Here's what you need to know", "Without further ado", "At the end of the day", "Moving forward", "To put this in perspective", "What makes this particularly interesting is", "In other words", "It goes without saying", "nobody is talking about", "most people don't realize", "In this article, we will", "Despite its strengths, X faces challenges", "Honestly?", "Look,", "Here's the thing", "Real talk".

**Dead transitions:** Furthermore, Additionally, Moreover, That said, That being said, With that in mind, It is also worth mentioning, On top of that, In conclusion, To sum up, Ultimately, Overall. Use a transition the logic earns ("but", "so", "because") or none.

**Engagement bait:** "Let that sink in", "Read that again", "Full stop", "This changes everything", "You're not ready for this", "Spoiler alert", "Plot twist", "Game over".

**Hype:** no 10x anything, no overnight transformation, no superpowers, no "the future of", no "the future looks bright", no "exciting times ahead".

## 5. Structural tells (act on one sighting)

**5.1 The reframe (fatal).** The single most reliable AI tell: negate one frame, assert another.
Banned in every disguise: "This isn't X. This is Y." / "Not X. Y." / "Forget X, focus on Y." / "It's not just about X, it's about Y." / "Less X, more Y." / "Not only X but also Y." / "The real issue isn't X, it's Y." / "You don't need X, you need Y." / "X is dead, Y is the future." / "Stop thinking X, start thinking Y." / "The question isn't X, the question is Y." / split across sentences ("This does not mean X. It means Y.") / clipped tail ("..., no guessing.") / sneaky versions ("While X may seem...", "At first glance...", "Most people think X...", "Sure, X works, but Y is where...", "X gets all the attention, but Y...").
Fix: delete the rejected half and state the claim. "It's not about the prompt, it's about the context." → "Context controls the output."
Headings too: "Not a tool. A system." → "The system."
Allowed contrast: correcting a specific fact, number, date, name, or scope ("The file is 12 MB, not 12 GB").

**5.2 One-line closers and dramatic fragments.** A one-sentence paragraph that restates the paragraph above; "That's the real win."; "That distinction matters."; a line after an example naming what it showed ("This shows the importance of..."); rows of fragments ("No setup. No training. No excuses."); every. single. word. with periods. Cut the closer that repeats; keep one only if it adds a fact or consequence. Merge fragment rows into a sentence with a claim.

**5.3 Sayings that sound deep.** "The real question is", "at its core", "what really matters", "fundamentally", "the heart of the matter", "X is the Y of Z", "X becomes a trap", "the language of", "the currency of", "the architecture of". Replace the saying with the specific claim.

**5.4 Arguing with no one.** "This isn't about", "I'm not saying", "To be clear", "Don't get me wrong", "Some might say... but", "A tempting approach would be", "You might think... but", "It would be easy to just". The text rejects an option nobody raised. Remove the defence; keep the claim if there is one.

**5.5 Forced triads.** Three items because three sounds complete ("innovation, inspiration, and insights"; three parallel examples; three facts then a lesson). Keep three only when the meaning has three parts; otherwise use 2, 4, or the one that matters.

**5.6 Dashes.** The final text contains no em dashes (—), en dashes (–), or spaced double hyphens used as dashes, unless the user's own writing sample uses them; then match the sample's rate. Replace with a period, comma, colon, or parentheses, or rewrite. Leave hyphens inside code, commands, paths, URLs, and compound modifiers before a noun (a high-quality report) alone.

**5.7 Stacked qualifiers.** "could potentially possibly", "it's also possible that", "might arguably", "in some cases it may". Keep a hedge only when the source supports it and the meaning needs it. Softener test: remove the "often / can / may"; if the sentence stays true, cut the softener; if it becomes false, keep it. Honest hedging ("I think", "my read is") is allowed when the next sentence shows why you would know.

**5.8 Inflated significance and -ing riders.** "stands as a testament", "a pivotal moment", "plays a key role", "marking a shift", "underscoring its importance", "reflecting broader trends", "setting the stage for", "paving the way for", "highlighting", "showcasing", "fostering", "ensuring", "symbolizing". Keep the fact, cut the rider. Stock "Challenges and future outlook" sections and send-off paragraphs ("The future looks bright") are cut; end on the last concrete fact.

**5.9 Sales language and borrowed authority.** "rich" (figurative), "profound", "nestled", "in the heart of", "renowned", "diverse array", "breathtaking", "must-visit", "stunning", "world-class", "best-in-class", "industry-leading", "trusted by thousands" (unless the number is real and stated). "Experts argue", "studies show", "industry reports", "observers have cited", "featured in [list of outlets]" without the named source and what it said. Name the source or cut the claim.

**5.10 Vague connection.** "associated with", "linked to", "tied to", "in connection with". Name the relationship the source gives (founded, owns, causes, requires). If the source does not say, keep the vagueness rather than inventing a role.

**5.11 Analogy control.** Default: none. An analogy stays only if the subject is technical, the analogy clarifies, it is shorter than the literal explanation, it is exact enough not to mislead, and it sounds normal aloud. Banned setups: "Think of it as", "Imagine", "Picture", "It's like", "Works like", "The engine of", "The DNA of", "A lens for". Banned families: journey, battlefield, ecosystem, compass, iceberg, north star, flywheel, chess, sports, puzzle, signal-and-noise, Swiss army knife, secret sauce, silver bullet, low-hanging fruit. Physical verbs for abstract work (sanded down, bolted on, stitched together, baked in, distilled, surfaced, crystallized): at most one per piece.

**5.12 Formatting by rule.** Bold on words that carry no emphasis; every list item with a bold label and a colon; Title Case Headings; emojis or arrows (→) as decoration; a horizontal rule between every section; a heading repeated in its first sentence; curly quotes where the target uses straight. Sentence case, bold 1 to 2 moments per section, labels only when they carry information.

**5.13 Chatbot residue and drafting leftovers.** "I hope this helps", "Of course!", "Certainly!", "Great question", "You're absolutely right", "Would you like me to", "Let me know if", "Here is a", "as of my last update", "while specific details are limited", "based on available information", "it is believed that", "likely grew up". Also meta narration: "In this section we will", "the table below compares", "this article was generated from". Remove outright; state what the source does not show, or cut the sentence.

**5.14 Metronome rhythm.** Every sentence medium, every paragraph 3 to 4 sentences, every section ending the same way. Read three consecutive paragraphs aloud; if their shapes feel identical, break them: a short sentence, then a longer one that carries a full thought across two clauses, then a fragment if the voice allows it.

**5.15 Elegant variation and rule of synonyms.** Never swap "Sarah" for "the seasoned operator" or "the payroll tool" for "the solution" to avoid repeating a name. Reuse the name. This is also an entity signal (`04-semantic-seo.md` § 6).

**5.16 Wrong reader.** In a reply, a reviewer comment, or a page for returning users, lead with the decision or the answer and keep only the reasoning that would change whether the reader agrees. Do not rebuild background the reader already has.

## 6. What human writing does instead

- Starts with the useful answer. No warm-up lap.
- Paragraphs of 1 to 2 sentences by default, 3 at most.
- Varied rhythm on purpose. Fragments allowed. Sentences may start with And, But, So.
- Contractions: don't, can't, it's, you're.
- "I" and "you". Active voice. One specific reader.
- A number, name, date, source, or example within two sentences of every strong claim. "The company faced challenges" → "The company missed payroll twice in 6 months."
- A stance when the evidence supports one. Honest uncertainty when it doesn't, with the reason.
- The one objection a smart reader would raise hardest, answered in the text instead of avoided.
- Mixed feelings, a real aside, a specific odd detail, a self-correction: these are kept, not sanded off.
- Stops when the point is made. Most pieces end two paragraphs before a model thinks they do.

## 7. What to keep (do not over-correct)

Leave a watched phrase alone inside a quotation, a title, a proper name, or a sentence that discusses the phrase. Do not force jokes, slang, or punchiness. Do not make every paragraph one sentence. Do not turn the text into a checklist of avoided mistakes. Write normally, then remove what sounds machine-made. If the user supplies a writing sample, match its sentence length, word choice, punctuation, openings, and transitions; the sample overrides the dash rule and the voice defaults.

## 8. Working modes

- **Pasted text**: return the marked tells (short list), then the final rewrite. Keep every supported claim. Add no fact, name, number, date, quote, or citation that is not in the source or from the user.
- **File mode**: rewrite prose only; keep code blocks, inline code, commands, paths, front matter, data, and link targets unchanged. Write only the final text to the file and give a 3-line summary.
- **Embedded mode** (inside another command of this skill): run silently, return only the final text, never label the modes.

## 9. Pass B: voice audit (mandatory, run silently)

1. Cut throat-clearing openers and staged run-ups.
2. Hunt reframes in every disguise; delete the rejected half. One instance fails the draft.
3. Cut one-line closers that restate; merge fragment rows.
4. Replace vague claims with a number, name, date, or example within two sentences, or soften or cut.
5. Remove inflated significance, -ing riders, sales words, borrowed authority.
6. Replace bloated verbs with is, has, does.
7. Remove every em dash and en dash (unless the sample uses them).
8. Break forced triads; vary sentence shape; kill metronome runs.
9. Run the softener test on every hedge.
10. Delete analogies that fail the five tests; swap metaphor verbs for literal ones.
11. Strip chatbot residue, meta narration, cutoff disclaimers.
12. Remove decorative bold, title case, emojis, arrows, repeated headings.
13. Reuse entity names; remove elegant variation.
14. Answer the strongest objection somewhere in the piece.
15. Cut the ending that only repeats; end on the last sentence that does work.
16. Scan against all three vocabulary tiers.
17. Confirm nothing was added and nothing supported was lost.
18. Final read: would the author publish this under their name to readers who push back?

## 10. AI garbage score (report when asked, or for audits)

Count per 1,000 words and report the worst first:

| Tell | Fail threshold |
|---|---|
| Tier-1 words | any |
| Reframes (any disguise) | any |
| Em or en dashes | any (unless sample uses them) |
| Chatbot residue, cutoff disclaimers | any |
| One-line closers that restate | more than 1 |
| Forced triads | more than 2 |
| Dead openings or transitions | more than 2 |
| Tier-2 words | more than 3 |
| Tier-3 words | more than 5 |
| Unsupported strong claims (no specific within 2 sentences) | more than 2 |
| Paragraphs of 4 or more sentences | more than 10% of paragraphs |

Pass means every row is under threshold. Report "AI garbage score: pass" or list the failing rows with the first example of each.
