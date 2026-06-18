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

Date: completed via ChatGPT web fetch, not UpRock direct API  
Module: Crawler-equivalent public fetch  
Input URL: `https://www.honda.com.sg/`  
Goal: Check whether structured page extraction is useful for official website inventory.

### Test 2 — Crawl Kah Motor about page

Date: completed via ChatGPT web fetch, not UpRock direct API  
Module: Crawler-equivalent public fetch  
Input URL: `https://www.honda.com.sg/about-us/about-kah-motor.html`  
Goal: Extract official about/company facts for manual review before source-of-truth update.

### Test 3 — Verify first repo claim

Date: pending UpRock Verify  
Module: Verify  
Claim: `The main official website identified for Honda Singapore / Kah Motor work is https://www.honda.com.sg/.`  
Source URL: `https://www.honda.com.sg/`  
Goal: Test whether Verify can check a repo claim against an official public URL.

### Test 4 — AI Sitemap official website

Date: pending UpRock AI Sitemaps  
Module: AI Sitemaps  
Target URL: `https://www.honda.com.sg/`  
Goal: Inventory official page structure for source-of-truth expansion.

### Test 5 — Extraction comparison

Date: pending actual UpRock output  
Module: UpRock Crawler + manual review  
Input URL: pending model/service page  
Goal: Compare UpRock extraction quality against manual browser review.

## Completed tests

## Test 1 — Official homepage public fetch

Date: 2026-06-17 / 2026-06-18 session  
Module: ChatGPT web fetch; not direct UpRock API  
Input URL: `https://www.honda.com.sg/`  
Input claim, if any: none  
Device / region settings, if any: none  
Output type: parsed public HTML/text  
Cost / credits, if visible: not applicable  
Response time, if visible: not available

### Result

The official homepage produced a useful structured navigation inventory. It surfaced model categories, model pages, after-sales sections, shopping tools, feedback link, mailing list language, and footer links.

### Useful extracted facts

- The homepage title appears as `Honda - Kah Motor - Home`. Source: `https://www.honda.com.sg/`
- New car categories surfaced: Hatchback, Sedan, SUV & MPV, About e:HEV, Compare Now. Source: `https://www.honda.com.sg/`
- Model links surfaced: All-New Super-ONE, Jazz, Accord, Civic, All-New ZR-V, All-New STEP WGN, New Freed, HR-V, CR-V. Source: `https://www.honda.com.sg/`
- After Sales links surfaced: Service Appointment, Service & Product, Service Packages, KAH Privilege, Concierge Service, Off Peak Service Deal, Extended Warranty, Honda Key Drop Check In, 1 Hour Priority Service, 24 Hour Roadside Assistance, Pre-LTA Inspection Services, Free Coverage with New Tyres, OBU Installation, Accident Reporting Mobile Service, Service Information, Car Care Tips, One Stop Service, Complimentary Shuttle Service, Body Repair & Paint, Warranty, Insurance. Source: `https://www.honda.com.sg/`
- Other top-level links surfaced: Parts & Accessories, Rental & Leasing, Promotions, About Us, Careers, Our Locations, Contact Us. Source: `https://www.honda.com.sg/`
- Shopping tools surfaced: Calculator, Price Guide, Test Drive, Brochure. Source: `https://www.honda.com.sg/`
- The homepage displays `24 Hr Roadside Assistance` and phone number `6841 3838`. Source: `https://www.honda.com.sg/`
- Footer shows `© Copyright Kah Motor 2026. All Rights Reserved.` Source: `https://www.honda.com.sg/`

### Observations

- The homepage navigation supports the existing project assumption that after-sales and ownership content are likely high-value areas for SEO and customer-support workflows.
- The public fetch output was already structured enough to update the source-of-truth file with an official website inventory.
- Actual UpRock Crawler should be tested next to see whether it adds cleaner extraction, region/device options, sitemap grouping, or verification workflow value beyond this baseline.

### Assumptions / unresolved items

- Need exact URLs for each surfaced link before adding a final sitemap inventory.
- Need actual UpRock output to compare extraction quality.
- Need AI Sitemap output to test whether website structure is easier to map than manual navigation extraction.

### Repo update needed

- `source-of-truth/kah-motor-source-of-truth.md`: add verified website navigation inventory.
- `research/public-presence-audit.md`: add official website structure notes.
- `research/seo-opportunity-map.md`: use after-sales/service/warranty/insurance/parts pages as priority SEO targets.

## Test 2 — Kah Motor about page public fetch

Date: 2026-06-17 / 2026-06-18 session  
Module: ChatGPT web fetch; not direct UpRock API  
Input URL: `https://www.honda.com.sg/about-us/about-kah-motor.html`  
Input claim, if any: none  
Device / region settings, if any: none  
Output type: parsed public HTML/text  
Cost / credits, if visible: not applicable  
Response time, if visible: not available

### Result

The official About Kah Motor page produced useful company/background facts and after-sales claims for manual source-of-truth expansion.

### Useful extracted facts

- Page heading: `About Kah Motor`. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- Page subtitle: `The one and only official authorised distributor for Honda in Singapore`. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states Boon Siew Sdn. Bhd. was formed in 1957 by Tan Sri Loh Boon Siew. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states Tan Sri Loh met Soichiro Honda the next year and a business partnership was formed. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states Kah Motor Co. Sdn. Bhd. was set up in 1969 to further Honda automobile business in Malaysia and Singapore. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states Kah Motor has more than 50 years with the Honda brand. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page says Kah Motor works with Honda Research & Development Tochigi Co. Ltd to develop a model line-up optimised for Singapore. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page lists `Exclusive After-Sales Services`, `Reliable Warranty From Manufacturer`, `Proprietary Servicing Equipment`, `Specialist Care`, `Genuine Components`, `Round-the-clock Assistance`, `Islandwide Network`, and `Higher Resale Value` under `Why Kah Motor`. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states warranty coverage is `3 years or 100,000km, whichever comes first`. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states the Kah Motor Service Division has `198 Honda experts`. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`
- The page states there are `six strategically located service centres` and `two Body Repair & Paint Shops`. Source: `https://www.honda.com.sg/about-us/about-kah-motor.html`

### Observations

- The About page gives several authoritative trust claims that could support an audit section around warranty, after-sales, service network, and authorised distributor positioning.
- The warranty, service-centre, and service-division claims should be cross-linked to dedicated warranty/location/service pages before being used in external-facing analysis.

### Assumptions / unresolved items

- Need to verify whether `198 Honda experts`, `six service centres`, and `two Body Repair & Paint Shops` are current on separate service/location pages.
- Need actual UpRock Crawler output for comparison.
- Need Verify module test for the authorised-distributor claim.

### Repo update needed

- `source-of-truth/kah-motor-source-of-truth.md`: add verified About Kah Motor facts.
- `research/public-presence-audit.md`: add trust/authority and after-sales content observations.
- `strategy/ai-automation-opportunities.md`: consider ownership/warranty/service assistant ideas tied to official pages.
