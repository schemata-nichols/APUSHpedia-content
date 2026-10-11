---
unlisted: true
---

# APUSHpedia Repository Instructions

## Project

APUSHpedia is an AP United States History knowledge base written in Obsidian-compatible Markdown and published with Quartz. Its term pages should work as a connected reference work, not as isolated flashcards or a general U.S. history encyclopedia.

The immediate editorial goal is to produce accurate, consistent pages for the canonical term inventory, beginning with Priority 5 terms.

## Sources of Truth

Before editing term pages:

1. Read tools/Term Inventory.md for canonical titles, priority, and period placement.
2. Inspect the nearest completed reference pages for current style.
3. Preserve established filenames and link targets.
4. If repository files conflict with this document, report the conflict instead of silently inventing a compromise.

Do not modify the inventory, repository configuration, Quartz code, Obsidian configuration, or unrelated pages unless the user explicitly requests it.

## File Placement and Naming

- Store a period-specific term at terms/Period N/Canonical Title.md.
- Store a concept assigned to Long-term at terms/Long-term/Canonical Title.md.
- Match the canonical title in tools/Term Inventory.md exactly, including punctuation and capitalization.
- Keep one primary page per term. Use aliases instead of duplicate pages.

## Required Frontmatter

Use exactly these four fields, in this order:

```yaml
---
title: Canonical Title
aliases:
  - Useful Alternate Name
apush-priority: 5
status: stub
---
```

Rules:

- Do not add period, type, category, tags, author, dates, or verification fields.
- Use an empty list as aliases: [] when no useful alias exists.
- Copy apush-priority from the inventory; do not estimate it independently.
- New AI-generated or substantially rewritten pages remain status: stub.
- Do not mark a page checked or verified without explicit human instruction.

## Page Goal

A term page should answer four connected questions:

1. What was it?
2. Why did it develop in this historical setting?
3. What did it change, and what limits or contradictions mattered?
4. Why is it analytically important in APUSH?

Priority 5 pages should normally take about four to five minutes to read. Aim for roughly 800–1,100 words before Sources. Prefer a shorter complete explanation over length created by repetition.

When referring to any other term that occurs in Term Inventory, use wikilinks. Versatile wikilinks usage is strongly recommended.

## Opening Summary

- Begin immediately after frontmatter with one plain Markdown blockquote.
- Do not add an Abstract heading.
- In roughly 80–130 words, identify the term, time and setting, central mechanisms or aspects, and its APUSH significance.
- Make the summary useful as a standalone review note.
- End with the central analytical distinction or question when that improves understanding.
- A plain blockquote is allowed; Obsidian or Quartz callouts such as [!note] are not.

## Body Structure

Use unnumbered H2 and H3 headings. Choose headings that fit the term instead of forcing every page into an identical outline.

Every Priority 5 page should place ## APUSH Significance immediately after the opening summary. It should explain the page's most important APUSH relationships, not provide generic test-taking advice.

Possible later sections include:

- Historical Development
- Causes
- Mechanisms
- Regional Patterns
- Political Conflict
- Social and Economic Effects
- Limits and Contradictions
- Interpretation

Use only the sections the term actually needs. Do not add a separate AP Usage, Connections, Knowledge Path, Fun Facts, or Common Misunderstandings section. Integrate useful distinctions and connections into the explanation itself.

## APUSH Focus

- Center material required to understand APUSH developments and arguments.
- Connect the term to causation, comparison, continuity and change, or contextualization where those relationships are historically meaningful.
- Explain how the term connects to major APUSH themes such as Politics and Power, Work, Exchange and Technology, American and National Identity, Migration and Settlement, Geography and the Environment, America in the World, and Social Structures.
- Show why evidence matters. Avoid empty statements such as “this may appear on the exam” or “this can be used in a DBQ.”
- Distinguish the term from commonly confused concepts inside the relevant section.
- Treat contradictions as part of the history: expansion of democracy may coexist with exclusion; reform may coexist with paternalism; economic growth may deepen slavery or inequality.
- Keep material that is merely interesting but not explanatory near the end or omit it.

## Prose and Formatting

- Write in clear academic English for a high-school APUSH reader.
- Prefer direct claims followed by explanation and concrete evidence.
- Use chronological order when development over time is central.
- Use numbered or bulleted lists only for genuinely parallel points.
- Use bold sparingly for analytical distinctions or essential terms.
- Do not number major headings.
- Do not use callouts, collapsible sections, decorative HTML, emojis, or tables unless a table materially clarifies a comparison.
- Avoid encyclopedia filler, inflated transitions, motivational language, and repeated conclusions.
- Avoid unsupported absolutes. Preserve necessary qualifications and historical disagreement.

## Links

- Use Obsidian Wikilinks for internal APUSHpedia pages: [[Canonical Title]].
- Use aliases when grammar requires them: [[Second Bank of the United States|national bank]].
- Link a heading with [[Page Title#Heading|label]] when a specific subsection is the real destination.
- Prefer canonical titles found in tools/Term Inventory.md.
- Link the first useful occurrence, not every repetition.
- Connections must help explain the current term. Do not turn the page into a directory of related topics.
- Uncreated canonical pages may remain as unresolved Wikilinks during drafting.
- Use ordinary Markdown links for external sources.

## Sources

- End every term page with ## Sources.
- Include three to six sources in a numbered list.
- Prefer, in order: the College Board Course and Exam Description; primary sources and official archives; federal museums or historic sites; university or scholarly reference works; reputable open textbooks.
- Do not cite Wikipedia as a final source.
- Verify names, dates, laws, court cases, and numerical claims against the listed sources.
- Paraphrase sources. Do not reproduce long passages.

## Editing Workflow

1. Inspect the target page, inventory entry, and nearby reference pages.
2. State which files will be changed.
3. Work in batches of no more than eight term pages.
4. Preserve unrelated user changes.
5. Validate frontmatter, headings, links, and formatting.
6. Review the diff for repetition, unsupported claims, and accidental scope expansion.
7. Report changed files, checks performed, unresolved links, and any factual uncertainty.

Useful repository checks:

- git diff --check
- rg -n "apush-relevance|^period:|^type:|^category:|^tags:" terms
- rg -n "\[![A-Za-z]" terms
- rg -n "^## [0-9]" terms

Do not commit, push, delete branches, install dependencies, or change Git configuration unless the user explicitly asks.

## Reference Standard

The initial P5 reference set is:

- Market Revolution
- Jacksonian Democracy
- Second Great Awakening
- Antebellum Reform
- Indian Removal

These pages demonstrate different content shapes. Follow their shared principles, not their exact section names.
