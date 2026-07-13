# Formatting review: v2

**Reviewer**: Formatting (editorial compliance)
**Draft**: v2.md
**Date**: 2026-07-13

---

## Scores

| Dimension | Weight | Score (1-10) | Weighted |
|---|---|---|---|
| Heading hierarchy | 1x | 9 | 9 |
| Code formatting | 1x | 9 | 9 |
| CTA placement | 2x | 8 | 16 |
| SEO readiness | 1x | 7 | 7 |
| Link strategy | 1x | 8 | 8 |
| Editorial compliance | 2x | 8 | 16 |
| Brand standards | 1x | 8 | 8 |
| Word count | 1x | 6 | 6 |
| **Total** | **10** | | **79** |

**Normalized score: (79 / 100) * 10 = 7.9**

---

## Dimension-level feedback

### Heading hierarchy (9/10)

Headings are well structured. All body headings are H2, no H1 in the body. Clean cascade with no skipped levels. Sentence case is used throughout. Minor deduction:

- **Line 139**: "Validation results: 10 traces, 248 steps, zero errors" -- correctly capitalizes after colon. Good.
- No H3 headings are used at all, which is fine given the structure. The bold "labels" under "What we learned" (lines 154-160) function as pseudo-H3s using bold text, which is an acceptable pattern.
- All headings are sentence case. No title case violations found.

### Code formatting (9/10)

v2 changelog states backticks were removed from running text and this is confirmed -- no inline backticks in prose paragraphs. Code blocks use proper fenced blocks with language identifiers (dockerfile, bash, yaml, mermaid). All code appears runnable and real, not pseudocode.

- **Line 71**: "USER 0 / USER 1001" in running text -- these are used as plain text references to Dockerfile directives. Acceptable without backticks, though slightly ambiguous visually. No deduction since the rubric prohibits backticks.
- **Line 156**: "USER 0" in bold-started paragraph -- same pattern, acceptable.

### CTA placement (8/10)

Three CTA-adjacent placements identified:

1. **Line 26** (near top): Links to Red Hat OpenShift AI in the opening paragraph. Functions as context-setting link, not a strong action CTA.
2. **Line 137** (mid-article): "If you're building your own AI data-processing tools, this pattern works well on Red Hat OpenShift AI." Links to redhat.com. Good mid-article CTA.
3. **Lines 162-176** (closing): "Try it yourself" section with actionable commands and a closing CTA linking to both OpenShift AI product page and documentation.

Deduction: The top-of-article link (line 26) is informational rather than a true call-to-action. A stronger mid-funnel CTA pattern would place an explicit invitation to act near the top, not just a product link. The closing CTA is strong with both code and documentation links. The abstract's CTA mentions "AutoPoC pipeline" but the blog doesn't reference this -- minor disconnect but not a formatting issue.

### SEO readiness (7/10)

- **Title (line 22)**: "Deploying an AI agent trace toolkit on Red Hat OpenShift AI" -- 59 characters, within the 50-60 char guideline. Contains the keyword "Red Hat OpenShift AI" and the topic "AI agent trace toolkit." Good.
- **First paragraph (line 26)**: Contains "Red Hat OpenShift AI" with link, "Forsy Trace Skill," "Kubernetes Jobs," and "containerizing." Keywords are present.
- **Deductions**: The title does not contain a strong action verb or benefit signal (e.g., "How to deploy..." or "...in under 5 minutes"). The subtitle on line 24 provides this but subtitles don't carry H1 SEO weight. No meta description is provided (common omission for drafts). The keyword "OpenShift" appears 12 times, which is appropriate density for a ~1200-word post. "AI agent" appears 6 times -- good topical clustering.

### Link strategy (8/10)

- **redhat.com links**: 4 links to redhat.com/Red Hat properties (OpenShift AI product page x3, OpenShift AI docs x1). Good internal linking.
- **External links**: GitHub links to the upstream repo (line 30) and fork repo (line 164). These are appropriate attribution links.
- **No competitor links**: Confirmed. No links to AWS, Azure, GCP, or competing platforms.
- **Deduction**: The three OpenShift AI links all point to the same product page URL. Varying internal links (e.g., linking to a developer blog category page, a getting-started guide, or an OpenShift AI trial page) would strengthen the link graph. The quay.io reference on line 164 is plain text, not a link -- acceptable since it's a registry path, not a navigational link.

### Editorial compliance (8/10)

**Oxford commas**:
- Line 27: "running scientific computations, drafting legal analyses, prototyping products, and coordinating tool calls" -- Oxford comma present. Good.
- Line 34: "task context, each step the agent took, tool usage, observations, reasoning signals, retries, feedback, and final artifacts" -- Oxford comma present. Good.
- Line 39: "validation, normalization, and JSON Lines (JSONL) export" -- Oxford comma present. Good.
- Line 154: "which saved us from managing a multi-stage or multi-base build" -- two-item list, no Oxford comma needed. Correct.

**Acronym expansion**:
- Line 41: CLI expanded to "command-line interface (CLI)" on first use. The changelog confirms this.
- Line 39: JSONL expanded to "JSON Lines (JSONL)." Good.
- Line 71: UID expanded to "user ID (UID)." Good.
- Line 51: UBI expanded to "Universal Base Image (UBI)." Good.
- Line 103: MiB -- not expanded. "Mebibyte" is standard but rarely expanded in developer content. Borderline acceptable.

**Contractions**:
- Line 27: "doesn't tell you" -- good.
- Line 49: "they don't run cleanly" / "they do" -- good.
- Line 101: "Forsy Trace Skill is a CLI toolkit, not a web service" -- could use "isn't" for consistency with contraction style. Minor.
- Line 160: "couldn't pull it" -- good.
- Generally good contraction usage but a few spots could be more aggressive (line 45: "this maps to" could be "this maps to" -- actually fine, no contraction needed).

**Product names**:
- "Red Hat OpenShift AI" used in full on first mention (line 26). Subsequent mentions also use the full name (lines 45, 137, 176). Never shortened to "RHOAI." Good.
- "Universal Base Image (UBI)" -- full name on first mention (line 51), "UBI" thereafter. Correct.
- Line 56: "Red Hat Universal Base Image (UBI)" -- adds "Red Hat" prefix, even better.

**Em dashes**:
- None found in the entire draft. Good.

**Deductions**:
- **Line 13**: "Forsy Trace Skill" is not a Red Hat product, but it's used consistently as a proper noun. Fine.
- **Line 49**: "not just model serving" -- the period ending this sentence could arguably be inside the conditional construction more cleanly, but it's grammatically correct.
- **Line 99**: Heading "Deploying as Kubernetes Jobs" -- "Kubernetes Jobs" capitalizes "Jobs" as a Kubernetes resource kind. This is correct Kubernetes convention.
- **Line 101**: "CLI toolkit, not a web service, we deployed" -- this is a comma splice. Should be restructured: "Since Forsy Trace Skill is a CLI toolkit rather than a web service, we deployed it..." Actually, looking again at line 101: "Since Forsy Trace Skill is a CLI toolkit, not a web service, we deployed it as Kubernetes Jobs" -- this is correct parenthetical usage. No issue.

### Brand standards (8/10)

- Red Hat brand colors are referenced in the Mermaid diagram and image placeholder (lines 17, 91-92): #EE0000, #151515, #F0F0F0, #0066CC. These match the Red Hat brand palette.
- "Red Hat" is always two words, always capitalized. Never "Redhat" or "redhat." Good.
- "OpenShift" always capitalized correctly. Good.
- Image placeholder includes alt text (line 18) -- good accessibility practice.
- **Deduction**: No mention of Red Hat font families (Red Hat Display, Red Hat Text), though this is only relevant if the blog platform requires font specification. The Mermaid diagram theme overrides may not render in all contexts. Minor concern about whether the blog platform supports Mermaid natively.

### Word count (6/10)

Total word count: ~1,560 words (including changelog, image placeholders, and code blocks). Excluding the changelog (lines 1-11, ~55 words), image placeholder block (lines 13-20, ~75 words), and Mermaid block (lines 90-97, ~40 words), the substantive content is approximately 1,390 words. The rubric specifies 800-1,300 words for tutorials. The post is slightly over at ~1,390 substantive words, or ~1,200 if code blocks are excluded (code blocks account for roughly 190 words across the Dockerfile, bash, and YAML blocks).

This is on the edge. The content is dense and well-organized, but runs long for the tutorial blog type. The "Why structured agent traces matter for AI platforms" section (lines 44-49) could be tightened. The closing CTA section is appropriately concise.

---

## Editorial compliance checklist

| Rule | Status | Notes |
|---|---|---|
| Sentence case headings | Pass | All headings use sentence case |
| Oxford commas | Pass | Consistently applied in all lists |
| No backticks in running text | Pass | v2 removed all inline backticks |
| Full product name on first mention | Pass | "Red Hat OpenShift AI" line 26, "Universal Base Image (UBI)" line 51 |
| No H1 in body | Pass | All body headings are H2 |
| No em dashes | Pass | None found |
| Expand acronyms on first use | Pass | CLI, JSONL, UID, UBI all expanded |
| Use contractions | Pass | Consistent contraction usage throughout |
| Numerals in running text | Pass | "10 traces," "248 steps," "4 Jobs," etc. |
| Lowercase component descriptors | Pass | No capitalized component descriptors found |

---

## Line-level feedback

| Line | Issue | Severity | Suggestion |
|---|---|---|---|
| 24 | Subtitle uses italics -- confirm blog platform renders italics in subtitle position | Low | Verify with publishing template |
| 45 | "this maps to the data preparation and evaluation layers" -- slightly abstract | Low | Consider specifying which OpenShift AI features (e.g., data science pipelines) |
| 49 | Long sentence (47 words) ending the paragraph | Low | Consider splitting after "platform story." |
| 71 | "user ID (UID)" -- the acronym UID is not reused later in the post | Info | Expansion is still correct per the rules, just noting it's unnecessary |
| 101 | "not a web service" parenthetical -- correct but dense | Info | No change needed |
| 137 | Mid-article CTA could be stronger | Medium | Consider: "Try this pattern on Red Hat OpenShift AI to deploy your own batch workloads." |
| 164 | "quay.io/aicatalyst/forsy-trace-skill:latest" in running text without formatting | Low | Acceptable per no-backticks rule; reads fine in context |

---

## Summary

v2 is editorially clean. The major v1 formatting issues (inline backticks, unexpanded acronyms, missing CTAs) have all been addressed. The post follows Red Hat editorial conventions consistently: sentence case headings, Oxford commas, proper product names, contraction usage, and numeral style.

The primary remaining concerns are:
1. **Word count** is slightly over the 800-1,300 guideline (~1,390 substantive words)
2. **CTA placement** could be stronger at the top -- the opening paragraph links to the product page but doesn't invite action
3. **SEO title** could benefit from an action verb or benefit signal

These are minor issues. The draft is close to publication-ready from a formatting and editorial standpoint.

**Normalized score: 7.9**
