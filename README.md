# Competitor Intelligence Briefer

**An agent skill that generates structured competitive intelligence briefings using only web search.** No API keys. No paid tools. No LinkedIn scraping. Just thorough research synthesized into actionable intelligence.

## What It Does

Give it your business and your competitors (or let it discover them), and it produces a comprehensive briefing covering:

- **Company profiles** — what each competitor does, their size, target market
- **Product & pricing analysis** — features, pricing models, free tiers
- **Market positioning** — how they describe themselves, key differentiators
- **Content & marketing strategy** — blog, social, video, SEO visibility
- **Recent moves** — launches, partnerships, funding, press coverage (last 90 days)
- **Hiring signals** — what they're hiring for and what it means strategically
- **Customer sentiment** — what users love and hate, review scores
- **Comparative analysis** — positioning map, feature gaps, pricing comparison
- **Strategic recommendations** — market gaps, competitive advantages, threats, quick wins

## Why This One?

Most competitor intelligence skills require paid API access (LinkedIn, Anysite, etc.) or complex tool chains. This skill works with **web search alone** — the one tool every major agent already has. That means it works out of the box with Claude Code, Hermes, Codex, Copilot, and any other SKILL.md-compatible agent.

It's also designed for **business operators, not developers**. The output is a briefing you can act on, not a JSON blob you need to parse.

## Installation

### Claude Code
```bash
cp -r competitor-intel-briefer ~/.claude/skills/
```

### Hermes Agent
```bash
cp -r competitor-intel-briefer ~/.hermes/skills/
```

### GitHub Copilot
```bash
cp -r competitor-intel-briefer .github/skills/
```

### OpenAI Codex
```bash
cp -r competitor-intel-briefer .codex/skills/
```

Or just drop the folder into whatever skills directory your agent uses.

## Usage

Just ask your agent:

- "Research my competitors in the Australian opal market"
- "Who are the top competitors for project management SaaS?"
- "Analyze what [Company X] has been up to lately"
- "Build me a competitive landscape for [industry]"
- "Compare [Company A] vs [Company B] vs [Company C]"

The skill activates automatically when it detects a competitive research request.

## Example Output

See [assets/example-briefing.md](assets/example-briefing.md) for a sample briefing.

## Requirements

- An agent that supports the SKILL.md standard
- Web search capability (built into most agents)
- No API keys or paid services needed

## License

MIT — use it however you want.

## Author

Built by [@opal-digger](https://github.com/opal-digger)
