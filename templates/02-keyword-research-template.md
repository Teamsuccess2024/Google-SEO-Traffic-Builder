**File path:** seo-traffic-builder/templates/keyword-research-template.md

**Keyword Research Template**

**Why This Template Exists**

Keyword research is only useful if it's organized. A list of 200 keywords in someone's notes app is not a keyword strategy - it's a graveyard. This template gives keyword research a consistent structure that makes it actionable: every keyword has a target page, a priority, and a path from research to ranking.

This template works whether Claude is populating it for a user, a user is filling it in themselves, or a team is collaborating on it. The structure is the same. The discipline of using it is what produces results.

**How To Use This Template**

The template is designed for a spreadsheet (Google Sheets, Excel, Airtable). Each row is one keyword. Each column captures one attribute of that keyword.

Three ways to use it:

- **Claude populates it** - based on intake and research, Claude produces a populated keyword sheet the user can copy into a spreadsheet
- **User fills it** - using free tools (Google Keyword Planner, Search Console, AnswerThePublic) or paid tools (Ahrefs, Semrush)
- **Hybrid** - Claude provides the seed keyword list and structure; the user fills in volume and difficulty data from their preferred tools

Whichever approach is used, the column structure stays consistent.

**The Column Structure**

The full template has 15 columns. Not every column needs data immediately - some are filled during research, some during planning, some during ongoing tracking. The structure accommodates the entire lifecycle.

**Column 1: Keyword**

The exact search phrase, in lowercase, as a user would type it.

Examples:

- "what does the bible say about suffering"
- "free christian books on servant leadership"
- "books like zig ziglar for christians"

Rules:

- One keyword per row, no comma-separated lists
- Use the actual phrasing - don't auto-correct grammar that real searches contain
- Long-tail variations get their own rows even if related to a head term

**Column 2: Search Volume**

Estimated monthly searches in the target country/language.

Sources:

- Google Keyword Planner (free with Google Ads account, gives ranges)
- Ahrefs / Semrush / Mangools (paid, gives specific numbers)
- Google Search Console (for keywords already getting impressions)

Rules:

- Use a single source consistently - don't mix tools, since estimates vary
- For very low-volume long-tail terms, use "<10" or "10-100" if exact data isn't available
- Volume is a guide, not a target - long-tail keywords with low volume often convert better than head terms

**Column 3: Keyword Difficulty (KD)**

How hard it is to rank in the top 10 for this keyword. Most tools score 0-100.

Rough thresholds:

- 0-20: Easy - new sites can compete
- 21-40: Moderate - possible with good content and some authority
- 41-60: Difficult - requires established site or significant link building
- 61-80: Very difficult - dominated by major sites
- 81-100: Effectively unattainable for most sites

Rules:

- Use one tool's scoring consistently
- For sites under 6 months old, focus primarily on KD under 30
- For established sites, KD up to 50 is realistic
- Beyond 60, only attempt if you have strong existing authority on the topic

**Column 4: Search Intent**

What the searcher actually wants. Four primary categories:

- **Informational** - wants to learn or understand ("what is grace," "how to read the bible")
- **Navigational** - looking for a specific site or brand ("team success network," "billy graham website")
- **Commercial** - researching before a purchase decision ("best christian books on prayer," "niv vs esv comparison")
- **Transactional** - ready to take action ("buy christian devotional," "download free christian ebook")

Rules:

- Pick the dominant intent, not all that might apply
- When unclear, search the keyword on Google and look at what's currently ranking - the SERP reveals intent
- Mismatched intent is the #1 cause of content that ranks but doesn't convert

**Column 5: Topic Cluster**

Which content cluster or theme this keyword belongs to. Groups related keywords for strategic content planning.

Examples for a Christian library:

- "Suffering and Hardship"
- "Servant Leadership"
- "Christian Sales / Ziglar"
- "Identity in Christ"
- "Spiritual Warfare"
- "Reading Recommendations"

Rules:

- Define your clusters before populating the sheet (typically 5-15 for a content site)
- Every keyword belongs to exactly one cluster
- Clusters become the structural backbone of your content strategy
- See references/content-strategy.md for cluster planning

**Column 6: Funnel Stage**

Where in the audience journey this keyword fits.

- **Top of Funnel (TOFU)** - broad awareness, problem identification
- **Middle of Funnel (MOFU)** - comparing options, building knowledge
- **Bottom of Funnel (BOFU)** - ready to take action, looking for the right specific solution

Examples:

- "what does the bible say about leadership" - TOFU (problem awareness)
- "best christian books on servant leadership" - MOFU (evaluating options)
- "download seek first the kingdom free pdf" - BOFU (specific action)

Rules:

- A balanced strategy includes content for all three stages
- BOFU keywords convert highest but have lower volume
- TOFU keywords have highest volume but require strong conversion paths to be valuable
- Most sites overweight TOFU and underweight BOFU; correcting this often dramatically improves results

**Column 7: Target Page**

The specific URL or planned URL that will rank for this keyword. One page should target one primary keyword (plus related variations).

Format:

- Existing page: full URL ("teamsuccessnetwork.com/books/seek-first-kingdom")
- New page to create: planned slug ("/blog/what-does-it-mean-to-seek-gods-kingdom-first")
- TBD: placeholder ("TBD - new pillar page on suffering")

Rules:

- Never assign the same target page to multiple primary keywords (causes cannibalization)
- Group related long-tail keywords under the same target page if they share intent
- New target pages get added to the content calendar before any optimization work begins

**Column 8: Existing Rank**

Where the target page currently ranks for this keyword (if anywhere).

Sources:

- Google Search Console (for pages already earning impressions)
- Manual incognito searches (for spot checks)
- Rank tracking tools (Ahrefs, Semrush, AccuRanker) for systematic tracking

Format:

- "1-10" if on page 1
- "11-20" if on page 2 (highest-priority optimization candidates)
- "21-50" if on page 3+
- "50+" if effectively invisible
- "Not ranking" if no impressions
- "N/A" for keywords with no target page yet

Rules:

- Update this column monthly
- Page 2 keywords (positions 11-20) are the highest-leverage optimization targets - small improvements often produce large traffic gains

**Column 9: Priority**

How important this keyword is to your strategy. Three levels:

- **High** - top 20% of keywords; aligned with primary conversion, achievable difficulty, strong intent match
- **Medium** - secondary keywords that support clusters or capture additional intent
- **Low** - opportunistic targets, may pursue if easy, won't drive strategy

Rules:

- Resist the temptation to mark everything High
- High-priority keywords get content created first, optimization attention first, link building first
- Low-priority keywords may sit in the sheet for a year before action; that's fine

**Column 10: Status**

Where this keyword is in the workflow.

- **Researched** - added to sheet, not yet acted on
- **Brief Created** - content brief written
- **Content In Progress** - drafting underway
- **Published** - content is live
- **Optimizing** - published, currently being improved
- **Ranking** - earning meaningful traffic
- **Stalled** - published but not ranking; needs reassessment
- **Retired** - no longer pursuing

Rules:

- Update status as work progresses
- Filter by status to see what needs attention
- "Stalled" pages need diagnostic - content quality, intent match, or link gaps

**Column 11: Date Targeted**

When work on this keyword began (brief created or content started).

Format: YYYY-MM-DD

Rules:

- Helps track time-to-rank patterns over time
- Useful for understanding how long content takes to mature for your specific site

**Column 12: Date Published**

When the target content went live.

Format: YYYY-MM-DD

Rules:

- Most content takes 3-6 months to reach stable ranking
- Don't expect ranking before this date plus 3 months as a baseline

**Column 13: Notes**

Free-form context that doesn't fit other columns.

Examples:

- "SERP has strong featured snippet - target snippet capture"
- "Competitor X dominates with 5,000-word pillar; need to outdo"
- "Personal story angle from author available"
- "AI Overview present - informational queries showing reduced clicks"
- "Seasonal - peaks in November"

Rules:

- Use sparingly; every note should drive future action
- Most rows won't have notes; that's fine

**Column 14: Link to Brief**

URL to the content brief document for this keyword (if created).

Format: Full URL to Google Doc, Notion page, or wherever briefs live

Rules:

- Provides direct path from keyword sheet to actual content production
- Empty until brief is created

**Column 15: Conversion Path**

What action this keyword's target page is meant to drive.

Examples:

- "Email signup via mid-article opt-in"
- "Book recommendation links to library"
- "Direct CTA to free book download"
- "Internal linking to commercial pillar"

Rules:

- Every keyword that gets content needs a conversion path
- "None" or empty conversion paths produce vanity traffic
- The conversion path determines content structure, not just SEO

**Sample Populated Row**

To make the structure concrete, here's a single row fully populated:

| **Column**&nbsp; &nbsp; &nbsp; | **Value**&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| --------------- | ------------------------------------------------------------------------------------------------------- |
| Keyword&nbsp; &nbsp; &nbsp; &nbsp;  | what does it mean to seek gods kingdom first&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| Search Volume&nbsp;  | 1,300&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| KD&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | 22&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| Intent&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Informational&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| Topic Cluster&nbsp;  | Kingdom-Seeking&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| Funnel Stage&nbsp; &nbsp; | TOFU&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| Target Page&nbsp; &nbsp;  | /blog/seek-gods-kingdom-first-meaning&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| Existing Rank&nbsp;  | Not ranking&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| Priority&nbsp; &nbsp; &nbsp; &nbsp; | High&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| Status&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | Brief Created&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| Date Targeted&nbsp;  | 2026-05-12&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| Date Published&nbsp; | (blank - pending)&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |
| Notes&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  | Featured snippet opportunity. Pillar page for kingdom cluster. Connects to existing book on this topic. |
| Link to Brief&nbsp;  | docs.google.com/\[brief-link\]&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; |
| Conversion Path | Internal link to free book + email opt-in for Kingdom reading guide&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  |

A populated sheet with 50-200 rows like this becomes the operating manual for an entire content strategy.

**Sheet Setup Instructions**

For users creating this in a spreadsheet from scratch:

**Initial Setup**

- Open Google Sheets, Excel, or your preferred spreadsheet tool
- Create columns A through O matching the 15 columns above
- Freeze row 1 (header row) so it stays visible while scrolling
- Apply data validation to columns where applicable:
&nbsp; - Intent column: dropdown with the four intent types
&nbsp; - Funnel Stage column: dropdown with TOFU/MOFU/BOFU
&nbsp; - Priority column: dropdown with High/Medium/Low
&nbsp; - Status column: dropdown with the workflow statuses

**Filtering and Views**

Create saved filter views for:

- **High Priority Active** - Priority = High AND Status ≠ Retired
- **Page 2 Opportunities** - Existing Rank = "11-20" (highest-leverage optimization)
- **Stalled Content** - Status = Stalled (needs intervention)
- **By Cluster** - group by Topic Cluster to see content density per theme
- **By Funnel Stage** - verify balance across TOFU/MOFU/BOFU

**Conditional Formatting**

Useful highlights:

- Green for keywords currently ranking 1-10
- Yellow for page 2 (positions 11-20) - opportunity zone
- Red for Status = Stalled
- Bold for Priority = High

**Frequency of Updates**

- **Weekly** - update Status column as content moves through workflow
- **Monthly** - update Existing Rank from Search Console data
- **Quarterly** - full review; retire keywords that aren't working, add new opportunities discovered

**How Claude Uses This Template**

When Claude populates the template for a user, the workflow is:

- **Pull from intake** - review user's audience, business model, and goals from templates/intake-questionnaire.md
- **Reference cluster planning** - use clusters defined in content strategy work
- **Generate seed keywords** - produce 30-60 starting keywords across clusters
- **Tag intent and funnel stage** - every keyword gets categorized
- **Suggest target pages** - either existing URLs or planned URLs
- **Set initial priority** - based on alignment with primary conversion and likely difficulty
- **Leave research data blank** - search volume and KD require user's tools or paid access
- **Mark status as "Researched"** - initial state for all rows
- **Add notes** - for keywords with specific opportunities or risks worth flagging

The deliverable is a structured starting point the user fills in with research data and acts on systematically.

**Common Mistakes To Avoid**

**Targeting only head terms** - keyword sheets dominated by high-volume, high-difficulty terms produce no rankings. Long-tail balance is required.

**Ignoring intent** - populating volume and difficulty without matching intent produces content that ranks for the wrong searches.

**Assigning the same target page to multiple primary keywords** - causes cannibalization. One page = one primary keyword (plus related variations).

**No conversion path on TOFU keywords** - pulls in traffic that doesn't convert. Every TOFU page needs a path to MOFU/BOFU content or direct conversion.

**Letting the sheet go stale** - research that isn't acted on is wasted. Status updates and rank checks must happen on schedule.

**Pursuing too many clusters at once** - spreading effort thin produces shallow coverage in many areas instead of authority in a few. Most sites should focus on 3-5 clusters initially.

**Treating the sheet as the strategy** - the sheet is the organizing structure, not the strategy itself. Strategy lives in references/content-strategy.md and the cluster decisions made there.

**Final Principle**

A keyword research sheet is a working document, not a one-time deliverable. The sites that get the most from keyword research are the ones that maintain the sheet for years - adding, updating, retiring, and learning from what worked. A sheet built carefully and used consistently is one of the highest-leverage assets in an SEO operation.

Do not let it sit. Use it weekly. Update it monthly. Review it quarterly. The compounding pays off.

**End of keyword-research-template.md**