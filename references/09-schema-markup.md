**File path:** seo-traffic-builder/references/schema-markup.md

**Schema Markup: Structured Data For Rich Results**

Schema markup is the part of SEO most site owners skip. It's invisible to readers, technically intimidating, and not a direct ranking factor - so it gets pushed to "someday."

This is a mistake. Schema markup is one of the highest-leverage technical SEO investments because it changes how your pages _appear_ in search results. The same #5 ranking with rich results often outclicks the #2 ranking without them. In a world where the click is what matters, schema markup is leverage.

This document covers what schema is, why it matters, which types matter most, and exactly how to implement them - with copy-paste-ready JSON-LD examples for each major type.

**What Schema Markup Actually Is**

Schema markup (also called structured data) is code added to a page that explicitly tells search engines what the content is about, in a standardized vocabulary they understand.

Without schema, Google has to _infer_ what your page is - is it an article? a product? a recipe? a book? Inference is good but imperfect.

With schema, you _tell_ Google explicitly: "This is a Book. Its title is X. Its author is Y. It belongs to category Z."

Google rewards this explicit clarity in two ways:

- **Better understanding of the page** (helping it rank for the right queries)
- **Rich results in search** - visual enhancements like star ratings, FAQ accordions, image carousels, recipe cards, breadcrumb trails, and dozens of other formats that make your result stand out from plain text listings.

Rich results dramatically increase click-through rate. Higher CTR means more traffic - and over time, higher rankings, because CTR is itself a ranking signal.

**The Vocabulary: Schema.org**

Schema.org is the open standard maintained by Google, Microsoft, Yahoo, and Yandex. It defines the vocabulary for marking up content. Every schema type and property in this document is part of Schema.org.

The full vocabulary is enormous (1000+ types), but the practical reality is: about 10-15 types cover 95% of useful cases. This document focuses on those.

**The Format: JSON-LD**

Schema can be implemented in three formats, but only one matters in 2026: **JSON-LD**.

JSON-LD is Google's recommended format. It's a script block placed in the &lt;head&gt; (or anywhere in the HTML) that contains structured data without affecting the page's visible content.

**Generic structure of any JSON-LD block:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "TypeName",

"propertyName": "propertyValue",

"anotherProperty": "anotherValue"

}

&lt;/script&gt;

The two other formats (Microdata, RDFa) embed schema directly in HTML elements. They work but are messier and harder to maintain. Use JSON-LD exclusively unless you have a specific legacy reason not to.

**Where to place JSON-LD on a page:**

- Ideal: in the &lt;head&gt; section
- Acceptable: anywhere in the &lt;body&gt;
- Multiple JSON-LD blocks per page are fine - each block describes one entity

**How To Test Your Schema**

Before relying on any schema, validate it.

**The two essential testing tools:**

**1\. Google's Rich Results Test** (search.google.com/test/rich-results)

Paste in a URL or code snippet. The tool tells you which rich results the page is eligible for, plus any errors or warnings. This is the most important schema tool - what it says, Google does.

**2\. Schema.org Validator** (validator.schema.org)

A more thorough validation against the full schema specification. Useful for catching property errors that Google's tool might not flag.

**Workflow for any new schema implementation:**

- Write the JSON-LD
- Test in Google's Rich Results Test
- Fix errors and warnings
- Deploy to the live page
- Re-test the live URL
- Monitor Google Search Console's "Enhancements" reports for indexing-time issues

Never deploy schema you haven't tested. A single typo can break the entire block.

**Priority Schema Types For Most Sites**

For most sites, these are the schema types worth implementing first, in priority order:

- **Organization** - sitewide, identifies the site/business as an entity
- **WebSite** - sitewide, enables sitelinks search box
- **BreadcrumbList** - every page below depth 1
- **Article** (or BlogPosting) - every blog post / informational article
- **FAQPage** - pages with FAQ sections
- **Product** - every product page (ecommerce)
- **Book** - every book listing page (your case)
- **HowTo** - every step-by-step tutorial
- **Review / AggregateRating** - review and rated content
- **LocalBusiness** - local-service businesses
- **VideoObject** - pages with embedded video content
- **Recipe** - every recipe page

Each is covered in detail below with copy-paste-ready examples.

**Schema Type 1: Organization**

**Purpose:** Identifies your site/business as a recognized entity. Provides Google with name, logo, social profiles, contact info - the data behind knowledge panels.

**Where to place:** Sitewide (typically homepage, but harmless on every page)

**Triggers:** Knowledge panel eligibility, brand recognition signals

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "Organization",

"name": "Team Success Network",

"alternateName": "TSN",

"url": "<https://www.teamsuccessnetwork.com>",

"logo": "<https://www.teamsuccessnetwork.com/logo.png>",

"description": "A free Christian library offering 200+ free books on faith, leadership, prayer, and spiritual growth.",

"sameAs": \[

"<https://www.facebook.com/teamsuccessnetwork>",

"<https://www.youtube.com/@teamsuccessnetwork>",

"<https://twitter.com/teamsuccessnetwork>"

\],

"contactPoint": {

"@type": "ContactPoint",

"contactType": "customer support",

"email": "<support@teamsuccessnetwork.com>"

}

}

&lt;/script&gt;

**Critical fields:**

- name - exactly as the brand is known
- url - canonical homepage URL
- logo - direct URL to your logo file (must be at least 112x112px)
- sameAs - array of all official social profiles (helps Google connect entity to known accounts)

**Schema Type 2: WebSite**

**Purpose:** Identifies the website as an entity, optionally enables a sitelinks search box for branded searches.

**Where to place:** Homepage (one instance per site)

**Triggers:** Sitelinks search box in branded SERPs

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "WebSite",

"name": "Team Success Network",

"url": "<https://www.teamsuccessnetwork.com>",

"potentialAction": {

"@type": "SearchAction",

"target": {

"@type": "EntryPoint",

"urlTemplate": "<https://www.teamsuccessnetwork.com/search?q={search_term_string}>"

},

"query-input": "required name=search_term_string"

}

}

&lt;/script&gt;

**The search box requirement:**

The potentialAction only triggers a sitelinks search box if your site actually has a search function reachable at the URL template specified. Make sure urlTemplate matches your real search URL pattern.

**Schema Type 3: BreadcrumbList**

**Purpose:** Tells Google the navigation path to the current page. Replaces the URL display in search results with a cleaner breadcrumb trail.

**Where to place:** Every page below depth 1 (where breadcrumbs exist)

**Triggers:** Breadcrumb display in search results (replacing or supplementing URL)

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "BreadcrumbList",

"itemListElement": \[

{

"@type": "ListItem",

"position": 1,

"name": "Home",

"item": "<https://www.teamsuccessnetwork.com>"

},

{

"@type": "ListItem",

"position": 2,

"name": "Books",

"item": "<https://www.teamsuccessnetwork.com/books>"

},

{

"@type": "ListItem",

"position": 3,

"name": "Christian Leadership",

"item": "<https://www.teamsuccessnetwork.com/books/leadership>"

},

{

"@type": "ListItem",

"position": 4,

"name": "Servant Leadership Reading List"

}

\]

}

&lt;/script&gt;

**Notes:**

- position numbers must be sequential starting from 1
- The final item (the current page) does not include an item URL - Google infers it from the page itself
- Breadcrumb names should match what's visible to users
- Match the visible breadcrumb HTML exactly - Google compares the two

**Schema Type 4: Article (and BlogPosting)**

**Purpose:** Marks blog posts and informational articles, enabling article-specific rich results and helping Google understand content type, author, and publish date.

**Where to place:** Every article, blog post, or news page

**Triggers:** Article rich results, news carousel inclusion, top stories eligibility, publish-date indication

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "Article",

"headline": "What Every New Christian Needs to Know About Spiritual Warfare",

"description": "A complete beginner's guide to understanding spiritual warfare - the weapons God provides, common attacks, and how to pray when under pressure.",

"image": \[

"<https://www.teamsuccessnetwork.com/images/spiritual-warfare-guide-1x1.jpg>",

"<https://www.teamsuccessnetwork.com/images/spiritual-warfare-guide-4x3.jpg>",

"<https://www.teamsuccessnetwork.com/images/spiritual-warfare-guide-16x9.jpg>"

\],

"datePublished": "2026-05-01T08:00:00-05:00",

"dateModified": "2026-05-05T10:30:00-05:00",

"author": {

"@type": "Person",

"name": "Author Name",

"url": "<https://www.teamsuccessnetwork.com/about-author>"

},

"publisher": {

"@type": "Organization",

"name": "Team Success Network",

"logo": {

"@type": "ImageObject",

"url": "<https://www.teamsuccessnetwork.com/logo.png>"

}

},

"mainEntityOfPage": {

"@type": "WebPage",

"@id": "<https://www.teamsuccessnetwork.com/spiritual-warfare-beginners-guide>"

}

}

&lt;/script&gt;

**Critical fields:**

- headline - should match the H1 (no longer than 110 characters)
- image - Google strongly prefers multiple aspect ratios (1:1, 4:3, 16:9) for best rich result display
- datePublished and dateModified - both in ISO 8601 format with timezone
- author - required, ideally as a Person with a profile URL
- publisher - required, with logo

**Article vs. BlogPosting:**

BlogPosting is a subtype of Article. For most blog content, BlogPosting is the more precise choice. For news, longer journalism, or pillar guides, Article is fine. Google treats them similarly.

**Schema Type 5: FAQPage**

**Purpose:** Marks Q&A sections on a page so Google can display them as expandable FAQ accordions in search results.

**Where to place:** Pages with genuine FAQ sections (or where you've intentionally structured content as Q&A)

**Triggers:** FAQ rich result (expandable Q&A directly in search results)

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "FAQPage",

"mainEntity": \[

{

"@type": "Question",

"name": "What is spiritual warfare?",

"acceptedAnswer": {

"@type": "Answer",

"text": "Spiritual warfare is the spiritual conflict described in scripture between believers and unseen spiritual forces. It involves prayer, scripture, and the armor of God, and is described most directly in Ephesians 6:10-18."

}

},

{

"@type": "Question",

"name": "How do I know if I'm under spiritual attack?",

"acceptedAnswer": {

"@type": "Answer",

"text": "Common signs include sudden waves of doubt, persistent intrusive thoughts contrary to scripture, sleep disruption around prayer or worship, and unusual conflict in close relationships. Discernment requires consistent prayer and scripture grounding."

}

},

{

"@type": "Question",

"name": "What is the armor of God?",

"acceptedAnswer": {

"@type": "Answer",

"text": "The armor of God is the metaphorical equipment Paul describes in Ephesians 6: the belt of truth, breastplate of righteousness, gospel of peace as shoes, shield of faith, helmet of salvation, and sword of the Spirit (the Word of God)."

}

}

\]

}

&lt;/script&gt;

**Important rules:**

- The FAQ content must be visible on the page - don't mark up content the user can't see
- Keep answers under 250 words for best rich result display
- Use plain text (no HTML markup inside the answer text)
- Make the questions and answers genuinely useful, not keyword-stuffed
- Don't mark up FAQs that promote a product as the answer (Google has cracked down on commercial FAQs)

**The 2026 reality:**

Google has reduced FAQ rich result displays significantly since 2023. They now show primarily for authoritative health, government, and educational sites. For other sites, FAQ schema still helps Google understand content but rarely produces visible rich results. Implement it anyway - the understanding signal is valuable, and rich results can return.

**Schema Type 6: Product**

**Purpose:** Marks ecommerce product pages with structured pricing, availability, ratings, and other commercial data.

**Where to place:** Every individual product page

**Triggers:** Product rich results (price, ratings, availability, shipping info in search results), Google Shopping eligibility

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "Product",

"name": "The Servant Leadership Workbook",

"description": "A 60-day workbook on Christian servant leadership, integrating biblical principles with practical leadership practices.",

"image": \[

"<https://www.teamsuccessnetwork.com/images/servant-leadership-workbook.jpg>"

\],

"brand": {

"@type": "Brand",

"name": "Team Success Network"

},

"sku": "TSN-SLW-001",

"offers": {

"@type": "Offer",

"url": "<https://www.teamsuccessnetwork.com/products/servant-leadership-workbook>",

"priceCurrency": "USD",

"price": "27.00",

"priceValidUntil": "2026-12-31",

"availability": "<https://schema.org/InStock>",

"itemCondition": "<https://schema.org/NewCondition>"

},

"aggregateRating": {

"@type": "AggregateRating",

"ratingValue": "4.8",

"reviewCount": "127"

}

}

&lt;/script&gt;

**Critical fields:**

- name - exact product name
- image - at least one high-quality image URL
- offers.price - the actual current price as a number, no currency symbol
- offers.priceCurrency - ISO 4217 currency code (USD, GBP, EUR, etc.)
- offers.availability - the appropriate Schema.org URL (InStock, OutOfStock, PreOrder, etc.)
- aggregateRating - only include if you have genuine ratings; fake ratings violate Google's policies

**Critical rule:** Schema must match the actual visible content. If your visible price is \$27 but schema says \$19, Google may penalize the page or remove it from rich results entirely.

**Schema Type 7: Book**

**Purpose:** Marks book pages with author, edition, format, and rating information. Especially valuable for content libraries and book retailers.

**Where to place:** Every individual book page

**Triggers:** Book rich results, knowledge panel inclusion for books, integration with Google Books results

**Template (for free book on your library):**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "Book",

"name": "Seeking God's Kingdom First: A 30-Day Journey",

"author": {

"@type": "Person",

"name": "Author Name"

},

"url": "<https://www.teamsuccessnetwork.com/books/seeking-gods-kingdom-first>",

"image": "<https://www.teamsuccessnetwork.com/images/seeking-gods-kingdom-cover.jpg>",

"bookFormat": "<https://schema.org/EBook>",

"inLanguage": "en",

"isbn": "",

"numberOfPages": 240,

"publisher": {

"@type": "Organization",

"name": "Team Success Network"

},

"datePublished": "2025-08-15",

"description": "A 30-day journey through scripture and prayer focused on Matthew 6:33 - seeking God's kingdom first in every area of life.",

"genre": "Christian Living",

"offers": {

"@type": "Offer",

"price": "0.00",

"priceCurrency": "USD",

"availability": "<https://schema.org/InStock>",

"url": "<https://www.teamsuccessnetwork.com/books/seeking-gods-kingdom-first>"

}

}

&lt;/script&gt;

**Special notes for free book libraries:**

- Set price to "0.00" - this is valid and signals free availability
- bookFormat should be EBook for HTML-readable books
- Include numberOfPages even for HTML books (use the equivalent print page count)
- genre helps Google categorize the book; use clear, recognized genre names
- If you don't have ISBNs (common for self-published or library content), omit the isbn field rather than leaving it empty

**Why this matters for your library:** With 200+ books, properly schema-marked book pages can produce dramatically more rich results visibility than competitor sites that only have plain text book listings. This is one of the highest-leverage moves available to a content library.

**Schema Type 8: HowTo**

**Purpose:** Marks step-by-step instructions so Google can display them as numbered step rich results.

**Where to place:** Tutorial, instructional, and how-to pages with clear sequential steps

**Triggers:** HowTo rich results (numbered step display in search results)

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "HowTo",

"name": "How to Build a Daily Prayer Routine",

"description": "A simple 5-step process to establish a sustainable daily prayer routine in 30 days.",

"totalTime": "PT15M",

"supply": \[

{

"@type": "HowToSupply",

"name": "Bible (any translation)"

},

{

"@type": "HowToSupply",

"name": "Notebook or journal"

}

\],

"step": \[

{

"@type": "HowToStep",

"name": "Choose a consistent time",

"text": "Pick a specific time of day you'll pray every day. Most people find early morning works best, but consistency matters more than the specific time.",

"url": "<https://www.teamsuccessnetwork.com/prayer-routine#step1>"

},

{

"@type": "HowToStep",

"name": "Choose a consistent place",

"text": "Identify a single physical space you'll always use for prayer. Same chair, same room, same corner. The location becomes a trigger for prayer mode.",

"url": "<https://www.teamsuccessnetwork.com/prayer-routine#step2>"

},

{

"@type": "HowToStep",

"name": "Start with scripture",

"text": "Begin every prayer session by reading 1-2 chapters of scripture, ideally a Psalm or section of the Gospels. Let the reading shape what you pray about.",

"url": "<https://www.teamsuccessnetwork.com/prayer-routine#step3>"

},

{

"@type": "HowToStep",

"name": "Use the ACTS framework",

"text": "Pray in four phases: Adoration (worship God for who He is), Confession (acknowledge sin), Thanksgiving (express gratitude), and Supplication (request needs).",

"url": "<https://www.teamsuccessnetwork.com/prayer-routine#step4>"

},

{

"@type": "HowToStep",

"name": "Journal what you hear",

"text": "End each session by writing 1-2 sentences about what God seemed to be saying, any verses that struck you, or any conviction you felt. This builds a record of growth over time.",

"url": "<https://www.teamsuccessnetwork.com/prayer-routine#step5>"

}

\]

}

&lt;/script&gt;

**Notes:**

- totalTime uses ISO 8601 duration format (PT15M = 15 minutes)
- Each step should have a name and text; URLs are optional but help with deep-linking
- The step content must match what's visible on the page
- Google has reduced HowTo rich result displays since 2023 (similar to FAQ), but the schema still helps page understanding

**Schema Type 9: Review and AggregateRating**

**Purpose:** Marks review content and rating data, enabling star ratings to appear in search results.

**Where to place:** Pages that feature genuine reviews - products, services, books, courses, recipes

**Triggers:** Star rating display in search results (one of the highest CTR boosts available)

**Single review template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "Review",

"itemReviewed": {

"@type": "Book",

"name": "Seeking God's Kingdom First: A 30-Day Journey"

},

"reviewRating": {

"@type": "Rating",

"ratingValue": "5",

"bestRating": "5"

},

"author": {

"@type": "Person",

"name": "Reader Name"

},

"reviewBody": "This book transformed my morning prayer time within the first week. The daily structure is exactly what I needed - biblical, practical, and challenging without being overwhelming."

}

&lt;/script&gt;

**Aggregate rating (multiple reviews summarized) - usually embedded inside a Product or Book schema rather than standalone:**

json

"aggregateRating": {

"@type": "AggregateRating",

"ratingValue": "4.8",

"reviewCount": "127",

"bestRating": "5"

}

**Critical compliance rules:**

- Reviews must be from real people, displayed publicly on the page
- Self-reviews (the business reviewing itself) violate Google's guidelines
- Don't mark up reviews that don't exist on the page
- Don't include only positive reviews while hiding negative ones from the schema
- The visible content must include the review information being marked up

Google has aggressively cracked down on fake/manipulated review schema. Use it honestly or not at all.

**Schema Type 10: LocalBusiness**

**Purpose:** Identifies a physical or service business with a specific location. Critical for local SEO.

**Where to place:** Homepage of local business sites; potentially location-specific landing pages

**Triggers:** Knowledge panel inclusion, Google Business Profile cross-validation, local pack visibility

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "LocalBusiness",

"name": "Example Business Name",

"image": "<https://www.example.com/storefront.jpg>",

"@id": "<https://www.example.com>",

"url": "<https://www.example.com>",

"telephone": "+1-555-555-1234",

"priceRange": "\$\$",

"address": {

"@type": "PostalAddress",

"streetAddress": "123 Main Street",

"addressLocality": "City Name",

"addressRegion": "ST",

"postalCode": "12345",

"addressCountry": "US"

},

"geo": {

"@type": "GeoCoordinates",

"latitude": 40.7128,

"longitude": -74.0060

},

"openingHoursSpecification": \[

{

"@type": "OpeningHoursSpecification",

"dayOfWeek": \["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"\],

"opens": "09:00",

"closes": "17:00"

},

{

"@type": "OpeningHoursSpecification",

"dayOfWeek": "Saturday",

"opens": "10:00",

"closes": "14:00"

}

\],

"sameAs": \[

"<https://www.facebook.com/examplebusiness>",

"<https://www.instagram.com/examplebusiness>"

\]

}

&lt;/script&gt;

**For specific business types**, use more specific subtypes when available:

- Restaurant (with servesCuisine, acceptsReservations)
- MedicalBusiness, Dentist, Physician
- LegalService, Attorney
- Plumber, Electrician, HVACBusiness
- Store, ClothingStore, BookStore
- Hotel, LodgingBusiness

The more specific the subtype, the better Google understands the business.

**Schema Type 11: VideoObject**

**Purpose:** Marks pages with embedded video content, enabling video carousel inclusion and video rich results.

**Where to place:** Any page with primary video content (YouTube embed, self-hosted video, video tutorials)

**Triggers:** Video rich results, key moments display, video carousel inclusion

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "VideoObject",

"name": "How to Build a Daily Prayer Routine in 5 Steps",

"description": "A 12-minute walkthrough of a simple framework for establishing a sustainable daily prayer practice, including time, place, and structure.",

"thumbnailUrl": "<https://www.teamsuccessnetwork.com/images/prayer-routine-thumbnail.jpg>",

"uploadDate": "2026-04-22T08:00:00-05:00",

"duration": "PT12M30S",

"contentUrl": "<https://www.teamsuccessnetwork.com/videos/prayer-routine.mp4>",

"embedUrl": "<https://www.youtube.com/embed/VIDEO_ID>",

"publisher": {

"@type": "Organization",

"name": "Team Success Network",

"logo": {

"@type": "ImageObject",

"url": "<https://www.teamsuccessnetwork.com/logo.png>"

}

}

}

&lt;/script&gt;

**Notes:**

- duration uses ISO 8601 (PT12M30S = 12 minutes 30 seconds)
- For YouTube embeds, use the YouTube embed URL in embedUrl
- Include thumbnailUrl - required for rich result display
- Google can also pull video schema from YouTube directly when you embed; explicit schema helps but isn't always required

**Schema Type 12: Recipe**

**Purpose:** Marks recipe content with ingredients, cooking time, ratings, and instructions.

**Where to place:** Every recipe page

**Triggers:** Recipe rich results (image carousel, ratings, cooking time, calorie info - one of the most visually distinctive rich results)

**Template:**

html

&lt;script type="application/ld+json"&gt;

{

"@context": "<https://schema.org>",

"@type": "Recipe",

"name": "Classic Sourdough Bread",

"image": \[

"<https://www.example.com/sourdough-1x1.jpg>",

"<https://www.example.com/sourdough-4x3.jpg>",

"<https://www.example.com/sourdough-16x9.jpg>"

\],

"author": {

"@type": "Person",

"name": "Chef Name"

},

"datePublished": "2026-04-15",

"description": "A traditional sourdough bread recipe using only flour, water, salt, and active starter.",

"prepTime": "PT30M",

"cookTime": "PT45M",

"totalTime": "PT24H",

"recipeYield": "1 loaf",

"recipeCategory": "Bread",

"recipeCuisine": "European",

"nutrition": {

"@type": "NutritionInformation",

"calories": "180 calories"

},

"recipeIngredient": \[

"500g bread flour",

"350g water",

"100g active sourdough starter",

"10g salt"

\],

"recipeInstructions": \[

{

"@type": "HowToStep",

"text": "Mix flour and water; rest for 30 minutes (autolyse)."

},

{

"@type": "HowToStep",

"text": "Add starter and salt; mix until combined."

},

{

"@type": "HowToStep",

"text": "Bulk ferment for 4-6 hours with stretches every 30 minutes."

}

\],

"aggregateRating": {

"@type": "AggregateRating",

"ratingValue": "4.9",

"reviewCount": "238"

}

}

&lt;/script&gt;

Recipe is one of the most rich-result-friendly schema types - implementing it well dramatically increases CTR for any recipe site.

**Combining Schema Types On A Single Page**

A single page can (and often should) use multiple schema types. They don't conflict - each describes a different aspect of the page.

**Example: A blog post page might include:**

- BlogPosting schema for the article itself
- BreadcrumbList schema for the navigation path
- FAQPage schema if it includes a Q&A section
- Organization schema (or rely on a sitewide implementation)

These are deployed as separate JSON-LD blocks, each in its own &lt;script&gt; tag.

**Example: A book page might include:**

- Book schema for the book itself
- BreadcrumbList schema
- Review or AggregateRating if user ratings exist

**Implementation By CMS**

**WordPress:**

The easiest path is a plugin:

- **Yoast SEO** - handles Article, BlogPosting, BreadcrumbList, Organization, WebSite automatically; FAQ blocks supported in editor
- **Rank Math** - comparable to Yoast, includes more schema types in free version (Product, Recipe, HowTo, Course, etc.)
- **Schema Pro** (paid) - comprehensive schema management with deeper customization

For custom schema beyond what plugins handle, use a code snippets plugin or insert directly into theme files.

**Shopify:**

- Built-in schema is decent for Product schema; third-party apps like Schema App or Schema Plus extend coverage
- Custom code can be added through the theme code editor

**Webflow / Squarespace / Wix:**

- Most builders allow custom code injection in page settings
- Add JSON-LD to the &lt;head&gt; section of each page
- Some templates may need theme-level schema added by developers

**Custom HTML/PHP sites:**

- Direct JSON-LD insertion into templates
- Use server-side templating to dynamically populate values from your database
- This is your situation for the Team Success Network site - JSON-LD blocks generated dynamically per book and per article from your existing data

**Common Schema Mistakes To Avoid**

**Mistake 1: Marking up content that isn't visible on the page.**

Schema must reflect what users actually see. Hidden FAQs, fake reviews, unrelated content marked up to game results - all violate guidelines and can trigger penalties.

**Mistake 2: Using schema as a ranking shortcut.**

Schema doesn't directly improve rankings. It improves CTR via rich results, which indirectly helps. Sites that "stuff" schema hoping for ranking gains see no benefit and risk penalties for misleading markup.

**Mistake 3: Inconsistent data between schema and visible content.**

If your visible price is \$47 but schema says \$97, Google removes the rich result and may penalize the page.

**Mistake 4: Self-reviews and rating manipulation.**

Marking up your own glowing review of your own product violates guidelines. Use only genuine, third-party-supplied reviews. AggregateRating must reflect real review counts.

**Mistake 5: Not testing.**

Untested schema with a single broken character can disable the entire block. Always test with Google's Rich Results Test before deploying.

**Mistake 6: Ignoring required fields.**

Every schema type has required fields for rich result eligibility. Missing one means the block validates as schema but doesn't trigger any rich result.

**Mistake 7: Using outdated schema types.**

Schema.org evolves. Older properties get deprecated. Check the current Google documentation for required and recommended properties when implementing.

**Mistake 8: One sitewide schema only.**

A single Organization schema on the homepage is good. But every blog post needs its own Article schema, every product needs its own Product schema, and so on. Sitewide schema doesn't replace per-page schema.

**Monitoring Schema In Search Console**

After deploying schema, monitor it in Google Search Console:

**Search Console → Enhancements** shows reports for each schema type Google recognizes:

- Articles
- Products
- FAQ
- HowTo
- Reviews
- Breadcrumbs
- Recipes
- (and others as deployed)

Each report shows:

- Total pages with that schema
- Pages with errors (won't trigger rich results)
- Pages with warnings (will trigger but missing optional improvements)
- Valid pages (full rich result eligibility)

**The discipline:** Check these reports monthly. Errors block rich results entirely; warnings reduce them. Both are fixable.

**A Final Word On Schema**

Schema markup is the most underused leverage in SEO. Most sites either skip it entirely or deploy only the basics (Article, BreadcrumbList) and stop. The sites that go further - implementing Book, FAQ, Review, HowTo, and other relevant types deliberately - get rich results their competitors don't, which means higher CTR, which means more traffic, which means stronger rankings over time.

For your situation specifically - a content library with 200+ books and 30+ category pages - proper Book schema across the entire library is potentially the single highest-impact SEO move available. It makes every book page eligible for visual rich results that text-only competitors can't match. Combined with BreadcrumbList for category navigation and Article for blog content, you'd be operating at a structural data sophistication level that dwarfs typical Christian content sites.

The implementation is mechanical - once you have the templates above, generating them dynamically from your book database is straightforward PHP. The work pays back for years.

Don't skip schema. Don't half-implement it. Deploy it deliberately, test it rigorously, monitor it consistently. Then watch as your search results visually outclass everyone else competing for the same queries.

That's the leverage. Take it.

**End of schema-markup.md**