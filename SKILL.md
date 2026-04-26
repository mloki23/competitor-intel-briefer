---
name: competitor-intel-briefer
description: >-
  Generate structured competitive intelligence briefings for any business,
  product, or market. Researches competitors via web search, analyzes their
  positioning, pricing, content strategy, hiring signals, and recent moves,
  then produces an actionable briefing with strategic recommendations.
  No API keys or paid tools required — works with web search alone.
  Use when asked to research competitors, analyze a market, compare businesses,
  scout competition, build a competitive landscape, or prepare a market briefing.
license: MIT
metadata:
  author: mloki23
  version: "1.0"
  category: business
---

# Competitor Intelligence Briefer

Generate structured, actionable competitive intelligence briefings using only web search. No API keys, no paid tools, no LinkedIn scraping — just thorough research synthesized into a briefing that tells you what your competitors are doing and what you should do about it.

## When to Use This Skill

- "Research my competitors"
- "What are my competitors doing?"
- "Analyze the competitive landscape for [industry/product]"
- "Who are the top players in [market]?"
- "Compare [Company A] vs [Company B]"
- "What's [competitor] up to lately?"
- "Prepare a competitive briefing"
- "Scout the competition for my [business type]"

## Inputs

Ask the user for (if not already provided):

1. **Their business/product** — what they do, who they serve
2. **Known competitors** — any competitors they already know about (optional)
3. **Focus areas** — what matters most to them (optional, default to all)

If the user gives you a business description but no competitor names, discover competitors through research.

## Research Process

### Phase 1: Competitor Discovery (if needed)

Search for competitors using queries like:
- `[industry] competitors [year]`
- `[product type] alternatives`
- `best [product/service type] companies`
- `[known competitor] vs`

Identify 3-5 primary competitors. For each, confirm they are genuinely competing for the same customers.

### Phase 2: Per-Competitor Deep Dive

For EACH competitor, research these dimensions. Use multiple searches per competitor — do not rely on a single search.

#### 2a. Company Overview
- What they do (in one sentence)
- Founded when, where based
- Company size (employees, funding if applicable)
- Target customer profile

Search: `[competitor name] company overview`, `[competitor name] about`

#### 2b. Product & Pricing
- Core product/service offering
- Pricing model and price points (search their pricing page)
- Free tier or trial availability
- Key features or unique selling points

Search: `[competitor name] pricing`, `[competitor name] features`, `[competitor name] review [year]`

#### 2c. Market Positioning
- How they describe themselves (tagline, homepage messaging)
- What market category they claim
- Key differentiators they emphasise

Search: `[competitor name] homepage`, `site:[competitor domain]`

#### 2d. Content & Marketing Strategy
- Blog frequency and topics
- Social media presence and engagement
- Content formats (video, podcast, newsletter, etc.)
- SEO visibility — what terms they rank for

Search: `[competitor name] blog`, `[competitor name] social media`, `[competitor name] youtube OR podcast`

#### 2e. Recent Moves (Last 90 Days)
- New product launches or features
- Partnerships or integrations announced
- Funding rounds or acquisitions
- Leadership changes
- Press coverage

Search: `[competitor name] news [year]`, `[competitor name] launch OR announce`

#### 2f. Hiring Signals
- What roles they're hiring for (indicates strategic direction)
- Hiring volume (growing or stable)

Search: `[competitor name] careers`, `[competitor name] hiring`

#### 2g. Customer Sentiment
- What customers praise
- Common complaints or weaknesses
- Review scores on relevant platforms

Search: `[competitor name] reviews`, `[competitor name] complaints`, `[competitor name] reddit`

### Phase 3: Comparative Analysis

After researching all competitors, synthesize:

1. **Positioning Map** — how each competitor positions relative to others (premium vs budget, simple vs feature-rich, etc.)
2. **Feature Gap Analysis** — what features/services are common vs unique
3. **Pricing Comparison** — side-by-side pricing if available
4. **Strength/Weakness Matrix** — each competitor's strongest and weakest dimensions

### Phase 4: Strategic Recommendations

Based on the research, provide:

1. **Market Gaps** — underserved segments or unmet needs you spotted
2. **Competitive Advantages** — where the user's business could win
3. **Threats to Watch** — competitors making aggressive moves
4. **Quick Wins** — specific, actionable things the user could do this week
5. **Long-term Plays** — strategic positions worth building toward

## Output Format

Structure the briefing as follows:

```
# Competitive Intelligence Briefing
## [User's Business/Market]
### Generated: [Date]

---

## Executive Summary
[3-5 sentence overview of the competitive landscape and key findings]

---

## Competitor Profiles

### [Competitor 1 Name]
- **What they do:** [one sentence]
- **Size:** [employees/funding/revenue if known]
- **Target customer:** [who they serve]
- **Pricing:** [model and price points]
- **Key strengths:** [2-3 bullets]
- **Key weaknesses:** [2-3 bullets]
- **Recent moves:** [notable activity in last 90 days]
- **Hiring signals:** [what roles, what it suggests]

[Repeat for each competitor]

---

## Comparative Analysis

### Positioning Map
[Describe where each player sits — e.g. "X targets enterprise at premium pricing while Y focuses on SMBs with freemium"]

### Feature Comparison
| Feature | Competitor 1 | Competitor 2 | Competitor 3 | Your Business |
|---------|-------------|-------------|-------------|---------------|
| [Feature] | ✅/❌ | ✅/❌ | ✅/❌ | ✅/❌ |

### Pricing Comparison
[Side-by-side pricing table or summary]

---

## Strategic Recommendations

### Market Gaps
[Opportunities no one is addressing well]

### Your Competitive Advantages
[Where you can win based on what competitors lack]

### Threats to Watch
[Competitors making moves that could impact you]

### Quick Wins (This Week)
1. [Specific actionable item]
2. [Specific actionable item]
3. [Specific actionable item]

### Long-term Plays (3-6 Months)
1. [Strategic recommendation]
2. [Strategic recommendation]

---

## Sources
[List key sources referenced during research]
```

## Important Guidelines

- **Be specific, not generic.** Every recommendation should reference actual findings from the research. "Improve your marketing" is useless. "Competitor X is ranking for [keyword] with [content type] — you should create [specific content]" is actionable.
- **Flag uncertainty.** If you couldn't find pricing, say so. If information seems outdated, note it. Never fabricate data.
- **Prioritise recency.** A blog post from last month matters more than a review from 2022. Always note when information was published.
- **Research thoroughly but don't loop.** Use 3-5 searches per competitor, but cap total research at 15-20 searches maximum. Once you have solid data on the major players, STOP researching and compile. Perfectionism kills delivery — a good briefing now beats a perfect briefing never. If some data is missing, note the gap and move on.
- **Compile promptly.** After completing your research searches, immediately write the briefing. Do not run additional "just one more" searches. The research phase and the writing phase are separate — finish one before starting the other.
- **Review before saving.** Scan the final output for formatting artifacts, encoding glitches, repeated phrases, or broken markdown tables. Fix any issues before saving.
- **Save the briefing.** If the agent supports file output, save the briefing as a markdown file the user can keep.

