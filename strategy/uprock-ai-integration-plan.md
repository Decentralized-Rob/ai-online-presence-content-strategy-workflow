# UpRock AI Integration Plan

Status: working setup plan  
Branch: `kahmotor`  
Repo: `Decentralized-Rob/ai-online-presence-content-strategy-workflow`  
Scope: Kah Motor / Honda Singapore public-source research workflow  
Affiliation: none  
Internal access: none

## Purpose

Use UpRock.ai as a tool for crawl, verification, sitemap, and workflow testing inside this public-source online presence project.

UpRock is not treated as a source of truth. It is treated as a tool under test. Public claims still need source URLs, review notes, and separation between verified facts, observations, assumptions, and implementation ideas.

## Project boundaries

- Use public sources only.
- Do not claim affiliation with Kah Motor, Honda Singapore, or Honda.
- Do not use private company data.
- Do not scrape personal data.
- Do not store API keys in GitHub.
- Do not commit `.env` files or local MCP secrets.
- Keep company-specific work on `kahmotor`.
- Keep `main` generic and reusable.

## What UpRock should be used for

### 1. Official-source crawling

Use UpRock Crawler to fetch structured content from official public URLs already identified in the source file.

Initial known official URLs:

- `https://www.honda.com.sg/`
- `https://www.honda.com.sg/about-us/about-kah-motor.html`

Candidate page types to add after verification:

- Model pages
- Test drive page
- Contact page
- Showroom / location pages
- Service and after-sales pages
- Warranty pages
- Insurance pages
- Parts and accessories pages
- Promotions pages
- Reviews / press pages

### 2. Verification checks

Use UpRock Verify to test whether a repo claim can be checked against an official public source URL.

Example claim to verify first:

> The official Honda Singapore / Kah Motor website identified for this project is `https://www.honda.com.sg/`.

Verification target:

- `https://www.honda.com.sg/`

### 3. AI Sitemap discovery

Use UpRock AI Sitemaps to map the public website structure if the module supports it.

Target:

- `https://www.honda.com.sg/`

Desired output:

- Major page groups
- Model page URLs
- Ownership / service URLs
- Contact / location URLs
- Promotions / press URLs
- Pages that look useful for SEO or customer-support research

### 4. Cross-checking normal fetch quality

Compare UpRock output against normal browser/web fetch output.

Track whether UpRock provides:

- Cleaner structure
- Better page extraction
- Region/device-aware results
- More complete metadata
- Better source links
- More usable content for repo updates

## What UpRock should not be used for

- Do not use it to generate unsupported claims.
- Do not treat its output as automatically authoritative.
- Do not use it to scrape private data.
- Do not use it to bypass access restrictions.
- Do not use it to over-crawl or stress public websites.
- Do not use it to collect personal information.
- Do not use it as a replacement for manual source review.

## First tests to run

### Test 1: Crawl homepage

Module: Crawler  
URL: `https://www.honda.com.sg/`  
Goal: Determine whether UpRock returns structured, AI-ready content useful for source-of-truth updates.

Record:

- Timestamp
- Input URL
- Module used
- Output summary
- Key extracted links
- Response time if visible
- Credits/cost if visible
- Whether the output was useful
- Manual review notes

### Test 2: Crawl Kah Motor about page

Module: Crawler  
URL: `https://www.honda.com.sg/about-us/about-kah-motor.html`  
Goal: Extract company/about information from the official page without adding assumptions.

Record:

- Exact claims found
- Source URL
- Whether claims belong in source-of-truth
- Any missing context

### Test 3: Verify one repo claim

Module: Verify  
Claim: `The main official website identified for Honda Singapore / Kah Motor work is https://www.honda.com.sg/.`  
Source URL: `https://www.honda.com.sg/`  
Goal: Test whether Verify can check a repo claim against a public source.

Record:

- Claim tested
- Source URL
- Result
- Evidence returned
- Confidence / status if provided
- Manual judgment

### Test 4: Generate or inspect AI Sitemap

Module: AI Sitemaps  
Target: `https://www.honda.com.sg/`  
Goal: Identify official website sections for source-of-truth expansion.

Record:

- Page groups found
- URLs surfaced
- Missing areas
- Useful SEO/customer-support opportunities
- Whether sitemap output needs manual cleanup

### Test 5: Compare extraction quality

Module: Crawler and standard browser/manual review  
Target: one official model page after identified  
Goal: Compare UpRock output quality against manual page review.

Record:

- UpRock extracted content
- Manually observed content
- Differences
- Missed sections
- Best use case

## Candidate URLs from current source file

Verified in repo source file:

- `https://www.honda.com.sg/`
- `https://www.honda.com.sg/about-us/about-kah-motor.html`
- `https://sg.linkedin.com/company/kahmotorsingapore`

Only the first two should be used for initial official website crawl tests. LinkedIn should not be crawled unless the tool behavior and terms are clear.

## Output format for UpRock test results

Use this format in `logs/uprock-test-log.md`:

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

## Security notes

- Store `UPROCK_API_KEY` locally only.
- Use `.env` for local testing, but do not commit it.
- Use GitHub repository secrets only if a GitHub Action is later added.
- Do not paste API keys into markdown files, issues, prompts, screenshots, or logs.
- Do not commit MCP config files if they contain tokens.
- Keep screenshots out of the repo unless they are intentionally scrubbed.

Current `.gitignore` already excludes:

- `.env`
- `.env.*`
- `node_modules/`
- Python cache files

Recommended future additions if local tooling expands:

- `*.local`
- `secrets/`
- `private/`
- `.mcp.local.json`

## How to judge UpRock value for this repo

Useful if it helps with at least one of these:

- Faster official URL inventory
- Cleaner structured extraction
- Better source checking
- Repeatable claim verification
- Website structure mapping
- SEO opportunity discovery from public pages
- Execution logs that make the project look operational, not theoretical

Not useful if it only returns generic summaries that still require the same manual work.

## Immediate next action for the user

Inside UpRock.ai:

1. Open Crawler.
2. Create or select an API key without exposing it in chat or GitHub.
3. Run a crawl for `https://www.honda.com.sg/`.
4. Save the output summary, extracted links, visible cost/credits, and any region/device settings.
5. Paste only the non-secret result into the next working chat or add it to `logs/uprock-test-log.md`.
