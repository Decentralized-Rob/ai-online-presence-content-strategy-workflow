# UpRock AI GitHub Handoff Prompt

Use this prompt to start a new ChatGPT/Codex-style working chat for setting up UpRock.ai with this GitHub project.

```text
You are working in the GitHub repo `Decentralized-Rob/ai-online-presence-content-strategy-workflow`.

Work on the `kahmotor` branch only. Keep `main` generic and reusable.

Context:
This repo documents an independent public-source online presence workflow. The current company-specific test case is Kah Motor / Honda Singapore. Do not claim affiliation with Kah Motor, Honda Singapore, or Honda. Use public sources only. Separate verified facts, observations, assumptions, implementation ideas, and open questions.

Goal:
Set up UpRock.ai as an execution and verification tool for this repo. The purpose is not to promote UpRock. The purpose is to test whether UpRock can improve public-source research, crawl verification, SEO checks, source monitoring, and AI-agent workflow execution for this project.

Available UpRock context from the user:
- UpRock.ai dashboard is available at `https://uprock.ai/app`.
- Dashboard modules observed by the user include Crawler, Verify, and AI Sitemaps.
- Crawler is shown as live and says: "Fetch structured, AI-ready content. Any URL."
- Crawler can be used via API or MCP from Claude, Cursor, or an app.
- Crawler actions shown: Create new key, Manage keys, MCP setup.
- Verify is shown as live and says: "Your AI can verify its own work."
- Verify references real devices and 190+ countries.
- Verify actions shown: Install MCP, Add to Slack, Learn more.
- AI Sitemaps is visible as a live module.
- UpRock API overview URL supplied by the user: `https://uprock.ai/docs/api-reference/overview`.
- UpRock docs URL supplied by the user: `https://uprock.ai/docs`.

Primary repo files to inspect first:
- `README.md`
- `source-of-truth/kah-motor-source-of-truth.md`
- `research/public-presence-audit.md`
- `research/socials-and-web-presence.md`
- `research/seo-opportunity-map.md`
- `strategy/ai-automation-opportunities.md`
- `roadmap/implementation-roadmap.md`

If any of these files do not exist yet, create a minimal placeholder only when useful. Do not invent facts.

First task:
Create an UpRock setup plan for this repo under:
- `strategy/uprock-ai-integration-plan.md`

The plan should include:
1. What UpRock should be used for in this project.
2. What it should not be used for.
3. Exact first tests to run using Crawler, Verify, and AI Sitemaps.
4. Candidate URLs to test from the Kah Motor source files.
5. Output format for recording UpRock test results.
6. A lightweight execution log format.
7. Security notes for API keys and MCP setup.
8. Clear separation between public-source facts and user/product testing observations.

Recommended first UpRock tests:
- Crawl official Kah Motor homepage.
- Crawl official Honda Singapore model pages, if identified in the source-of-truth file.
- Crawl showroom/service pages, if identified.
- Test whether UpRock output is more structured or complete than normal browser/web fetch output.
- Use Verify to check one repo claim against one official source URL.
- Use AI Sitemaps to map the public website structure, if the module allows it.

Do not:
- Store API keys in the repo.
- Commit `.env` files.
- Claim that UpRock results are authoritative without source review.
- Scrape private data.
- Over-crawl or stress any public website.
- Use non-public/private company information.

Create or update these files if appropriate:
- `strategy/uprock-ai-integration-plan.md`
- `logs/uprock-test-log.md`
- `.gitignore` if API key/env patterns are missing

Suggested `.gitignore` entries if not already present:
- `.env`
- `.env.*`
- `*.local`
- `secrets/`
- `private/`

Output required at the end:
- Files inspected.
- Files created or updated.
- Branch used.
- Exact next action for the user inside UpRock.ai.
```

## Notes

This handoff intentionally treats UpRock as a tool under test, not as a verified source of truth. Public claims should still be checked against source URLs and logged separately from product behavior observed during testing.
