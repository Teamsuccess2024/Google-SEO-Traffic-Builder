**File path:** seo-traffic-builder/templates/90-day-roadmap.md

**90-Day SEO Roadmap**

**Why This Template Exists**

Most SEO efforts fail not because the strategy was wrong, but because nothing concrete got done. "Improve SEO" is not a plan. "Publish more content" is not a plan. A real plan specifies what gets done, in what order, by when, with what expected outcome.

This template is that plan. It is a week-by-week, task-by-task roadmap covering the first 90 days of SEO work on any site. It assumes the intake questionnaire has been completed and the audit has produced a prioritized fix list. From there, this roadmap turns priorities into scheduled action.

Three phases:

- **Days 1-30: Foundation** - fix what's broken, set up what's missing, prepare the site to compete
- **Days 31-60: Content Velocity** - produce the content that builds topical authority
- **Days 61-90: Authority and Optimization** - earn external signals, refine what's published, set the trajectory for months 4-12

The phases are sequential. Skipping foundation to jump into content produces content built on broken infrastructure. Skipping content to jump into link building produces a site with nothing worth linking to. Order matters.

**How To Use This Template**

Three workflows:

- **Claude tailors the roadmap** - based on intake and audit, Claude adjusts the generic plan to the user's specific site, resources, and priorities
- **User executes the roadmap** - using this as their weekly checklist, marking tasks complete, reporting progress
- **Hybrid** - Claude executes some tasks (content briefs, drafts, technical recommendations); user executes others (publishing, outreach, decisions)

The roadmap assumes:

- A solo operator or small team with 8-15 hours per week available for SEO work
- A site with existing content that needs optimization (or a new site with content production capacity)
- Standard CMS access (WordPress, Shopify, Squarespace, Webflow, or similar)
- No prior critical penalties or manual actions

For larger teams, scale tasks proportionally. For sites with severe issues, extend the foundation phase.

**Pre-Roadmap Requirements**

Before Day 1, the following must be complete:

- Intake questionnaire (templates/intake-questionnaire.md)
- SEO audit (templates/seo-audit-template.md)
- Keyword research initiated (templates/keyword-research-template.md)
- Topical clusters defined (3-5 primary clusters)
- Goals and 12-month vision documented

If any of these are incomplete, do not start the 90-day roadmap. Foundation work without strategic clarity produces motion without progress.

**Phase 1: Foundation (Days 1-30)**

The goal of this phase is to make the site competitive at the technical and structural level. Most sites lose ranking opportunities not because their content is bad but because their foundation is shaky. Fixing the foundation is the highest-leverage work in early SEO.

**Week 1: Tracking, Indexing, and Technical Triage**

The week dedicated to making sure measurement works and Google can crawl the site properly.

**Task 1.1 - Verify Google Search Console (1 hour)**

- Confirm property added (Domain property preferred)
- Confirm XML sitemap submitted
- Note current state: total impressions, clicks, indexed pages
- This is the baseline against which all progress is measured

**Task 1.2 - Verify Google Analytics 4 (1 hour)**

- Confirm tracking installed and firing
- Verify timezone, currency, data retention (14 months)
- Link GA4 to GSC
- Mark internal traffic to exclude own visits
- Note baseline organic sessions

**Task 1.3 - Define and configure conversions (1-2 hours)**

- Identify the primary conversion event
- Identify 2-3 secondary conversion events
- Set up tracking for each in GA4
- Verify firing in DebugView
- Mark as key events

**Task 1.4 - Run technical scans (2 hours)**

- PageSpeed Insights on homepage and 3 key page types
- Mobile-Friendly Test on key pages
- Schema validator on key pages
- Document baseline scores

**Task 1.5 - Address P1 technical issues from audit (3-5 hours)**

- The "Critical (P1)" items from the audit
- These are typically fast fixes with high impact
- Examples: removing accidental noindex, fixing robots.txt errors, repairing broken sitemap, resolving major mobile issues

**End of Week 1 deliverables:**

- Tracking confirmed working with conversions defined
- All P1 technical issues resolved
- Baseline metrics documented

**Week 2: Site Speed, Mobile, and Crawl Health**

**Task 2.1 - Image optimization sweep (3-4 hours)**

- Compress oversized images sitewide
- Convert to modern formats (WebP) where supported
- Implement lazy loading on below-fold images
- Add explicit dimensions to images in HTML
- Replace any obviously low-quality stock images with originals where high-leverage

**Task 2.2 - Core Web Vitals improvements (2-4 hours)**

- Address LCP issues identified in PageSpeed Insights
- Defer or async non-critical JavaScript
- Eliminate render-blocking resources where feasible
- Re-test after changes

**Task 2.3 - Mobile experience review (1-2 hours)**

- Test all major page templates on actual mobile devices, not just emulators
- Confirm touch targets, font sizes, no horizontal scroll
- Resolve any intrusive interstitials or popups blocking content
- Verify CTA visibility on mobile

**Task 2.4 - Crawl error cleanup (1-2 hours)**

- Pull crawl errors from Search Console Coverage report
- Fix or redirect 404s with internal link sources
- Eliminate redirect chains
- Resolve any 5xx errors with hosting if applicable

**End of Week 2 deliverables:**

- Core Web Vitals improved across key page types
- Mobile experience verified
- Crawl errors resolved or in active resolution

**Week 3: On-Page Foundation Across the Site**

**Task 3.1 - Title tag and meta description sweep (3-4 hours)**

- Identify pages with missing, duplicate, or weak titles and metas
- Rewrite for the top 20 traffic-earning pages first
- Use the formula: keyword positioned early + clear value proposition + brand
- Update via CMS

**Task 3.2 - Heading structure audit on key pages (2 hours)**

- Verify single H1 per page
- Confirm H1 includes target keyword
- Reorganize H2/H3 hierarchy where broken
- Replace generic headings ("Introduction," "Conclusion") with descriptive ones

**Task 3.3 - Schema implementation (2-3 hours)**

- Implement Organization schema on homepage
- Implement Article/BlogPosting schema on blog content
- Implement BreadcrumbList sitewide
- Implement Person schema on author pages (if they exist; if not, create them in week 4)
- Validate everything with Rich Results Test

**Task 3.4 - URL audit on key pages (1-2 hours)**

- Identify URLs that are non-descriptive or contain query parameters
- For new pages going forward, establish URL conventions
- Avoid mass URL changes on existing pages unless serious issues exist (URL changes require careful redirect implementation)

**End of Week 3 deliverables:**

- Top 20 pages have optimized titles and metas
- Schema implemented and validated on key page types
- Heading structure cleaned on key pages

**Week 4: E-E-A-T Foundation**

**Task 4.1 - Author pages (3-4 hours)**

- Create or rewrite an author page for each named contributor
- Include: real name, professional photo, 200-400 word bio, credentials, years of experience, links to published work, links to professional profiles, contact info, list of articles authored
- Implement Person schema on each
- Reference: references/e-e-a-t.md

**Task 4.2 - About page (2 hours)**

- Rewrite or create an About page that includes: site purpose, origin story, editorial standards, team, mission, affiliations, contact information
- Avoid marketing fluff; aim for honest specificity

**Task 4.3 - Contact and trust pages (1-2 hours)**

- Create or update Contact page with multiple working methods
- Confirm Privacy Policy, Terms of Service, Cookie Policy are present and current
- Create Editorial Policy page (how content is sourced, reviewed, updated)
- Create Disclosure Policy if relevant (affiliates, sponsorships, AI assistance)

**Task 4.4 - Author attribution on existing content (2-3 hours)**

- Audit existing content for missing or generic author attribution
- Add real author bylines linking to author pages
- Update Article schema with author property pointing to Person schema

**End of Week 4 deliverables:**

- Every named contributor has a complete author page
- About, Contact, and trust pages established
- E-E-A-T signals visible across the site

**End of Phase 1 Checkpoint:**

- Foundation complete: site is technically sound, on-page basics handled, E-E-A-T signals established
- Baseline metrics documented for comparison
- Ready to focus on content production at velocity

**Phase 2: Content Velocity (Days 31-60)**

The goal of this phase is consistent, high-quality content production aligned with the keyword research and topical clusters. Foundation makes the site competitive; content makes the site rank. This phase is where most of the writing happens.

Cadence: 2 substantive pieces per week minimum (8 total in this phase). Adjust up or down based on resources, but consistency matters more than volume.

**Week 5: Pillar Page Production Begins**

**Task 5.1 - Select first pillar page topic (1 hour)**

- Choose the highest-priority cluster from keyword research
- This pillar will anchor an entire content cluster
- Pillar topic should be broad enough to support 5-15 cluster posts but specific enough to dominate

**Task 5.2 - Write content brief for pillar (2 hours)**

- Use templates/content-brief-template.md
- Complete all 18 sections
- Conduct full SERP analysis
- Specify the outline in detail (this drives the entire piece)

**Task 5.3 - Draft pillar page (4-6 hours)**

- Pillar pages typically 2,500-5,000 words
- Cover the topic comprehensively
- Include all required E-E-A-T signals
- Embed planned internal links (will become useful as cluster posts publish)
- Include conversion path

**Task 5.4 - Edit and prepare for publish (2 hours)**

- Substantive editing pass
- Add original images/graphics
- Implement schema
- Set up internal links from existing relevant pages
- Configure tracking

**End of Week 5 deliverables:**

- First pillar page drafted, edited, and ready (publish at start of Week 6)

**Week 6: Pillar Publishes, First Cluster Posts Begin**

**Task 6.1 - Publish pillar page (1 hour)**

- Final review, schema validation, mobile check
- Publish
- Submit URL for indexing in Search Console
- Update internal links from related existing content within 24 hours

**Task 6.2 - Brief and draft Cluster Post 1 (5-6 hours)**

- A 1,200-2,000 word piece supporting the pillar
- Complete content brief with full SERP analysis
- Draft, edit, prepare for publish
- Include 2-3 internal links to the pillar

**Task 6.3 - Brief and draft Cluster Post 2 (5-6 hours)**

- Second cluster post supporting same pillar
- Same process as 6.2

**Task 6.4 - Email announcement of pillar (1 hour)**

- If email list exists, send a thoughtful announcement
- If no list yet, prioritize building one (next week)

**End of Week 6 deliverables:**

- Pillar page published
- 2 cluster posts drafted and ready to publish

**Week 7: Cluster Continues, Email Capture Activated**

**Task 7.1 - Publish Cluster Post 1 (Tuesday) (1 hour)**

**Task 7.2 - Publish Cluster Post 2 (Thursday) (1 hour)**

**Task 7.3 - Email capture system setup or improvement (3-4 hours)**

- If email tool not yet set up: choose one (ConvertKit, MailerLite, Beehiiv are common)
- Add email capture to: every blog post (mid-content and end), every book/product page, sidebar, footer, optional exit-intent
- Create a simple welcome sequence (3-5 emails) that introduces the site and primary content
- Configure conversion tracking for email signups

**Task 7.4 - Brief and draft Cluster Posts 3 and 4 (6-8 hours)**

- Continue building out the first cluster
- Each piece links to pillar and to other cluster posts where contextually relevant

**End of Week 7 deliverables:**

- 4 pieces of cluster content live or queued
- Email capture system operating sitewide

**Week 8: Cluster Completion and Second Cluster Begins**

**Task 8.1 - Publish Cluster Posts 3 and 4 (Tuesday/Thursday) (2 hours)**

**Task 8.2 - Begin second cluster: pillar brief (2 hours)**

- Select second-highest-priority cluster from keyword research
- Begin pillar brief

**Task 8.3 - Internal linking review on first cluster (2 hours)**

- Verify all 5 pieces (pillar + 4 cluster posts) link to each other where contextually appropriate
- Update older content on the site to reference the new pillar where natural
- Aim for at least 5 inbound internal links to each new piece

**Task 8.4 - Search Console review (1 hour)**

- Check indexing status of new content
- Note any crawl errors or coverage issues
- Confirm impressions starting to register (clicks may not yet)

**End of Week 8 deliverables:**

- First cluster substantially complete (5 pieces)
- Second cluster initiated

**End of Phase 2 Checkpoint:**

- 5+ substantial pieces published
- One full cluster established with internal linking
- Email capture functional sitewide
- First impressions appearing in Search Console
- Trajectory established: 2 quality pieces per week sustainable

**Phase 3: Authority and Optimization (Days 61-90)**

The goal of this phase is to convert published content into ranked content, earn external authority signals, and refine what's working. Foundation made the site competitive. Content gave it something to rank with. This phase focuses on getting it ranked and amplifying impact.

**Week 9: Second Cluster Production + Optimization Begins**

**Task 9.1 - Publish second cluster pillar (1 hour)**

**Task 9.2 - Brief and draft 2 cluster posts for second cluster (8-10 hours)**

**Task 9.3 - First content optimization pass (3-4 hours)**

- Pull Search Console data on first cluster pieces (now 30+ days old)
- Identify pieces ranking on page 2 (positions 11-20) - these are highest-leverage optimization targets
- For each: analyze the gap between this content and current page 1 results
- Apply targeted improvements: deeper coverage, additional sections, better internal linking, sharper E-E-A-T signals

**End of Week 9 deliverables:**

- 7+ pieces published
- First optimization pass on early content complete

**Week 10: Backlink Strategy Activation**

**Task 10.1 - Publish 2 more cluster posts (Tuesday/Thursday) (2 hours)**

**Task 10.2 - Identify link-worthy content assets (2 hours)**

- From the first cluster, identify the piece most likely to attract links (typically the pillar)
- Assess link-attracting strength: original framework? Useful data? Comprehensive resource?
- If the strongest piece isn't link-worthy enough, identify what would make it more so

**Task 10.3 - Outreach target list (2-3 hours)**

- Identify 30-50 sites that:
  - Cover the same topical area
  - Have published roundup, resource, or comparison content
  - Have linked to similar content from competitors (use Ahrefs/Semrush competitor backlink reports if available)
- Document each: site, contact, hook, what to ask for

**Task 10.4 - Begin outreach (2-3 hours)**

- Send 10 personalized outreach emails this week
- Use a clear pattern: introduce yourself, demonstrate familiarity with their work, offer specific value (your content as a resource, a guest post idea, a quote contribution)
- Avoid generic mass outreach - response rates collapse below 1%

**End of Week 10 deliverables:**

- 9+ pieces published
- Outreach list documented
- First 10 outreach emails sent

**Week 11: Continued Production and External Authority**

**Task 11.1 - Publish 2 cluster posts (2 hours)**

**Task 11.2 - Continue outreach (2-3 hours)**

- Send 10-15 more personalized outreach emails
- Respond to any replies promptly
- Track response rate, conversion rate, links earned

**Task 11.3 - Pursue 1-2 guest post or contribution opportunities (3-4 hours)**

- Pitch high-quality sites in the topical area
- Pitch specific topics, not generic offers
- Goal: 1 guest post placement per month to start

**Task 11.4 - Brand mention monitoring setup (1 hour)**

- Set up Google Alerts for brand name and key author names
- Set up notifications for when the site is mentioned without being linked
- These mentions become future link reclamation opportunities

**End of Week 11 deliverables:**

- 11+ pieces published
- 20-25 outreach emails sent
- 1-2 guest opportunities in progress
- Brand monitoring operational

**Week 12: Synthesis, Measurement, and Strategy for Months 4-12**

**Task 12.1 - Publish final 2 pieces of the 90-day phase (2 hours)**

- 13+ total pieces should be live by end of Week 12

**Task 12.2 - Full performance review (3 hours)**

- Pull Search Console data: impressions, clicks, CTR, average position trends
- Pull GA4 data: organic sessions, engagement, conversions
- Compare to Day 1 baseline
- Identify top performers and underperformers
- Document specific wins (pieces ranking, queries earning impressions, conversions)

**Task 12.3 - Second optimization pass (3 hours)**

- Apply optimization to any pieces from earlier weeks now stuck on page 2 or page 3
- Refine titles and metas on pieces with low CTR
- Add internal links from newer content to older content as cross-references mature

**Task 12.4 - 90-day report and forward plan (2-3 hours)**

- Document what was accomplished vs. planned
- Document what worked, what didn't, what to change
- Outline the next 90 days based on what was learned
- Adjust cluster priorities if signals suggest different topics deserve focus
- Reference: templates/monthly-report-template.md for structure

**End of Week 12 deliverables:**

- 13+ pieces published across 2 clusters
- Optimization passes complete on early content
- 25-30 outreach emails sent
- 1-3 backlinks earned (typical for first 90 days)
- Full performance review completed
- Month 4-12 plan drafted

**End of Phase 3 Checkpoint:**

- Foundation, content velocity, and authority work all in motion
- Compounding has begun (older content earning more impressions, internal linking strengthening)
- Sustainable production cadence established
- Clear data on what's working to inform next phase

**Realistic Expectations Through 90 Days**

Honest forecasting based on a properly executed roadmap:

**Day 30:**

- Technical foundation solid
- E-E-A-T basics established
- Tracking confirming activity
- New impressions appearing in Search Console (clicks may still be near zero)

**Day 60:**

- 5-8 pieces published
- First content earning consistent impressions
- Long-tail queries beginning to register
- Click-throughs starting on a few pieces
- Email list beginning to grow

**Day 90:**

- 13+ pieces published across 2 clusters
- Several pieces ranking on page 2 with optimization potential
- Some pieces on page 1 for long-tail queries
- Measurable organic traffic (often 100-500 monthly sessions for new sites; more for sites with existing authority)
- 1-3 earned backlinks
- Email list growing from sitewide capture

What 90 days does NOT typically produce:

- Top rankings on competitive head terms
- Tens of thousands of monthly visitors (unless site already had authority)
- Major revenue from organic traffic alone
- Complete topical authority

These come in months 4-12 and beyond, built on the foundation this 90 days establishes.

If the site is brand new and has no existing authority, expect the lower end of these ranges. If the site has existing pages, traffic, or links, expect higher.

**Adjustments by Site Type**

**For new sites with no content:**

- Foundation phase compressed slightly (less to fix)
- Content phase extended (need more pieces to establish topical authority)
- Authority phase focused on building first connections, not link building at scale

**For established sites with weak SEO:**

- Foundation phase extended (more cleanup needed)
- Content phase emphasizes optimization of existing content alongside new production
- Authority phase realistic - existing authority signals matter

**For sites in highly competitive niches:**

- All phases extended (90 days isn't enough to make significant ranking progress in saturated markets)
- Focus on long-tail and underserved sub-niches
- Authority phase critical - competitive niches require strong external signals

**For YMYL sites:**

- E-E-A-T work in foundation phase is non-negotiable
- Content production slower (every piece requires expert review)
- Authority signals from credentialed sources are essential

**For local service sites:**

- Foundation phase includes Google Business Profile optimization (references/local-seo.md)
- Content phase emphasizes location-specific landing pages
- Authority phase emphasizes local citations and reviews

**For ecommerce sites:**

- Foundation phase includes product schema, category page optimization
- Content phase mixes commercial pages and supporting content
- Authority phase emphasizes review generation

**Common Failure Patterns To Avoid**

**Falling behind early and giving up.** Missing Week 1 tasks doesn't ruin the plan; abandoning the plan because Week 1 was hard does. Adjust the schedule, but keep the discipline.

**Skipping foundation to publish content.** Content on broken foundations doesn't rank. Foundation work feels boring; doing it anyway is what separates sites that work from sites that don't.

**Publishing without briefs.** The brief is the content's quality assurance. Skipping it produces forgettable content that doesn't rank.

**Optimizing too early.** Pieces under 30 days old haven't shown what they can do. Premature optimization is wasted effort. Wait for data.

**Mass outreach without personalization.** Sending 200 generic emails produces 0 links. Sending 20 personalized emails produces 1-3.

**Tracking obsessively, executing rarely.** Daily Search Console refreshing doesn't move metrics. Publishing and optimizing does.

**Comparing to mature sites.** A 90-day-old site does not look like a 5-year-old site. Compare yourself to your Day 1 baseline, not to competitors with years of compounding.

**What Comes After Day 90**

The 90-day roadmap establishes the trajectory. Months 4-12 continue the work:

**Months 4-6:**

- Continue content velocity (2 pieces per week)
- Begin third and fourth clusters
- Continue outreach and link building
- First substantial ranking improvements typically appear in this window
- First meaningful organic traffic growth

**Months 7-9:**

- Topical authority becomes visible (ranking for queries beyond targets)
- Pillar pages begin to dominate their topics
- Email list compounds
- Brand search begins to grow
- First substantial backlinks from real outreach

**Months 10-12:**

- Compounding becomes visible
- Older content continues to gain rankings
- New content ranks faster as site authority grows
- Conversion paths producing meaningful business outcomes
- Strategy refinement based on accumulated data

By month 12, the work done in days 1-90 should be visibly paying off. By month 18-24, the trajectory is clear. By month 36, sites that committed to this discipline have substantially better outcomes than sites that pursued shortcuts or gave up.

**Final Principle**

Ninety days is a beginning, not an end. The roadmap exists to make the first 90 days productive - to produce real foundation, real content, and real momentum. None of those things finish on Day 90. They continue.

The sites that win in SEO are the ones that treat 90 days as the proof of concept and the next 90 days as the next phase. Compounding is the prize, and compounding requires consistency.

Execute the plan. Adjust based on what you learn. Keep going. The work compounds.

**End of 90-day-roadmap.md**