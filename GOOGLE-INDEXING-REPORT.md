# Google Search Indexing Report
## salamivf.com - April 2026

---

## Executive Summary

Your **new Hugo website is NOT appearing in Google search** because Google is still indexing your **old WordPress website**. This is a site migration issue, not a technical problem with the new site itself.

---

## Current Situation

### What Google Currently Shows

When searching `site:salamivf.com`, Google returns results from **the OLD website**:

| Page | URL (OLD WordPress Structure) |
|------|------------------------------|
| Our Lab | www.salamivf.com/our-lab/ |
| Doctors | www.salamivf.com/doctors/ |
| Gynecology | www.salamivf.com/gynecology/ |
| Contact Us | www.salamivf.com/contactus/ |
| Articles | www.salamivf.com/articles/ |

### Your NEW Website Structure

Your new Hugo site uses a completely different URL structure:

| Page | URL (NEW Hugo Structure) |
|------|--------------------------|
| Homepage EN | salamivf.com/en/ |
| Homepage AR | salamivf.com/ar/ |
| Services | salamivf.com/en/docs/fertility-services/ |
| About | salamivf.com/en/about/ |
| Contact | salamivf.com/en/contact/ |

**Google doesn't know these new URLs exist yet.**

---

## Root Causes Identified

### 1. Site Migration Without Proper SEO Handoff
- The old WordPress site was at `www.salamivf.com`
- The new Hugo site is at `salamivf.com` (no www)
- Google treats www and non-www as **different websites**
- No redirects from old URLs to new URLs

### 2. Robots.txt Missing Sitemap Reference
**Current robots.txt:**
```
User-agent: *

```

**Should be:**
```
User-agent: *
Allow: /

Sitemap: https://salamivf.com/sitemap.xml
```

The sitemap reference helps Google discover all your pages quickly.

### 3. Google Search Console Not Configured
- Sitemap likely not submitted to Google Search Console
- No request for Google to re-crawl the site
- No verification that Google can access the new site

### 4. No 301 Redirects From Old URLs
Old WordPress URLs like `/our-lab/` should redirect to new Hugo equivalents, but they currently don't exist or return 404.

---

## Technical Audit Results

### What's Working
| Check | Status | Notes |
|-------|--------|-------|
| Sitemap.xml | Working | Properly formatted at /sitemap.xml |
| Site Accessible | Working | Both /en/ and /ar/ load correctly |
| HTTPS | Working | SSL certificate valid |
| Canonical Tags | Working | Implemented via head-end.html |
| Hreflang Tags | Working | EN/AR language alternates present |
| Schema.org | Working | MedicalBusiness structured data |
| Meta Pixel | Working | Facebook tracking active |
| GTM/Analytics | Working | Google Tag Manager configured |

### What Needs Fixing
| Issue | Priority | Impact |
|-------|----------|--------|
| No sitemap in robots.txt | HIGH | Google may not find all pages |
| No Google Search Console | HIGH | No way to request indexing |
| No 301 redirects | HIGH | Old URLs return 404, losing SEO value |
| www redirect missing | MEDIUM | Duplicate content risk |

---

## Action Plan

### IMMEDIATE ACTIONS (Do Today)

#### 1. Fix robots.txt
Create a custom robots.txt template:

**File: `layouts/robots.txt`**
```
User-agent: *
Allow: /

Sitemap: {{ .Site.BaseURL }}sitemap.xml
```

#### 2. Set Up Google Search Console
1. Go to https://search.google.com/search-console
2. Add property: `salamivf.com` (use Domain verification)
3. Verify ownership via DNS TXT record
4. Submit sitemap: `https://salamivf.com/sitemap.xml`
5. Request indexing for homepage

#### 3. Configure www to non-www Redirect
Add to `netlify.toml`:
```toml
[[redirects]]
  from = "https://www.salamivf.com/*"
  to = "https://salamivf.com/:splat"
  status = 301
  force = true
```

### SHORT-TERM ACTIONS (This Week)

#### 4. Create 301 Redirects for Old URLs
Add redirect mappings for important old pages:

```toml
# In netlify.toml
[[redirects]]
  from = "/our-lab/"
  to = "/en/about/"
  status = 301

[[redirects]]
  from = "/doctors/"
  to = "/en/about/"
  status = 301

[[redirects]]
  from = "/contactus/"
  to = "/en/contact/"
  status = 301

[[redirects]]
  from = "/about/"
  to = "/en/about/"
  status = 301

[[redirects]]
  from = "/gynecology/"
  to = "/en/docs/benign-gynaecology/"
  status = 301

[[redirects]]
  from = "/insemination-2/"
  to = "/en/docs/fertility-services/"
  status = 301
```

#### 5. Request Indexing via Search Console
After setup, use "Request Indexing" for these priority pages:
- `/en/` (English homepage)
- `/ar/` (Arabic homepage)
- `/en/docs/fertility-services/`
- `/en/about/`
- `/en/contact/`

### MEDIUM-TERM ACTIONS (Next 2-4 Weeks)

#### 6. Monitor Coverage Report
Check Google Search Console weekly for:
- Index coverage issues
- Crawl errors
- Mobile usability problems

#### 7. Build Backlinks to New URLs
- Update social media profile links
- Contact directories to update listings
- Update Google Business Profile URL

---

## Expected Timeline

| Milestone | Expected Time |
|-----------|---------------|
| Robots.txt fix deployed | Day 1 |
| Search Console verified | Day 1-2 |
| Sitemap submitted | Day 2 |
| First pages indexed | 3-7 days |
| Majority of pages indexed | 2-4 weeks |
| Full indexing recovery | 4-8 weeks |

---

## Why This Happened

When migrating a website:
1. **URL structure changed** - Google sees /en/about/ as completely different from /about/
2. **Domain variant changed** - www.salamivf.com vs salamivf.com are different to Google
3. **No migration signals sent** - Without 301 redirects and Search Console, Google has no reason to re-crawl
4. **Time factor** - Even with perfect setup, Google takes time to discover and index new sites

---

## Key Takeaway

**Your new website is technically sound for SEO.** The issue is purely a migration problem - Google doesn't know the old site has been replaced. The fixes above will resolve this within 4-8 weeks.

---

*Report generated: April 24, 2026*
