**File path:** seo-traffic-builder/templates/seo-audit-template.md

**SEO Audit Template**

**Why This Template Exists**

Every site that wants to improve its SEO must first know where it stands. An audit is the diagnostic that reveals what's broken, what's missing, what's working, and what to fix first. Without it, recommendations are guesses. With it, recommendations are surgical.

This template provides the full diagnostic checklist for assessing any existing site. It produces a prioritized fix list - not a 200-item dump, but a ranked plan that puts highest-impact, lowest-effort items first.

The audit covers six domains: technical foundation, on-page SEO, content quality, internal architecture, backlink profile, and competitive position. Each domain has its own checklist, severity scoring, and output format. Together they produce a complete picture.

This template is used at the start of every engagement (Phase 2 of the standard workflow) and revisited quarterly thereafter.

**How To Use This Template**

The audit takes 4-8 hours for a small site, longer for larger ones. Three workflows:

- **Claude conducts the audit** - based on what Claude can observe (sitemaps, public pages, Search Console data the user shares); produces the structured output
- **User conducts the audit** - using this template as a checklist with their own tools
- **Hybrid** - user pulls data from tools they have access to; Claude analyzes and structures the findings

Tools required (all free unless noted):

- Google Search Console
- Google Analytics 4
- A site crawler (Screaming Frog free tier covers 500 URLs; full version is paid)
- PageSpeed Insights (free)
- Mobile-Friendly Test (free)
- Structured Data Testing (Schema.org Validator and Google Rich Results Test, both free)
- Optional paid: Ahrefs, Semrush, Sitebulb, Ubersuggest

The output is a single audit document with findings, severity scores, and a prioritized action list.

**Audit Structure**

The full audit produces six domain assessments and one synthesis output. Work through them in order - each builds on the previous.

- Technical Foundation Audit
- On-Page SEO Audit
- Content Quality Audit
- Internal Architecture Audit
- Backlink Profile Audit
- Competitive Position Audit
- Synthesis and Prioritized Fix List

**Severity Scoring System**

Every finding is scored on two dimensions:

**Impact** - how much fixing this would improve SEO outcomes

- High: would meaningfully change rankings, traffic, or conversions
- Medium: would produce visible improvement but not transformative
- Low: minor improvement; matters at the margins

**Effort** - how much work is required to fix

- Low: under 1 hour or simple settings change
- Medium: 1-8 hours of focused work
- High: substantial project (days or weeks)

Priority is calculated by combining the two:

- High Impact + Low Effort = **P1 (Do First)**
- High Impact + Medium Effort = **P2 (Do Soon)**
- High Impact + High Effort = **P3 (Plan and Schedule)**
- Medium Impact + Low Effort = **P4 (Quick Wins)**
- Medium Impact + Medium/High Effort = **P5 (Consider)**
- Low Impact (any effort) = **P6 (Backlog)**

The synthesis output ranks all findings by priority. P1 and P4 items get done first because they produce the fastest wins.

**Domain 1: Technical Foundation Audit**

The base layer. If technical foundation is broken, nothing else matters. Check every item.

**1.1 Crawlability and Indexing**

- **Robots.txt exists and is configured correctly**
  - Located at yoursite.com/robots.txt
  - Allows crawling of public pages
  - Blocks admin, staging, private paths only
  - References XML sitemap
- **XML sitemap exists, is valid, and is submitted to Google Search Console**
  - Includes all important URLs
  - Excludes noindex pages, redirects, error pages
  - Updated automatically when content changes
  - Under 50,000 URLs and 50MB (split into multiple sitemaps if larger)
- **No accidental noindex tags on important pages**
  - Inspect homepage and key category/product/content pages
  - Common failure: noindex left on staging that propagated to production
- **Canonical tags configured correctly**
  - Self-referencing canonicals on most pages
  - Cross-domain canonicals only where intended
  - No conflicting signals (canonical pointing to different URL than internal links)
- **Pagination handled correctly**
  - Use rel="next"/"prev" or canonical to first page (Google's current preference)
  - Or self-canonical each paginated page
  - Avoid combining contradictory signals
- **No critical pages blocked by robots.txt or noindex**
  - Cross-check against Search Console Coverage report
  - Pages "excluded by noindex" should be intentional only
- **Search Console Coverage report reviewed**
  - Indexed page count matches expected publishing volume
  - "Crawled - currently not indexed" pages investigated
  - "Discovered - currently not indexed" pages investigated
  - Indexing errors documented
- **URL structure is clean**
  - Lowercase, hyphenated, descriptive slugs
  - No session IDs, tracking parameters, or unnecessary query strings
  - Consistent trailing slash policy
  - Reasonable depth (most pages 3 clicks or less from homepage)

**1.2 Site Speed and Core Web Vitals**

- **PageSpeed Insights scores reviewed for homepage and 3-5 key page types**
  - Mobile and desktop both checked
  - LCP under 2.5 seconds
  - INP under 200ms
  - CLS under 0.1
- **Search Console Core Web Vitals report reviewed**
  - Pages categorized as Good / Needs Improvement / Poor
  - Mobile and desktop both reviewed
  - Failing URLs documented
- **Largest Contentful Paint (LCP) issues addressed**
  - Largest above-fold element loads quickly
  - Hero images optimized (modern formats, properly sized, compressed)
  - Critical CSS inlined
  - Server response time reasonable (TTFB under 600ms)
- **Interaction to Next Paint (INP) acceptable**
  - JavaScript not blocking interactivity
  - Heavy third-party scripts deferred or async
  - Event handlers optimized
- **Cumulative Layout Shift (CLS) minimized**
  - Image dimensions specified
  - Ads and embeds reserve space
  - Fonts don't cause shift on load
- **Render-blocking resources minimized**
  - Critical resources prioritized
  - Non-critical CSS/JS deferred
- **Image optimization audit**
  - All images compressed
  - Modern formats (WebP, AVIF) used where supported
  - Lazy loading implemented for below-fold images
  - Image dimensions in HTML

**1.3 Mobile Usability**

- **Mobile-Friendly Test passed for key pages**
- **Responsive design works across screen sizes**
- **Touch targets (buttons, links) adequately sized**
- **Text legible without zooming**
- **No horizontal scrolling on mobile**
- **Interstitials and popups don't block content** (Google specifically penalizes intrusive interstitials on mobile)

**1.4 HTTPS and Security**

- **HTTPS implemented site-wide**
- **HTTP redirects to HTTPS automatically**
- **No mixed content warnings**
- **SSL certificate valid and current**
- **Security headers present** (HSTS, Content-Security-Policy where appropriate)

**1.5 Structured Data and Schema**

- **Schema markup implemented for relevant page types**
  - Organization on homepage
  - Article/BlogPosting on blog content
  - Product on product pages (ecommerce)
  - LocalBusiness on local sites
  - Person for author pages
  - BreadcrumbList sitewide
- **Structured data validates without errors**
  - Tested with Schema.org Validator
  - Tested with Google Rich Results Test
- **Search Console Enhancements report reviewed**
  - Rich results detected
  - No structured data errors
- **Schema reflects actual content** (no fake reviews, fabricated ratings, mismatched data)

**1.6 Crawl Errors and Server Issues**

- **404 errors reviewed** in Search Console and via crawler
  - Errors from external links: redirect to relevant content if substantial referrers
  - Errors from internal links: fix the source link
  - Old removed content: 410 if intentional, redirect if relevant alternative exists
- **Soft 404s identified and addressed**
  - Pages returning 200 but containing no real content
  - Search and category pages with no results
- **Server errors (5xx) investigated and resolved**
- **Redirect chains eliminated** (A → B → C → D becomes A → D)
- **Redirect loops eliminated**
- **Excessive redirects on the same URL investigated**

**1.7 International and Geographic Targeting**

(Skip if not relevant)

- **Hreflang implemented correctly for multi-language sites**
- **Country targeting set in Search Console where appropriate**
- **Geographic content served from same domain or properly subdomained**

**Technical Foundation Output**

Document findings in this format:
```
TECHNICAL FOUNDATION FINDINGS

Critical (P1):

\- \[Specific issue\] - \[Impact: High\] \[Effort: Low\]

Fix: \[Specific action\]

High Priority (P2):

\- \[Specific issue\] - \[Impact: High\] \[Effort: Medium\]

Fix: \[Specific action\]

(Continue through all findings)
```
**Domain 2: On-Page SEO Audit**

How well individual pages are optimized. Audit key page types: homepage, top 5 traffic-earning pages, top 5 commercial pages, top 5 underperforming pages.

**2.1 Title Tags**

For each audited page:

- **Title tag exists**
- **Length 50-60 characters**
- **Includes primary keyword**
- **Keyword positioned near the start**
- **Unique across the site (no duplicates)**
- **Compelling enough to win clicks (not generic)**
- **Brand name included where appropriate**

Common issues to flag:

- Missing title tags
- Truncated titles in SERPs (over 60 characters)
- Duplicate titles across multiple pages
- Generic titles like "Home" or "Blog Post"
- Keyword stuffing
- Title not matching page content

**2.2 Meta Descriptions**

For each audited page:

- **Meta description exists**
- **Length 140-160 characters**
- **Includes primary keyword naturally**
- **Promises specific value**
- **Includes soft call to action**
- **Unique across the site**

Common issues to flag:

- Missing descriptions (Google generates one, often poorly)
- Truncation in SERPs
- Duplicates across pages
- Descriptions that don't reflect actual content
- No call to action or value proposition

**2.3 Heading Structure**

For each audited page:

- **Single H1 per page**
- **H1 includes primary keyword or close variation**
- **H1 distinct from title tag (not identical, but related)**
- **H2s used for major sections**
- **H3s used for subsections under H2s**
- **Heading hierarchy is logical (no H3 without preceding H2)**
- **Headings include semantic keywords naturally**
- **Headings describe section content (not generic like "Introduction")**

**2.4 URL Structure (Per Page)**

- **URL is short and readable**
- **URL contains primary keyword**
- **No unnecessary query parameters**
- **No mixed case, special characters, or encoded spaces**
- **URL matches page topic clearly**

**2.5 Image Optimization (Per Page)**

- **All images have descriptive alt text**
- **Alt text describes the image, not the keyword**
- **Filenames are descriptive (not IMG_2843.jpg)**
- **Images sized appropriately (not 4000px wide on mobile)**
- **Modern formats used where possible**
- **Decorative images use empty alt="" (not omitted entirely)**

**2.6 Content Optimization (Per Page)**

- **Primary keyword appears in first 100 words**
- **Primary keyword appears in at least one H2**
- **Related keywords and semantic variations used naturally**
- **Content depth matches search intent (not too thin, not padded)**
- **Reading level matches audience**
- **No keyword stuffing**
- **Internal links present (3-10 contextual links per substantial page)**
- **External links to authoritative sources where claims need support**

**2.7 Schema Per Page**

- **Page-appropriate schema implemented**
- **Schema reflects actual content accurately**
- **Schema validates without errors**

**2.8 User Experience Signals**

- **Page loads quickly enough to retain attention**
- **Content is scannable (paragraphs, lists, headings, white space)**
- **No intrusive popups blocking content**
- **Clear primary CTA visible**
- **Mobile experience matches desktop quality**

**On-Page SEO Output**

Document findings per page type, not per individual page (unless single pages have unique critical issues). Format:
```
ON-PAGE FINDINGS

Page Type: \[Blog posts / Product pages / Category pages / etc.\]

Pages Audited: \[count\]

Recurring Issues:

\- \[Issue, e.g., "60% of blog posts missing meta descriptions"\] - \[Impact: Medium\] \[Effort: Medium\]

Fix: \[Specific action\]

Critical Single-Page Issues:

\- \[Specific page URL\]: \[Issue\]

Fix: \[Action\]
```
**Domain 3: Content Quality Audit**

The hardest domain to audit but often the highest-leverage. Quality is what core updates evaluate; technical perfection on weak content still gets demoted.

**3.1 Content Inventory**

- **Total page count documented**
- **Pages categorized by type** (homepage, category, product, blog, resource, legal/utility)
- **Pages categorized by traffic level** (high, medium, low, zero)
- **Pages categorized by age** (new, established, aging, stale)

**3.2 Helpfulness Assessment**

For sample pages across categories, evaluate:

- **Does the page provide substantial original value compared to other results?**
- **Is it written for humans first, search engines second?**
- **Does it demonstrate first-hand experience or genuine expertise?**
- **Does it answer the search intent fully?**
- **Would a reader land here, find what they needed, and want to come back?**
- **Is it the kind of page someone would bookmark, share, or recommend?**

Pages that fail multiple criteria are candidates for substantial improvement or removal.

**3.3 Content Freshness**

- **When was each page last updated?**
- **Are claims still accurate?**
- **Are referenced resources still available?**
- **Are external links still working?**
- **Are statistics current?**
- **Has the topic evolved since publication?**

Stale content presented as current is a frequent core update casualty.

**3.4 Thin Content Identification**

Flag pages that are:

- Under 300 words on substantive topics
- Largely auto-generated or templated
- Duplicate or near-duplicate of other pages
- Tag pages or archive pages with no original content
- Old promotional content no longer relevant
- AI-generated without substantial human contribution

**3.5 Cannibalization Check**

- **Multiple pages targeting the same keyword identified**
- **Decision made for each: consolidate, redirect, or differentiate**

When two or more pages compete for the same query, neither ranks well. Consolidation is usually the answer.

**3.6 E-E-A-T Signal Audit**

(Reference references/e-e-a-t.md for details)

- **Author attribution present on all content?**
- **Author pages exist with bios, credentials, photos?**
- **About page substantive and accurate?**
- **Contact page with multiple contact methods?**
- **Privacy policy, terms, editorial standards published?**
- **Citations and sourcing visible where claims are made?**
- **Original perspective, frameworks, or research present?**

**3.7 Content Gap Analysis**

What topics in your area of expertise are you missing?

- **Compare existing content against keyword research sheet** (which target keywords have no current content?)
- **Compare against top competitors** (what do they cover that you don't?)
- **Check People Also Ask boxes for your top queries** (which questions are unanswered on your site?)
- **Identify funnel-stage gaps** (do you have BOFU content, or only TOFU?)

**3.8 Conversion Path Audit**

- **Does every substantial page have a clear conversion path?**
- **Are CTAs visible and compelling?**
- **Is there an email capture mechanism on every page?**
- **Do internal links guide readers toward conversion or just provide navigation?**

**Content Quality Output**
```
CONTENT QUALITY FINDINGS

Inventory:

\- Total pages: \[N\]

\- High-traffic pages: \[N\]

\- Zero-traffic pages over 12 months old: \[N\]

\- Pages last updated over 24 months ago: \[N\]

Quality Patterns:

\- \[Pattern observed across multiple pages\]

Cannibalization:

\- \[Specific cases identified\]

Gaps:

\- \[Missing topical coverage\]

\- \[Missing funnel stages\]

Recommendations:

\- Pages to substantially improve: \[count + examples\]

\- Pages to consolidate: \[count + examples\]

\- Pages to remove or noindex: \[count + examples\]

\- Topics to add: \[list\]
```
**Domain 4: Internal Architecture Audit**

How the site is structured and how link equity flows. Often the biggest hidden lever.

**4.1 Site Architecture**

- **Maximum click depth from homepage** (most pages should be 3 clicks or fewer)
- **Logical category and subcategory structure**
- **Consistent URL hierarchy reflecting site structure**
- **Breadcrumbs present and matching site structure**

**4.2 Internal Linking Patterns**

- **Average internal links per page** (most substantial pages should have 5-15)
- **Orphan pages identified** (pages with no internal links pointing to them)
- **Pages with very few outbound internal links identified**
- **Anchor text distribution reviewed** (descriptive, varied, not all "click here")
- **Internal link patterns aligned with topical clusters**

**4.3 Link Equity Flow**

- **Most-linked pages identified** (these accumulate the most internal authority)
- **High-priority pages receive sufficient internal links**
- **Pages no one links to internally identified**
- **Footer and navigation links don't dominate (these pass less equity than contextual links)**

**4.4 Cluster and Pillar Structure**

- **Topical clusters identifiable in site structure**
- **Pillar pages exist and link to related cluster posts**
- **Cluster posts link back to pillars**
- **Cluster posts link to each other where contextually relevant**
- **No cluster has fewer than 5 supporting pieces**

**4.5 Navigation**

- **Main navigation reflects priorities, not exhaustive list**
- **Footer navigation includes key utility pages (About, Contact, Privacy)**
- **Search functionality works well if present**
- **Related content sections present on substantive pages**

**4.6 Sitemap and Crawl Path**

- **XML sitemap structure reflects content priorities**
- **HTML sitemap available for users (optional but useful)**
- **Crawler can reach all important pages**
- **No large sections of content reachable only through search or filters**

**Internal Architecture Output**
```
INTERNAL ARCHITECTURE FINDINGS

Click Depth:

\- Pages over 4 clicks deep: \[count\]

\- \[List of important pages buried too deep\]

Orphan Pages:

\- Pages with zero internal links: \[count\]

\- High-value orphans: \[list with URLs\]

Cluster Coverage:

\- Clusters with strong structure: \[list\]

\- Clusters with weak/missing pillar: \[list\]

\- Topics with no cluster organization: \[list\]

Linking Opportunities:

\- High-priority pages needing more inbound internal links

\- Anchor text issues requiring attention

\- Specific link additions recommended (page → page with anchor)
```
**Domain 5: Backlink Profile Audit**

External authority. Required tool: Search Console at minimum, ideally Ahrefs or Semrush for fuller analysis.

**5.1 Profile Overview**

- **Total referring domains**
- **Total backlinks**
- **Growth trajectory (gaining or losing domains over time)**
- **Most-linked pages on the site**
- **Domain Rating / Authority Score (directional, not absolute)**

**5.2 Quality Assessment**

- **Spot-check top 50 referring domains for quality**
  - Real sites in relevant niches: positive signal
  - Spam, link farms, irrelevant sites: negative signal
  - Mix of follow and nofollow links is normal
- **Identify any patterns suggesting manipulation**
  - Sudden link spikes from low-quality sources
  - Anchor text patterns over-optimized for commercial keywords
  - Reciprocal link arrangements
  - Network footprints (multiple sites with same hosting, design, ownership)

**5.3 Toxic Link Assessment**

- **Are there obvious spam links pointing to the site?**
  - Adult or gambling sites linking inexplicably
  - Foreign-language directories
  - Sites with no real traffic or content
- **Are there any reasons to consider a disavow file?**
  - Most sites do not need a disavow file
  - Only consider if there's a manual action or clear evidence of negative SEO

**5.4 Link Velocity and Patterns**

- **Steady acquisition over time vs. sudden spikes**
- **Anchor text distribution reasonable** (mix of brand, URL, and topical anchors; no over-concentration on commercial terms)
- **Geographic distribution of links makes sense for the audience**

**5.5 Competitor Backlink Comparison**

- **Top 3 competitors' referring domain count**
- **Domains linking to competitors but not to you (link gap analysis)**
- **High-value link opportunities identified from this analysis**

**5.6 Brand Mentions**

- **Unlinked brand mentions across the web** (opportunities to request links)
- **Citation consistency** (NAP - Name, Address, Phone - consistency for local sites)

**Backlink Profile Output**
```
BACKLINK PROFILE FINDINGS

Profile Snapshot:

\- Referring domains: \[N\]

\- Growth: \[trajectory\]

\- Authority: \[score directional\]

Quality:

\- Spam/toxic concerns: \[yes/no with detail\]

\- Manual action present: \[yes/no\]

\- Disavow recommended: \[yes/no with reasoning\]

Competitive Position:

\- Domains linking to competitors but not to us: \[count\]

\- Top 10 link opportunities identified: \[list\]

Recommendations:

\- Outreach targets: \[specific sites and approach\]

\- Content needed to attract links: \[specific topics\]

\- Brand mention reclamation opportunities: \[list\]
```
**Domain 6: Competitive Position Audit**

Where you stand against direct competitors in search.

**6.1 Competitor Identification**

- **Top 3-5 competitors identified for primary topical area**
- **Direct competitors (same business model) and indirect competitors (same audience, different model) both noted**

**6.2 Keyword Overlap and Gaps**

- **Keywords competitors rank for in top 10 that you don't**
- **Keywords you and competitors both rank for, with positions compared**
- **Keywords you rank for that competitors don't (your unique strengths)**

**6.3 Content Comparison**

- **Total content volume compared**
- **Topical coverage compared** (what clusters do they have that you don't?)
- **Content depth on shared topics** (their pillar page vs. yours)
- **Content freshness** (how often do they update?)

**6.4 SERP Visibility**

- **Estimated organic traffic compared** (Ahrefs/Semrush estimates are directional)
- **Share of voice on key topical terms**
- **Brand search volume comparison**

**6.5 SERP Feature Capture**

- **Featured snippets they own that you don't**
- **People Also Ask appearances**
- **AI Overview citations**
- **Image and video carousel presence**

**6.6 Authority Signals**

- **Their referring domain count vs. yours**
- **Their visible E-E-A-T signals vs. yours**
- **Their content production cadence vs. yours**

**Competitive Position Output**
```
COMPETITIVE POSITION FINDINGS

Competitors Analyzed:

\- \[Site 1\]

\- \[Site 2\]

\- \[Site 3\]

Where We're Strong:

\- \[Topics, keywords, or signals where we lead\]

Where We're Weak:

\- \[Topics, keywords, or signals where competitors lead substantially\]

Opportunity Gaps:

\- Keywords competitors rank for that we should target: \[list\]

\- Content topics they cover that we don't: \[list\]

\- SERP features they capture that we should pursue: \[list\]

Strategic Implications:

\- \[What this competitive picture tells us about strategy\]
```
**Synthesis: The Prioritized Fix List**

After all six domains have been audited, synthesize findings into one prioritized action list. This is the deliverable that turns audit into execution.

**Synthesis Format**
```
SEO AUDIT SUMMARY - \[SITE NAME\] - \[DATE\]

TOP-LINE FINDINGS:

\- \[3-5 sentence summary of the site's overall state\]

\- \[Identification of the single highest-leverage area for improvement\]

CRITICAL ISSUES (P1 - Do This Week):

1\. \[Issue\] | Impact: High | Effort: Low | Domain: \[Technical/On-Page/Content/etc.\]

Action: \[Specific fix\]

Expected outcome: \[What this should produce\]

2\. \[Issue\] | Impact: High | Effort: Low | Domain: \[Domain\]

Action: \[Specific fix\]

Expected outcome: \[What this should produce\]

(Continue for all P1 items)

HIGH PRIORITY (P2 - Do This Month):

1\. \[Issue\] | Impact: High | Effort: Medium | Domain: \[Domain\]

Action: \[Specific fix\]

Expected outcome: \[What this should produce\]

(Continue for all P2 items)

PLAN AND SCHEDULE (P3 - Do This Quarter):

\[Larger projects with high impact\]

QUICK WINS (P4 - Do When Time Permits):

\[Low-effort, medium-impact items\]

CONSIDER (P5):

\[Worth discussing before committing\]

BACKLOG (P6):

\[Document but don't prioritize\]

STRATEGIC RECOMMENDATIONS:

\- \[Bigger-picture suggestions that go beyond fix lists\]

\- \[Suggested next phase of SEO work\]

\- \[Resource allocation recommendations\]

WHAT WE'RE NOT FIXING (AND WHY):

\- \[Issues identified but consciously deferred or rejected, with reasoning\]
```
**How To Present The Synthesis To The User**

For users on mobile or who need the summary fast:

- Lead with the top-line finding (one sentence)
- List 3-5 P1 items with action and expected outcome
- Offer to expand into any specific area

For users needing the full picture:

- Present the full synthesis
- Walk through each section
- Confirm priority order with the user
- Build the execution plan from there

**Recommended Audit Cadence**

- **Initial audit** - at engagement start (this template, full)
- **Quarterly review** - focused re-audit on areas that changed or improved
- **Annual deep audit** - full template repeated to catch drift
- **Triggered audits** - after traffic drops, after major site changes, after Google algorithm updates

Sites that audit themselves on schedule catch problems while small. Sites that don't audit catch them only after damage compounds.

**Common Audit Mistakes To Avoid**

**Audit paralysis** - producing a 200-item checklist with no priority. Without prioritization, nothing gets fixed.

**Surface-level audits** - checking only what tools flag. Real audits include human judgment about content quality, intent match, and competitive positioning.

**Tool worship** - treating tool scores (DA, Site Health %, etc.) as ground truth. They're directional. Google's actual evaluation differs.

**Ignoring competitive context** - auditing the site in isolation. Most rankings are relative; what competitors do matters as much as what you do.

**Skipping content quality** - focusing on technical and on-page checks while ignoring whether the content actually deserves to rank. Technical excellence on weak content fails.

**Recommending everything** - a good audit recommends what matters most, not everything possible. Discipline in the synthesis is what makes audits useful.

**Not revisiting** - treating the audit as one-time. SEO conditions change continuously; audits must too.

**Final Principle**

An audit is not paperwork. It is the diagnostic that determines whether the next 6 months of SEO work hits the right targets. Sites that audit honestly and act on the findings see compounding improvement. Sites that audit superficially or ignore findings keep wondering why their efforts don't produce results.

Do the audit. Take the findings seriously. Prioritize ruthlessly. Execute on what matters most. The structure works when the discipline is there.

**End of seo-audit-template.md**