# UpRock AI Test Log

Status: active test log  
Branch: `kahmotor`  
Repo: `Decentralized-Rob/ai-online-presence-content-strategy-workflow`  
Scope: Kah Motor / Honda Singapore public-source workflow  
Affiliation: none  
Internal access: none

## Rules

- Log product behavior separately from public-source facts.
- Do not paste API keys, tokens, MCP secrets, private URLs, or unsanitized screenshots.
- Do not treat UpRock output as authoritative without checking the source URL.
- Do not add private company data.
- Treat public customer discussion as sentiment only unless independently verified.

## Test template

```md
## Test [number] — [short title]

Date:
Module:
Input URL:
Input claim, if any:
Device / region settings, if any:
Output type:
Cost / credits, if visible:
Response time, if visible:

### Result

[Short result]

### Useful extracted facts

- [Fact] — Source: [URL]

### Observations

- [Observation]

### Assumptions / unresolved items

- [Assumption or open question]

### Repo update needed

- [File path]
- [Change needed]
```

## Planned tests

### Test 1 — Crawl official homepage

Date: pending  
Module: Crawler  
Input URL: `https://www.honda.com.sg/`  
Goal: Check whether UpRock returns structured, AI-ready content useful for official website inventory.

### Test 2 — Crawl Kah Motor about page

Date: pending  
Module: Crawler  
Input URL: `https://www.honda.com.sg/about-us/about-kah-motor.html`  
Goal: Extract official about/company facts for manual review before source-of-truth update.

### Test 3 — Verify first repo claim

Date: pending  
Module: Verify  
Claim: `The main official website identified for Honda Singapore / Kah Motor work is https://www.honda.com.sg/.`  
Source URL: `https://www.honda.com.sg/`  
Goal: Test whether Verify can check a repo claim against an official public URL.

### Test 4 — AI Sitemap official website

Date: pending  
Module: AI Sitemaps  
Target URL: `https://www.honda.com.sg/`  
Goal: Inventory official page structure for source-of-truth expansion.

### Test 5 — Extraction comparison

Date: pending  
Module: Crawler + manual review  
Input URL: pending model/service page  
Goal: Compare UpRock extraction quality against manual browser review.

## Completed tests

None yet.
