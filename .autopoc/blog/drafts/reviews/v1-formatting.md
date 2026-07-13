# Formatting Review -- v1

**Reviewer:** Formatting (Editorial Compliance)
**Draft:** v1.md
**Date:** 2026-07-13

---

## Scores

| Dimension | Weight | Score | Weighted | Notes |
|---|---|---|---|---|
| Heading hierarchy | 1x | 9 | 9 | All sentence case, all H2, clean cascade, no H1 in body. Minor: no H3 subheadings used at all, but nothing is skipped. |
| Code formatting | 1x | 5 | 5 | Code blocks are real, runnable, and properly fenced. However, **inline backticks are used extensively** (lines 14, 28, 46, 48, 103, 112, 114, 122). Rubric says "no backticks." |
| CTA placement | 2x | 5 | 10 | CTA at closing only (line 133, linked to redhat.com). No CTA near the top or mid-article. The abstract specifies a CTA but the draft only places it at the end. |
| SEO readiness | 1x | 8 | 8 | Title is 59 characters (within 50-60 target). Keywords "AI agent trace" and "Red Hat OpenShift AI" appear in both title and first paragraph. Minor gap: subtitle (line 3) uses italics rather than a meta description field. |
| Link strategy | 1x | 6 | 6 | One internal link to redhat.com (line 133). Two external GitHub links (lines 7, 122). No competitor links. However, only 1 internal link is thin for a Red Hat developer blog. Could link to OpenShift docs, UBI docs, or related blog posts. |
| Editorial compliance | 2x | 6 | 12 | See detailed checklist below. Oxford commas are consistently used. Contractions are used well. However: UBI never expanded on first use, "four" and "three" spelled out instead of numerals, and "CLI" / "JSONL" / "UID" never expanded. |
| Brand standards | 1x | 7 | 7 | Mermaid diagram uses Red Hat brand colors (#EE0000, #A30000). "Red Hat OpenShift AI" used correctly on first mention (line 1) and later shortened to "OpenShift" appropriately. No font references, but this is markdown so not directly applicable. Minor: "UBI" used without "Red Hat Universal Base Image" on first mention. |
| Word count | 1x | 8 | 8 | ~1,125 words total including code blocks. Prose-only estimate is ~850-900 words. Within the 800-1300 target for tutorials. Slightly front-loaded with explanation; code sections are appropriately sized. |

---

**Weighted total:** 65 / 100

**Normalized score:** 6.5 / 10

---

## Line-level feedback

| Line | Issue | Severity | Recommendation |
|---|---|---|---|
| 14 | Inline backticks: `` `npx forsy-trace-skill init` `` | Must fix | Remove backticks. Use monospace formatting or describe the command in prose. |
| 26 | "Containerizing with UBI" -- UBI not expanded | Must fix | Change to "Containerizing with UBI (Universal Base Image)" or expand in the first body mention. |
| 28 | Inline backticks: `` `registry.access.redhat.com/ubi9/nodejs-22` `` | Must fix | Remove backticks. Reference the image name in a code block or use monospace styling without backticks. |
| 46 | Inline backticks: `` `USER 0` `` / `` `USER 1001` `` / `` `chgrp -R 0` `` | Must fix | Remove backticks around inline code references. |
| 48 | Inline backticks: `` `quay.io/aicatalyst/forsy-trace-skill:latest` `` | Must fix | Remove backticks. |
| 54 | "We created four Jobs" | Should fix | Use numeral: "We created 4 Jobs" per Red Hat style (numerals in running text). |
| 99 | "All four Jobs" | Should fix | Use numeral: "All 4 Jobs". |
| 103 | Inline backticks in table: `` `init` ``, `` `--out` ``, `` `--force` `` | Must fix | Remove backticks. |
| 108 | "three JSONL files" and "one duplicate" | Should fix | Use numerals: "3 JSONL files", "1 duplicate". |
| 112 | Inline backticks: `` `ubi9/nodejs-22` `` | Must fix | Remove backticks. |
| 114 | Inline backticks: `` `chgrp` ``, `` `USER 0` `` | Must fix | Remove backticks. |
| 7 | No mid-article CTA | Should fix | Add a CTA after the "Why this matters" section linking to Red Hat OpenShift AI or a trial page. |
| 14 | "CLI" not expanded on first use | Should fix | Expand to "command-line interface (CLI)" on first use (line 14). |
| 15 | "JSONL" not expanded on first use | Should fix | Expand to "JSON Lines (JSONL)" on first use. |
| 46 | "UID" not expanded on first use | Should fix | Expand to "user ID (UID)". |
| 122 | Inline backticks: `` `quay.io/aicatalyst/forsy-trace-skill:latest` `` | Must fix | Remove backticks. |

---

## Editorial compliance checklist

| Rule | Status | Details |
|---|---|---|
| Sentence case headings | Pass | All 7 headings use sentence case correctly. |
| Oxford commas | Pass | Consistently used throughout (lines 5, 11, 15, 16, 52, 65, 108). |
| No backticks | **Fail** | 10+ instances of inline backticks across 8 lines. |
| Full product name on first mention | Partial | "Red Hat OpenShift AI" correct (line 1). "UBI" never expanded to "Universal Base Image." |
| Lowercase component descriptors | Pass | No issues found. |
| No H1 in body | Pass | All headings are H2. |
| Expand acronyms on first use | **Fail** | UBI, CLI, JSONL, UID, YAML, CPU all used without expansion. |
| Use contractions | Pass | Good contraction usage: "doesn't", "don't", "they're", "it's", "Here's", "you're". |
| Numerals in running text | **Fail** | "four" (lines 54, 99), "three" (line 108), "one" (line 108) should be numerals. |
| No em dashes | Pass | No em dashes found. Colons used effectively as alternatives. |

---

## Summary

The draft is structurally sound with clean heading hierarchy, consistent Oxford comma usage, good contractions, and no em dashes. The title length and keyword placement are solid for SEO.

Three areas need attention before v2:

1. **Inline backticks (must fix):** The rubric prohibits backticks in final output. There are 10+ instances across 8 lines. These need to be removed and replaced with monospace styling or rephrased into prose.

2. **CTA placement (must fix):** The only CTA is at the very end (line 133). The rubric requires CTAs near the top, mid-article, and closing. Add a linked CTA after the "Why this matters" section and consider one in the introduction.

3. **Acronym expansion (must fix):** UBI, CLI, JSONL, and UID are all used without expansion on first mention. Expand each on first use per Red Hat editorial standards.

Secondary issues: spelled-out numbers ("four", "three") should be numerals, and the link strategy could be strengthened with additional internal links to Red Hat documentation pages (UBI docs, OpenShift Jobs documentation, OpenShift AI product page).
