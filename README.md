[My Actor](https://apify.com/iblead/my-actor?fpr=data)

# Google Maps Business Database -- 50M+ Leads with Emails

Search 50M+ businesses across 38 countries. Get instant results with full contact information: emails, phone numbers, 6 social media profiles, GPS coordinates, opening hours, and more. Results in seconds, not hours.

## What data do you get?

| Field | Description |
| --- | --- |
| `name` | Business name |
| `address` | Full street address |
| `city` | City name |
| `postal_code` | ZIP / postal code |
| `country_code` | ISO country code (US, FR, DE, etc.) |
| `phone` | Phone number from Google Maps listing |
| `website_url` | Business website |
| `google_maps_url` | Direct Google Maps link |
| `place_id` | Google Place ID |
| `cid` | Google CID |
| `category` | Primary Google Maps category |
| `categories` | All categories (array) |
| `business_description` | Business description from Google |
| `rating` | Google rating (1.0 - 5.0) |
| `review_count` | Number of Google reviews |
| `latitude` | GPS latitude |
| `longitude` | GPS longitude |
| `business_status` | Open, temporarily closed, permanently closed |
| `claimed` | Whether the business owner claimed the listing |
| `photo_url` | Main photo URL |
| `hours` | Opening hours (structured) |
| `timezone` | Business timezone |
| `emails` | Email addresses found on the business website (array) |
| `phones_from_website` | Phone numbers extracted from the website (array) |
| `facebook` | Facebook page URL |
| `instagram` | Instagram profile URL |
| `linkedin` | LinkedIn page URL |
| `twitter` | Twitter/X profile URL |
| `tiktok` | TikTok profile URL |
| `youtube` | YouTube channel URL |
| `confidence_score` | Email/phone extraction confidence score |
| `technologies` | Detected technologies by category (object) |
| `first_seen_at` | When the business was first indexed |
| `last_seen_at` | Last time the business data was refreshed |

## Use cases

- **Cold outreach and lead generation**: Search businesses by category and city, filter by "has email", and export ready-to-use prospect lists.
- **Local SEO audits**: Pull all businesses in a category and city to analyze ratings, review counts, and claimed status across competitors.
- **Market sizing**: Count how many businesses of a given type exist in a country, city, or postal code area.
- **Sales territory mapping**: Export businesses with GPS coordinates for geographic territory planning.
- **Social media prospecting**: Filter businesses by social media presence (Facebook, Instagram, LinkedIn, Twitter/X, YouTube) for targeted outreach.
- **Competitive analysis**: Compare ratings, review counts, and online presence across businesses in the same category.

## How to use

1. Get a free API key at [app.iblead.com](https://app.iblead.com) (200 free credits on signup, no credit card required).
2. Open this actor in Apify Console.
3. Select a **country** (required) -- 38 countries available, from US (18M businesses) to Iceland (28K).
4. Pick a **category** (macro grouping like "Restaurant") or a **subcategory** (exact Google Maps category like "Italian Restaurant"). You can also leave both empty to search all businesses.
5. Optionally add a **city** name and/or **postal code** to narrow results geographically.
6. Apply filters: has email, has phone, has website, minimum rating, minimum reviews, social media presence.
7. Set **max results** (default 1,000) and run.

Results appear in your Apify dataset within seconds.

## Input parameters

| Parameter | Required | Type | Description |
| --- | --- | --- | --- |
| `country` | Yes | String | Country code. 38 countries available. |
| `category` | No | String | Broad category (29 options: Restaurant, Health & Medical, etc.) |
| `subcategory` | No | String | Exact Google Maps category (4,037 options: Italian Restaurant, Dentist, etc.) |
| `city` | No | String | City name. Comma-separated for multiple (e.g. "New York,Los Angeles"). |
| `postal_code` | No | String | ZIP/postal code. Supports prefixes: "75" matches all Paris codes. |
| `has_email` | No | Boolean | Only businesses with an email address. |
| `has_phone` | No | Boolean | Only businesses with a phone number. |
| `has_website` | No | Boolean | Only businesses with a website. |
| `has_facebook` | No | Boolean | Only businesses with a Facebook page. |
| `has_instagram` | No | Boolean | Only businesses with an Instagram profile. |
| `has_linkedin` | No | Boolean | Only businesses with a LinkedIn page. |
| `has_twitter` | No | Boolean | Only businesses with a Twitter/X profile. |
| `has_youtube` | No | Boolean | Only businesses with a YouTube channel. |
| `min_rating` | No | Number | Minimum Google rating (1.0 - 5.0). |
| `min_reviews` | No | Integer | Minimum number of Google reviews. |
| `max_results` | No | Integer | Maximum businesses to return. Default: 1,000. Max: 100,000. |
| `api_key` | Yes | String | Your IBLead API key. |

## Pricing

This actor charges **$3.50 per 1,000 results**.

| Actor | Price per 1K | Emails | Social profiles | Coverage | Speed |
| --- | --- | --- | --- | --- | --- |
| **IBLead (this actor)** | **$3.50** | Yes | 6 platforms | 50M+ | Instant |
| Compass Google Maps | $4 - $5 | Limited | No | Smaller | Live scraping (slow) |
| Miso Google Maps | ~$3 | Partial | Partial | 9M | Live scraping (slow) |

Key differences: This actor returns results in seconds, while alternatives take minutes to hours for large datasets and are subject to rate limits. IBLead covers 50M+ businesses across 38 countries -- over 5x more than the next largest competitor on Apify.

## FAQ

**How is this different from a Google Maps scraper?**
Traditional scrapers extract data page by page in real-time. This is slow (minutes to hours for large queries) and breaks when Google changes their page structure. This actor returns results in seconds from continuously refreshed data. Same data, faster and more reliably.

**Where do the email addresses come from?**
Emails are extracted by crawling the business websites listed on Google Maps. We visit the website, scan the pages for email addresses, and store them. This is the same data you would find by visiting each website manually.

**How often is the data updated?**
Data is continuously refreshed. Each business is re-scanned on a regular cycle. The `last_seen_at` field in each record tells you when that specific business was last updated.

**Can I search all businesses in a country without a category filter?**
Yes. Leave both category and subcategory empty, set your country, and adjust max_results. Be aware that some countries have millions of businesses -- set a reasonable limit or use filters to narrow results.

**What does "200 free credits" mean?**
When you sign up at app.iblead.com, you get 200 credits to test the API at no cost, no credit card required. One credit = one business result. After that, you pay per result through the Apify platform pricing.

## About IBLead

IBLead covers 50M+ businesses across 38 countries and 4,037 Google Maps categories. The data includes contact information extracted from business websites (emails, phone numbers), 6 social media profiles (Facebook, Instagram, LinkedIn, Twitter/X, TikTok, YouTube), GPS coordinates, opening hours, ratings, and review counts. Data is refreshed continuously -- no manual scraping required on your end. Sign up at [app.iblead.com](https://app.iblead.com) for 200 free credits.