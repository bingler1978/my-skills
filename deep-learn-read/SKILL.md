---
name: deep-learn-read
description: "Book-anchored deep learning - use a specific book as a lens to understand its field, map consensus and controversy around its core topics, evaluate the book's position and worth, and prepare for deep discussion. Use this skill whenever the user wants to: prepare to read a book, understand what a book argues and whether it's worth reading, analyze a specific book's position in its field, study a book's topics through the book's lens, or says things like 'help me read [book]', 'I want to study [book title]', 'prepare a reading guide for [book]', 'analyze [book] for me', 'is [book] worth reading', 'what does [book] argue'. Also trigger when the user mentions a specific book title with intent to study or discuss it, uploads a book file (PDF/EPUB), or wants to understand a field through a specific book. Do NOT trigger for general topic research without a specific book — that's deep-learn-prep's job."
---

# Deep Learn Read: 以书为镜的深度学习

You are helping the user use a specific book as an entry point into a field of knowledge. The book is not the destination — it's a lens. Through this one author's argument, the user wants to understand a broader intellectual landscape: what the field agrees on, where genuine disagreements exist, how this book's ideas connect to today's world, and whether this book is worth their sustained attention.

## Core Philosophy

Every serious book is one voice in a larger conversation. The author saw a problem, disagreed with how others understood it, and built a case for a different way of seeing. Your job is to help the user hear that voice clearly — but also to hear the conversation around it: who agrees, who pushes back, what the mainstream thinks, and what all of this means for the world today.

This is the key difference from deep-learn-prep: prep starts from a field and pulls from many sources equally. This skill starts from one book and radiates outward — using the book's argument as the organizing thread for exploring its field. The book is the anchor, but the ocean is the real subject.

Think of it as equipping the user to walk into a dinner party where this book is being discussed by experts, critics, and enthusiasts. They should be able to hold their own — not just summarize the book, but engage with the ideas, spot the controversies, and form their own judgment about whether the author got it right.

## When to Use This Skill vs. deep-learn-prep

- **This skill (deep-learn-read)**: The user names a **specific book**. The book is the starting point, but the goal is broader understanding.
- **deep-learn-prep**: The user names a **topic or field** without a specific book as anchor.

If the user says "I want to learn about behavioral economics," that's deep-learn-prep. If they say "I want to read *Thinking, Fast and Slow*," that's this skill — and the output should help them understand not just Kahneman's argument, but where behavioral economics stands today, what's settled, and what's still being fought over.

## Workflow

### Stage 1: Confirm the Book

Confirm the specific book (title + author). If the user provides a file (PDF/EPUB), even better — direct access to the text is gold.

Don't ask about "reading modes" or make the user choose a plan. The user wants to understand the book and its field deeply, and they want to be ready for discussion. That's the default and only mode.

One useful thing to briefly ask: has the user already started reading? If yes, find out where they are — this lets you connect your analysis to what they've already encountered.

### Stage 2: Research — The Book AND Its World

This is where deep-learn-read diverges most from the first version. You research not just the book, but the broader intellectual territory it occupies. The book's argument is your guide through the field — follow the threads it raises.

#### 2.1 About the Author (3-4 searches)
- Academic/professional background, intellectual lineage, mentors and influences
- Other major works and how this book fits in their trajectory
- Known positions, biases, or intellectual commitments
- Interviews or talks where the author discusses this book specifically

#### 2.2 About the Book Itself (4-5 searches)
- Professional book reviews — academic journals, serious publications (NYRB, LRB, TLS), not just Amazon
- The book's reception: controversial? celebrated? ignored? misunderstood?
- Core thesis as described by multiple reviewers (cross-reference for consistency)
- Major scholarly responses — agreements, criticisms, extensions
- Awards, influence, citation patterns

#### 2.3 The Field Around the Book (5-6 searches) — THIS IS NEW AND CRUCIAL
Go beyond the book itself. For each major claim or topic the book raises, research the current state of knowledge:
- What does the mainstream academic consensus say about the book's core claims?
- Where do the book's positions align with current scientific/scholarly understanding?
- Where do the book's positions diverge from or challenge the mainstream?
- What has changed in the field since the book was published? Has evidence strengthened or weakened the author's case?
- What are the live controversies in this field that the book touches on?
- How do the book's ideas connect to current events, technology, society, or other fields?

#### 2.4 Competing and Complementary Perspectives (3-4 searches)
- What books/thinkers argue the opposite?
- What books/thinkers extend or build on similar foundations?
- What are the "must-know" alternative frameworks in this space?
- If someone read only this book, what blind spots would they have?

#### 2.5 If the User Uploaded the Book File
- Read the table of contents, preface/introduction, and conclusion first
- Skim chapter openings and endings to understand the argument arc
- Direct access to the text always beats secondary sources

#### Cross-Referencing Protocol
Same as deep-learn-prep: track evidence strength (Strong / Moderate / Weak / Contested). Pay special attention to:
- Where the book's claims align with broader academic consensus vs. where they're outlier positions
- Where reviewers agree about the book's argument vs. where they disagree about what it's saying
- Where evidence has shifted since publication

### Stage 3: Synthesize into Reading Guide

The core deliverable — a Markdown file that treats the book as a lens into its field.

```markdown
# 《[Book Title]》— 深度阅读指南
# [Book Title] — Deep Reading Guide

> 作者 (Author): [Author Name]
> 出版年份 (Year): [Year]
> 生成日期: [date]
> 参考资料数量: [N sources consulted, breakdown: N reviews, N academic sources, N interviews/talks]

---

## 一、这本书在说什么 (What This Book Is Really About)

Not a summary — an explanation of the book's core argument in 400-600 words. Write it the way a thoughtful expert would explain it to a smart friend from a different field:
- What problem or question does the author see?
- What is their central thesis?
- What is the key move — the insight or reframing that makes this argument distinctive?
- What would change in how you see the world if the author is right?
- Why does this argument matter beyond the academic field? What does it say about the world we live in today?

## 二、作者是谁 (Who the Author Is — and Why It Matters)

A brief intellectual portrait (200-300 words). Not a biography — focus on what shaped this book:
- Training, intellectual tradition, key influences
- Other major works and how this book fits in their trajectory
- Known commitments or biases a reader should be aware of
- Where they sit in the field: mainstream? maverick? bridge-builder?

## 三、这本书的论证地图 (The Book's Argument Map)

Chapter-by-chapter (or part-by-part) breakdown of HOW the argument builds. For each major unit:

### [Part/Chapter N]: [Chapter Title or Theme]
- **这一章在做什么 (Role in the argument)**: Sets up the problem? Provides evidence? Addresses objections? Draws conclusions?
- **核心论点 (Core claim)**: The chapter's main point in 1-2 sentences
- **关键证据/案例 (Key evidence)**: What the author uses to support the claim
- **与前后章节的关系 (Connection)**: How it builds on what came before and sets up what comes next

If working from the actual text, base this on the text. If not, construct from reviews and table of contents — and note uncertainty.

## 四、这本书在领域中的位置 (The Book's Position in Its Field)

This is the section that makes deep-learn-read more than just a book summary. Map where this book stands in relation to the broader field of knowledge:

### 这个领域的主流共识 (Mainstream Consensus in This Field)
5-7 points where the field broadly agrees. For each:
- The consensus position
- How this book relates to it (supports? builds on? takes for granted? challenges?)
- Evidence strength (well-established / evolving / recent)

### 这本书的独特贡献与争议 (The Book's Distinctive Claims — Where It Agrees and Where It Fights)
For each of the book's major claims, place it on a spectrum:
- Claims that are well-supported by the broader field (the book is voicing a consensus)
- Claims that are plausible but still being debated (the book is taking a side in a live controversy)
- Claims that are maverick or provocative (the book is pushing against the mainstream)

For each controversial claim:
- **书中的立场 (The book's position)**: The author's strongest argument
- **主流学界的看法 (Mainstream scholarly view)**: What most experts in the field think, with representative names/papers
- **为什么有分歧 (Why the disagreement exists)**: What makes this genuinely hard to settle
- **最新进展 (Recent developments)**: Has evidence shifted since publication?

### 这本书没说的 (What the Book Doesn't Cover)
- Important perspectives or evidence the book omits or underweights
- Neighboring fields or frameworks that would complicate or enrich the argument
- If someone read only this book, what would they miss about this topic?

## 五、与当今世界的关联 (Connections to Today's World)

Why does this book matter now? Connect the book's core ideas to:
- Current events, societal trends, or technological shifts
- Active public debates that the book's framework illuminates
- Other fields where the same questions are being asked differently
- What the book helps explain about the world we live in — and what it can't explain

This section is about relevance and cross-pollination. Help the user see why investing time in this book connects to things they already care about.

Important: tailor the connections to the user's actual interests and background (check auto-memory for their learner profile). Avoid defaulting to generic "hot topics" like climate change or environmental sustainability unless the book is specifically about those subjects. Prefer connections to domains the user works in or cares about.

## 六、作者的隐含假设与方法论 (Hidden Assumptions & Methodology)

What the author takes for granted without arguing for it:
- Methodological assumptions (favors case studies vs. statistics, assumes rational actors, privileges certain contexts)
- Philosophical or value commitments embedded in the argument
- What kinds of evidence the author finds persuasive — and what they ignore
- Blind spots identified by reviewers or critics

## 七、这本书值不值得深读 (Is This Book Worth a Deep Read?)

An honest, balanced assessment to help the user decide how much time to invest:

### 最受认可的贡献 (Most praised contributions)
- 2-3 points where reviewers broadly agree the book succeeds
- What specifically makes these arguments convincing

### 最受质疑的地方 (Most questioned aspects)
- 2-3 points where critics push back most strongly
- The strongest version of each critique (steel-manned)
- The author's likely defense

### 综合评估 (Overall Assessment)
A candid paragraph: who should definitely read this book? Who might be better served by alternatives? Is this the best entry point into this topic, or is there something more current/comprehensive? What kind of reader will get the most out of it?

## 八、深度讨论问题 (Deep Discussion Questions)

10 questions designed not for "reading comprehension" but for deep discussion — the kind you'd explore in a seminar or with a knowledgeable friend. These should:
- Require synthesis across the book's argument AND the broader field
- Force reasoning about whether the author got it right
- Connect the book's ideas to contemporary issues
- Have no simple lookup answers

For each:
### Q[N]: [Question]
- **考察维度**: What aspect of understanding does this test?
- **为什么这个问题有价值**: Why can't a surface-level reader answer this well?

## 九、关键术语表 (Key Terms & Concepts)

10-20 terms central to the book's argument. For each:
- The author's specific usage (which may differ from standard usage in the field)
- Why this term matters for following the argument
- Note if the author coins new terms or redefines existing ones

## 十、资料来源 (Sources)

Organized by type:
- **书评与学术评论**: Book reviews and academic responses (with links)
- **作者访谈/讲座**: Author interviews and talks
- **学术论文/综述**: Academic papers relevant to the book's claims
- **相关著作**: Related books and competing perspectives
- **课程材料**: University courses featuring this book (if any)
```

### Stage 4: Create Interactive Visual Map (.html)

Create a self-contained HTML file that helps the user see the book's argument AND its position in the field. This file must be directly openable in any browser — double-click from Finder/file manager and it just works.

Choose 2-3 visualization types from:

1. **Argument Flow Map** — The book's argument as an interactive flow diagram. Nodes = chapters/sections, edges = logical dependencies. Click a node to see core claim and evidence. Color-code by function: blue (foundational premises), green (evidence/cases), orange (addressing objections), purple (conclusions). Helps see where the argument is tight vs. has gaps.

2. **Field Position Map** — The book's claims plotted on a consensus-controversy spectrum. Green = aligned with mainstream consensus. Yellow = active debate. Red = maverick/challenged position. Clickable to reveal details of each position and the mainstream response. This is the visual analog of Section 四.

3. **Intellectual Conversation Map** — The book at center, surrounded by upstream influences and downstream responses. Clickable nodes reveal relationship nature (agrees, extends, challenges). Places the book in its intellectual ecosystem.

4. **Contemporary Relevance Web** — The book's core ideas connected to current-world topics, events, and cross-domain applications. Helps the user see why the book matters beyond its academic niche.

5. **Concept Network** — Key terms and concepts as an interactive network showing how the author's ideas relate to each other and to the broader field's vocabulary.

#### Technical Requirements
- Single `.html` file, self-contained, opens directly in any browser
- All CSS inline in `<style>` block, all JS inline in `<script>` block
- Use vanilla JavaScript for interactivity (no React, no framework dependencies)
- No external CDN links — everything must be embedded so the file works offline
- Clean typography, thoughtful color palette
- Color coding: green (consensus/supported), yellow-orange (debated), red (challenged/maverick), blue (foundational), purple (frontier/open)
- All data embedded as JS objects/arrays
- Responsive layout, works on both desktop and mobile browsers
- Include a concise title and subtitle at the top of the page identifying the book

Save as: `[workspace]/learning/topics/[book-slug]-visual.html`

### Stage 5: Save and Present

Save both files:
- Reading guide: `[workspace]/learning/topics/[book-slug].md`
- Visual map: `[workspace]/learning/topics/[book-slug]-visual.html`
- Create `topics/` subdirectory if it doesn't exist

Present to the user:
1. A concise summary of the most interesting findings — where the book aligns with the field, where it's provocative, what surprised you in the research, and the honest "is it worth it" verdict
2. Links to both files
3. Suggest which discussion questions are most worth exploring first
4. Let them know they can use deep-learn-discuss to dive into discussion (the discuss skill loads this guide as its knowledge base)

## Quality Standards

- **Book as lens, not destination**: The book anchors everything, but the real value is understanding the field and conversation around it. Don't just explain the book — map the territory it inhabits.
- **Prep-level rigor on field claims**: When you describe consensus or controversy in the field, apply the same cross-referencing standards as deep-learn-prep. Name researchers, cite papers, note evidence strength.
- **Steel-man the author**: Present the argument in its strongest form before introducing critiques.
- **Steel-man the critics**: Use the strongest version of critiques, not dismissive summaries.
- **Distinguish sources clearly**: "The author argues..." vs. "Mainstream consensus holds..." vs. "Reviewer X notes..." — always make the origin of claims explicit.
- **Be honest about gaps**: If reviews are sparse, if the field is too young for consensus, if you couldn't access the text — say so.
- **Make the "worth it" assessment genuinely useful**: Don't default to "yes, read it!" Be candid about the book's limitations and whether alternatives exist.
- **Connect to the present**: Always look for links between the book's ideas and the contemporary world. This makes abstract arguments tangible and relevant.

## Language

Write in the same language the user uses. Keep section headers bilingual (Chinese + English) for readability and searchability. Preserve technical terms in their original language where they are the standard.

## Integration with deep-learn-discuss

This guide is designed to work seamlessly with deep-learn-discuss. When the user wants to discuss:
- The discuss skill loads this guide as its knowledge base
- Discussion can focus on specific chapters, field controversies, or contemporary connections
- The "Deep Discussion Questions" provide ready-made prompts for Socratic dialogue
- Because this guide includes field-level consensus/controversy mapping, the discussion can go beyond the book itself into the broader intellectual landscape
