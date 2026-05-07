**File path:** seo-traffic-builder/references/analytics-tracking.md

**Analytics & Tracking for SEO**

**Why This File Exists**

You cannot improve what you don't measure. SEO without analytics is guessing. This reference walks through the exact tracking stack every site needs, how to configure each tool, what metrics actually matter, and - just as importantly - what metrics to ignore.

Most site owners either don't track anything or track everything and drown. Both fail. This file gives you the middle path: a small number of high-signal metrics, reviewed on a predictable cadence, that tell you whether your SEO is working.

**The Core Tracking Stack**

Every site needs three free tools, in this order:

- **Google Search Console (GSC)** - How Google sees your site
- **Google Analytics 4 (GA4)** - How users behave on your site
- **Bing Webmaster Tools** - Optional but easy; captures Bing/DuckDuckGo data

Paid tools (Ahrefs, Semrush, Sitebulb, Screaming Frog) become valuable later but are not required to start. Do not delay launch waiting for paid tools.

**Google Search Console Setup**

**What It Tells You**

GSC is the single most important SEO tool because it shows you actual Google search data: which queries your site appears for, how often it gets clicked, what position it ranks at, and what technical issues Google encounters when crawling.

**Setup Steps**

- Go to search.google.com/search-console
- Click "Add property"
- Choose "Domain" property type (covers all subdomains and protocols) - this requires DNS verification, which is the most thorough method
- Alternatively, use "URL prefix" property type if DNS access is limited - verify via HTML file upload, HTML tag, or Google Analytics
- Submit your XML sitemap under Sitemaps in the left menu (typically yoursite.com/sitemap.xml)
- Wait 3-7 days for initial data to populate

**What To Check Weekly**

- **Performance report** - impressions, clicks, CTR, average position over the last 28 days
- **Coverage / Pages report** - pages indexed vs. not indexed, with reasons for exclusions
- **Enhancements / Core Web Vitals** - page experience signals
- **Manual actions** - should always be empty; if anything appears here, it's an emergency

**What To Check Monthly**

- **Top queries** - what searches are bringing traffic
- **Top pages** - which URLs are earning impressions
- **Countries/devices** - where users are and how they're accessing
- **Links report** - who's linking to you and to which pages

**Google Analytics 4 Setup**

**What It Tells You**

GA4 shows what happens after someone clicks through to your site. Where they go, how long they stay, what they do, and whether they convert.

**Setup Steps**

- Go to analytics.google.com
- Create an account, then create a property (use your site name)
- Set timezone and currency correctly - these cannot be retroactively fixed for existing data
- Choose "Web" as the platform
- Add your domain and a stream name
- Copy the Measurement ID (format: G-XXXXXXXXXX)
- Install the tracking code via:
  - Google Tag Manager (recommended for flexibility)
  - Direct code in your site's &lt;head&gt; section
  - Native plugin (WordPress: Site Kit, MonsterInsights, GA Google Analytics)
- Verify installation in GA4 Real-time report by visiting your own site

**Critical Configuration After Install**

These settings are not on by default and must be enabled:

- **Enable Google signals** - Admin → Data Settings → Data Collection → toggle on Google signals data collection (enables demographics and cross-device tracking)
- **Extend data retention** - Admin → Data Settings → Data Retention → change from default 2 months to 14 months (the maximum free tier allows)
- **Link Search Console** - Admin → Product Links → Search Console Links → connect your GSC property (this puts search query data inside GA4 reports)
- **Link Google Ads if running ads** - same path, different product
- **Mark internal traffic** - Admin → Data Streams → your stream → Configure tag settings → Define internal traffic → add your office/home IP so your own visits don't pollute data
- **Set up enhanced measurement** - should be on by default; verify under your data stream settings (tracks scrolls, outbound clicks, site search, video engagement, file downloads automatically)

**Conversion Tracking**

**Why This Matters Most**

Traffic that doesn't convert is a vanity metric. Conversion tracking is what separates real SEO measurement from theater.

**Define Your Conversions Before Setup**

Write down what counts as a conversion for your site. Examples:

- Email signup
- Free download/lead magnet click
- Contact form submission
- Phone call (requires call tracking)
- Purchase completion
- Account creation
- Reaching a specific page (e.g., /thank-you)
- Engagement threshold (read 75% of an article, watched 50% of a video)

Pick a primary conversion (the one that drives revenue) and 2-3 secondary conversions (leading indicators).

**Setting Up Conversions in GA4**

GA4 calls conversions "key events." Setup:

- Identify the event you want to track (page_view to a thank-you page, form_submit, file_download, etc.)
- Admin → Events → check if the event already fires; if not, create it
- Once the event fires, Admin → Events → toggle "Mark as key event"
- Test by completing the action yourself and checking Real-time → Events

**For Form Submissions Specifically**

If your forms don't redirect to a thank-you page:

- Use Google Tag Manager to fire an event on form submission
- Or use the form plugin's built-in GA4 integration (Gravity Forms, WPForms, Contact Form 7 with extensions)
- Verify the event fires in GA4 DebugView before marking it as a conversion

**For Ecommerce Sites**

Enable enhanced ecommerce tracking. This requires implementing the GA4 ecommerce data layer (purchase, add_to_cart, view_item events). Most ecommerce platforms have plugins or built-in GA4 integration. Verify in DebugView that purchase events include transaction ID, value, and items array.

**The Metrics That Actually Matter**

Out of dozens of available metrics, focus on these. Everything else is supporting context.

**Tier 1 - Watch These Always**

**Organic sessions (GA4)** The number of visits from organic search. The single best indicator of SEO health over time. Track month-over-month and year-over-year.

**Conversions from organic (GA4)** Of those organic visitors, how many took the action that matters. Without this, traffic numbers are meaningless.

**Total clicks from search (GSC Performance)** Real clicks from Google to your site. Should trend upward over months as your SEO matures.

**Total impressions (GSC Performance)** How often your pages showed up in search results. Rising impressions with flat clicks means your titles/descriptions need work. Rising impressions with rising clicks means SEO is working.

**Tier 2 - Watch These Weekly**

**Average CTR (GSC)** Click-through rate from search results. Site-wide healthy range is 2-5%. Specific high-ranking pages should hit 5-15%+. Low CTR on high-impression pages means rewrite the title and meta description.

**Average position (GSC)** Where your pages rank on average across all queries. Less precise than per-keyword rank tracking but useful as a directional signal.

**Top landing pages from organic (GA4)** Which pages are actually pulling search traffic. Concentrate optimization effort here - small wins on high-traffic pages outweigh big wins on low-traffic pages.

**Engaged sessions / engagement rate (GA4)** GA4's replacement for the old "bounce rate." Engaged sessions are visits that lasted 10+ seconds, had a conversion, or had 2+ page views. If engagement rate is low, the content isn't matching what searchers expected.

**Tier 3 - Watch These Monthly**

**Indexed pages (GSC Coverage)** How many of your pages are actually in Google's index. Sudden drops mean technical issues. Sudden rises without you publishing mean possible spam or duplicate content problems.

**New referring domains (GSC Links)** How your backlink profile is growing. Slow steady growth is healthy. Sudden spikes can be either great PR or spam attacks - investigate.

**Core Web Vitals (GSC)** LCP, INP, and CLS scores. If any are red, page experience is hurting rankings. Fix red metrics before optimizing anything else.

**Queries you rank for (GSC)** Total unique queries pulling impressions. Broader query coverage = stronger topical authority over time.

**Metrics To Ignore**

These look meaningful but mislead:

- **Domain Authority / Domain Rating** - third-party scores from Moz/Ahrefs that Google does not use. Useful for relative comparison only, not as a goal.
- **Page count indexed in Bing** - almost always lower than Google and not a reliable signal of either platform.
- **Total backlinks** - quantity is meaningless; quality and relevance are everything. Ten links from real industry sites beat a thousand from directories.
- **Keyword density** - not a Google ranking factor. Write naturally.
- **Time on page (in isolation)** - high time on page can mean engaged readers OR confused users hunting for the answer. Pair with conversion data before drawing conclusions.
- **Real-time visitor count** - interesting but not actionable. Don't make decisions from real-time data; wait for stable trends.
- **Vanity rank for one specific keyword** - single-keyword obsession blinds you to broader topical performance. Ranking #1 for one term while losing visibility on twenty related terms is a net loss.

**How To Read GSC Performance Reports**

The Performance report is GSC's most-used screen. Here's how to actually use it:

**Compare Date Ranges**

Default view shows last 3 months. Toggle "Compare" → "Compare last 28 days year over year" to see real growth. Without comparison, single numbers tell you nothing.

**Filter By Query**

Type a query in the filter to see exactly which pages rank for it, what position, and how often it gets clicked. Use this to:

- Find pages ranking on page 2 (positions 11-20) - these are quick-win optimization candidates
- Find queries where you have impressions but low CTR - title/meta rewrite candidates
- Find queries you didn't intend to rank for - content expansion opportunities

**Filter By Page**

Click "Pages" tab, then click a specific URL to see all queries that page ranks for. This reveals what Google thinks the page is about, which often differs from what you intended. Discrepancies are signals to tighten the content's focus.

**The 28-Day Lag**

GSC data updates daily but with a 2-3 day delay. Monthly trends are reliable; daily fluctuations are noise.

**How To Read GA4 Reports**

GA4's interface frustrates many users. These are the screens worth your time:

**Reports → Acquisition → Traffic Acquisition**

Filter by "Session default channel group = Organic Search." Shows sessions, engagement, and conversions specifically from search engines. This is your primary SEO scorecard.

**Reports → Engagement → Pages and Screens**

Add a filter for organic search traffic. Shows which specific pages are receiving organic visits. Sort by sessions descending to see your top SEO performers.

**Reports → Engagement → Landing Page**

Specifically tracks which page someone first arrived on. For SEO, this is more useful than the general Pages report because it isolates entrance pages.

**Explore (Custom Reports)**

GA4's pre-built reports are limited. For real analysis, build a custom Exploration:

- **Dimensions:** Landing page, session source/medium
- **Metrics:** Sessions, engaged sessions, conversions, total revenue
- **Filter:** Session medium = organic
- **Sort:** Sessions descending

This becomes your weekly SEO dashboard.

**Reporting Cadence**

How often to review what:

**Daily (5 minutes, only after launch or after major changes):**

- GSC Coverage report for indexing errors
- GA4 Real-time to confirm tracking still works

**Weekly (20 minutes):**

- GSC Performance report - clicks, impressions, CTR trends
- GA4 organic sessions and top landing pages
- Note any sudden drops or spikes

**Monthly (60 minutes):**

- Full review using the monthly report template
- Compare month-over-month and year-over-year
- Identify wins to expand and losses to investigate
- Update the strategy based on what's working

**Quarterly (2-3 hours):**

- Strategic review - is the overall direction working?
- Backlink profile audit
- Content audit (which pages to update, consolidate, or remove)
- Competitor benchmark check

Anything more frequent than weekly is usually anxiety, not analysis. Resist the urge to obsessively check.

**Signal vs. Noise - Common Misreads**

**A 20% drop in traffic on a Monday** - Almost always a weekend pattern, not a problem. Compare week-over-week, not day-over-day.

**Sudden ranking jump for a new page** - Initial rankings often start high (Google testing new content), then settle lower over 2-4 weeks before stabilizing. Don't celebrate week-one results.

**Impressions up, clicks down** - Usually a SERP feature ate your traffic (featured snippet, AI overview, knowledge panel). Investigate the SERP for the affected query before assuming it's your fault.

**Traffic from a single keyword spiking** - Could be a news event, a viral mention, or seasonality. Check Google Trends for the term before drawing conclusions.

**Page indexed but no impressions** - Either no one searches for what you wrote, or you're ranking past page 5. Use GSC's URL Inspection tool to confirm the page is actually indexed.

**A core update happens and traffic shifts** - Wait 2-4 weeks for the update to fully roll out before reacting. Knee-jerk content changes during volatile periods often hurt more than help.

**When Numbers Don't Add Up**

GA4 and GSC will rarely show identical numbers, even for the same metric. This is normal:

- **GSC counts clicks** (someone clicked from a search result)
- **GA4 counts sessions** (someone arrived and triggered the tracking script)

Reasons they differ:

- Click happened but page failed to load (counts in GSC, not GA4)
- Browser blocks tracking (counts in GSC, not GA4)
- User clicks multiple results in one session (counts as multiple in GSC, one session in GA4)
- Bot traffic filtering differs between the two

A 10-20% discrepancy is normal. A 50%+ discrepancy means something is broken. Investigate tracking installation.

**Privacy & Compliance Notes**

Depending on your region and audience, you may need:

- **Cookie consent banner** - required in EU, UK, and increasingly elsewhere
- **Consent Mode v2** - required in EU for GA4 to function properly with consent
- **Privacy policy update** - disclose what data you collect and why
- **IP anonymization** - on by default in GA4

If you're operating in or serving the EU, configure Consent Mode v2 before assuming your data is reliable. Without it, you may be losing 30-50% of EU visitor data to consent rejections.

**Tooling Beyond The Free Stack**

Once the free stack is mature, paid tools add depth:

- **Ahrefs / Semrush** - competitor analysis, keyword research at scale, backlink monitoring
- **Screaming Frog** - full site crawls for technical audits (free up to 500 URLs)
- **Sitebulb** - visual site architecture mapping
- **Looker Studio (free)** - dashboards combining GSC + GA4 + other sources into one view
- **Rank tracking tools** (AccuRanker, Nightwatch, Wincher) - daily keyword position tracking GSC doesn't provide

None of these replace the free stack. They extend it.

**What "Working" Looks Like**

For a new site doing SEO right, expect roughly this pattern:

**Months 1-3:** Indexing builds, impressions slowly climb, clicks remain low. This is normal. Don't panic.

**Months 4-6:** First meaningful clicks arrive, often from long-tail queries you didn't specifically target. Average position improves on tracked terms.

**Months 7-12:** Compounding begins. Internal linking pays off. Pages start ranking for queries beyond their target keywords. Traffic graph starts curving upward visibly.

**Year 2+:** Established sites with consistent publishing and link building see traffic growth as a steady trend, with occasional jumps from breakthrough content or core update wins.

If you're still flat at month 9, something is structurally wrong. Audit using references/technical-audits.md and revisit references/content-strategy.md.

**Quick Setup Checklist**

Use this as a one-screen reference when setting up tracking on any new site:

- Google Search Console added (Domain property preferred)
- XML sitemap submitted in GSC
- GA4 property created with correct timezone/currency
- GA4 tracking code installed and verified in Real-time
- Google signals enabled
- Data retention extended to 14 months
- GSC linked to GA4
- Internal traffic filter configured
- Primary conversion identified and set up as key event
- Cookie consent / Consent Mode v2 configured if applicable
- Bing Webmaster Tools added (optional but quick)
- Looker Studio dashboard created (optional, for ongoing reporting)

When all boxes are checked, measurement is ready. Strategy and execution can now produce data instead of guesses.

**End of analytics-tracking.md**