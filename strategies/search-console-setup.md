# Search Console Setup (in the autopilot agent)

Status: playbook is in the agent. Actual GSC property creation is a browser sign-in step and runs on Rony's go — it is NOT claimed as done here.

## Sites to cover (Blogger, all owned via Google accounts already in use)
- amazondealshub4u.blogspot.com (Deals)
- ursmov13.blogspot.com (YoursMovie)
- reply2rony.blogspot.com (Rony portfolio)
- gramaus.blogspot.com (GRAMAUS)
- banglahub96.blogspot.com (Bangla Hub — search data only, never social)
- tinytalestv4kids.blogspot.com (Tiny Tales — search data only, excluded from social automation)

## Setup steps (per site, in order)
1. Google Search Console > Add property > URL prefix > enter the blogspot URL.
2. Verification: Blogger sites verify via the Google account that owns the blog (no HTML file upload needed on Blogspot) — sign in with the owning account in the browser, confirm ownership in GSC.
3. Sitemaps > Add sitemap: `sitemap.xml` (Blogger serves this automatically; also `sitemap-pages.xml` for pages).
4. Coverage check: confirm no "submitted URL not found" errors from custom-permalink posts; fix any post whose permalink fell back to blog-post_N (do not submit fallback URLs that pins/Shorts do not link to).
5. Performance baseline: record impressions, clicks, avg position, top queries into the KPI log (~/workspace/social-growth/kpi-log.md) — Week 0 baseline first, then weekly.
6. Ongoing (agent, weekly): pull GSC impressions + avg position + top queries per site, feed them into topic picking (queries that rank page 2 = refresh candidates: new pin design + price/date check, not a rewrite) and into the algorithm-extraction review.

## SEO rules the agent enforces on every blog post (BLOG SEO RULE)
Search description <150 chars, custom permalink (never publish at a fallback URL when pins/Shorts already link to the custom one), h1/h2/h3 structure, alt text on images, 3-5 internal links per post, affiliate disclaimer on every Deals post.
