# Workflow Engine Map

Status: working framework  
Scope: reusable online presence and content strategy workflow  
Example case: Kah Motor / Honda Singapore  
Affiliation: none  
Source boundary: public sources only

## Purpose

This file maps the core engine behind the AI-assisted online presence workflow. The goal is to show how messy public brand information can be collected, structured, reviewed, and turned into practical content, SEO, automation, and implementation outputs.

This is not a claim of affiliation with any company. It is an independent workflow demonstration built from public information and clearly labeled assumptions.

## Core concept

The workflow turns unstructured public brand material into a structured operating system for online presence work.

Input sources are collected, normalized, separated by confidence level, and passed through a sequence of research and strategy nodes. Each node has a specific job. The output is not just content. The output is a reusable decision trail that shows where each recommendation came from and what still needs verification.

## Engine sequence

### 1. Source intake node

Collect public material relevant to the brand, company, product, or market.

Typical inputs:

- Official website pages
- Product or service pages
- Support, FAQ, warranty, booking, or after-sales pages
- Official social profiles
- LinkedIn company presence
- Press pages and public announcements
- Search result observations
- Public customer discussion, labeled as sentiment only
- Competitor examples, labeled separately

Output:

- Raw source list
- Date checked
- Source type
- Confidence level
- Initial notes

### 2. Source-of-truth node

Convert raw public material into a clean reference file.

This node separates:

- Verified facts
- Observations
- Assumptions
- Open questions
- Sentiment-only material
- Competitor references

Output:

- `source-of-truth/[company]-source-of-truth.md`
- Stable facts that later strategy files can safely reference
- Open questions that need further checking

### 3. Public presence audit node

Review how the company appears across public web surfaces.

Audit areas:

- Website structure
- Navigation clarity
- Search discoverability
- Ownership/support information
- Trust pages
- Reviews and reputation surfaces
- Social channel consistency
- Customer friction points visible from public sources

Output:

- `research/public-presence-audit.md`
- Gaps and strengths
- Evidence-backed observations
- No private or internal claims

### 4. SEO opportunity node

Turn source and audit findings into search-intent opportunities.

Opportunity categories:

- Buyer-intent queries
- Ownership and after-sales queries
- Service booking queries
- Warranty, insurance, parts, and maintenance queries
- Model comparison queries
- Location-specific queries
- FAQ and knowledge-base gaps
- Internal linking opportunities

Output:

- `research/seo-opportunity-map.md`
- Query themes
- Page ideas
- Content gaps
- Prioritized SEO opportunities

### 5. Content system node

Translate research findings into repeatable content structures.

Possible outputs:

- Website content briefs
- FAQ entries
- Social post angles
- LinkedIn post concepts
- X post concepts
- Customer-support explainer drafts
- Model or service page improvement notes
- Evergreen content templates

Output:

- `outputs/`
- Reusable content patterns
- Platform-specific drafts or briefs
- Clear source trail back to research files

### 6. AI automation opportunity node

Identify places where AI or automation could reduce friction or improve execution.

Common opportunity areas:

- Customer-facing assistants
- Service booking support
- Ownership and after-sales support
- FAQ and knowledge-base maintenance
- Review monitoring
- Search visibility monitoring
- Content refresh workflows
- Internal research summaries
- Agent-assisted operational workflows

Output:

- `strategy/ai-automation-opportunities.md`
- Practical automation ideas
- Required inputs
- Human review points
- Risk notes
- Estimated implementation complexity

### 7. Implementation roadmap node

Convert opportunities into an execution order.

Roadmap should separate:

- Low-friction updates
- Source-of-truth improvements
- SEO/content work
- Automation prototypes
- Human review needs
- Unknowns that block execution

Output:

- `roadmap/implementation-roadmap.md`
- Sequenced priorities
- Dependencies
- Suggested next actions

### 8. Execution log node

Track what changed, why it changed, and which source supported it.

Output:

- `execution-log.md`
- Date-stamped updates
- Files changed
- Source references
- Open follow-ups

## Human-in-the-loop checkpoints

Human review should occur before any output is treated as final or publishable.

Required checkpoints:

- Source verification before adding facts to the source of truth
- Strategy review before recommendations are framed as priorities
- Voice review before content is published or shared
- Legal/reputation review before making claims about a company, customer issue, or competitor
- Final review before anything is used in outreach, a pitch, or public content

## Confidence labels

Use these labels throughout the repo:

- Verified fact: directly supported by a public source
- Observation: visible pattern or gap based on reviewed public material
- Assumption: plausible interpretation that needs confirmation
- Sentiment only: public customer/commentary material that should not be treated as fact
- Open question: unresolved item that should not be used as a claim

## Generic workflow diagram

```text
Public Sources
    ↓
Source Intake
    ↓
Source of Truth
    ↓
Public Presence Audit
    ↓
SEO Opportunity Map
    ↓
Content System
    ↓
AI / Automation Opportunities
    ↓
Implementation Roadmap
    ↓
Execution Log
```

## Example application: Kah Motor / Honda Singapore

The Kah Motor branch applies this workflow to public-source research around Kah Motor / Honda Singapore.

The example should remain clearly labeled as independent research. It should not imply company approval, partnership, private access, or insider knowledge.

The example case is useful because it can demonstrate:

- How the source-of-truth file is built
- How public presence gaps are identified
- How SEO opportunities are derived from public information
- How automation ideas can be connected to customer-facing friction
- How a reusable workflow can be shown through a specific public case study

## What this file does not solve yet

This file maps the engine. It does not yet define the full product layer.

Still needed:

- Client intake mechanism
- Dashboard or interface concept
- Human review workflow details
- Publishing and scheduling integrations
- Commercial model
- Reporting cadence
- Access control and permissions model

Those should live in separate files so the core workflow engine stays clean and reusable.
