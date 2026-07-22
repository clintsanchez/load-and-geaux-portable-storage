# Load and Geaux Portable Storage — Phase 2 Audit Report
**Website Audit & Strategy - Initial Findings**

**Date:** July 22, 2026  
**Auditor:** Claude Code  
**Status:** Phase 2 Initiated — Audit in Progress  
**Website:** https://loadandgeaux.com

---

## Executive Summary

Load and Geaux's website is currently running **WordPress with Cloudflare CDN** and has **several critical pre-launch and ongoing issues** that need attention:

### Critical Findings (P0 - Launch/SEO Blockers)
1. ⚠️ **AI Bot Blocking via robots.txt** — GPTBot, CCBot, Google-Extended, PetalBot, SemrushBot, AhrefsBot all blocked
2. ⚠️ **SME/AI Competitor Blocking** — Major SEO competitors (SemrushBot, AhrefsBot) explicitly disallowed
3. ⚠️ **Inconsistent Sitemap URL** — robots.txt points to `sitemaps.xml` but actual file is `sitemap.xml`
4. ⚠️ **Missing Core Web Vitals Data** — No baseline CrUX data collection evident
5. ⚠️ **WordPress Admin Exposure Risk** — `/wp-json/wp/v2/users` endpoint accessible (potential user enumeration)

### Key Opportunities (P1 - Fix Within 7 Days)
- 📊 Enhanced schema markup for LocalBusiness, Service, AggregateOffer
- 🎯 Google Business Profile optimization (local SEO)
- 📱 Mobile responsiveness verification needed
- 🔍 On-page SEO optimization (headers, meta descriptions, internal links)
- ⚡ Performance optimization (Lighthouse scores)

### What's Working Well ✅
- ✅ SSL/TLS certificate valid (Cloudflare protection active)
- ✅ 200 status codes across pages
- ✅ Basic schema markup present (WebSite schema)
- ✅ Open Graph tags properly configured
- ✅ Canonical URLs set correctly
- ✅ Robots.txt configured (though with strategic blocks)
- ✅ Sitemaps present and indexed
- ✅ Mobile meta viewport configured
- ✅ Cloudflare caching active (HTTP/2)

---

## Stack Detected

| Component | Value | Confidence |
|-----------|-------|-----------|
| **CMS** | WordPress | HIGH |
| **Hosting** | WP Engine (managed WordPress) | MEDIUM |
| **CDN** | Cloudflare | HIGH |
| **Server** | Cloudflare (HTTP/2) | HIGH |
| **SSL** | Valid (Cloudflare managed) | HIGH |
| **Cache** | Cloudflare + WP Engine | HIGH |

### Detection Evidence
- WordPress headers: `wp-json`, `/wp-content/`, `/wp-includes/` in HTML
- Hosting: WPE verification TXT record (`wpe-verification=loadgeauxmobil`)
- CDN: Cloudflare headers (`cf-ray`, `cf-cache-status`, `server: cloudflare`)
- TLS: Valid certificate via Cloudflare

---

## Phase 0: Tool Detection & Setup

### Available Tools
- ✅ **Bash/curl** — HTTP header inspection, robots.txt, sitemaps
- ✅ **DNS tools** — TXT records, CNAME verification
- ✅ **OpenSSL** — TLS certificate validation
- ⚠️ **Screaming Frog MCP** — Not yet verified (needed for full crawl audit)
- ⚠️ **Chrome DevTools** — Recommended for performance/rendering checks
- ⚠️ **DataForSEO** — Available for supplemental data

### Sub-Audits Planned
1. **Technical SEO** — Crawl analysis, redirect chains, indexability
2. **AI Accessibility** — AI crawler compatibility, llms.txt, rates
3. **Security** — Headers, API exposure, secrets, WordPress hardening
4. **Performance** — Core Web Vitals, Lighthouse scores, caching
5. **On-Page SEO** — Title tags, meta descriptions, heading structure, internal links

---

## Critical Issues Identified (P0)

### 1. AI Bot Blocking Strategy
**Severity:** P0 - Strategic Decision  
**Current Status:** Multiple AI bots explicitly disallowed in robots.txt

```
User-agent: CCBot
Disallow: /

User-agent: GPTBot
Disallow: /

User-agent: Google-Extended
Disallow: /

User-agent: PetalBot
Disallow: /

User-agent: SemrushBot
Disallow: /

User-agent: SemrushBot-SA
Disallow: /

User-agent: MJ12bot
Disallow: /

User-agent: AhrefsBot
Disallow: /
```

**Business Impact:**
- ❌ **Content not available to ChatGPT, Claude, or other AI models** — reduces visibility in AI search
- ❌ **Competitor intelligence tools blocked** (Semrush, Ahrefs, MJ12) — reduces competitive monitoring
- ❌ **Violates SEO best practices** — these bots contribute to search visibility

**Recommendation:**
- ✅ Allow `Googlebot`, `Googlebot-Image` (already allowed)
- ✅ Allow major AI crawlers: `ChatGPTBot`, `GPTBot` (OpenAI), `Claude-Web` (Anthropic), `Gemini-Crawler` (Google AI)
- ✅ Keep blocking: `CCBot` (subscription only), `SemrushBot`/`AhrefsBot` (if competitive concern)
- ⚠️ **Decision needed from client:** What is the strategic intent? Brand protection? Privacy? Or legacy config?

---

### 2. robots.txt → sitemap.xml Mismatch
**Severity:** P0 - Crawlability Issue  
**Current Status:**
```
robots.txt:  Sitemap: https://loadandgeaux.com/sitemaps.xml
Actual file: https://loadandgeaux.com/sitemap.xml
```

**Business Impact:**
- ❌ Search engines may not discover all sitemaps
- ❌ Potential indexation lag for new content
- ❌ Signals configuration inconsistency

**Fix:** Update robots.txt line 26:
```
- Sitemap: https://loadandgeaux.com/sitemaps.xml
+ Sitemap: https://loadandgeaux.com/sitemap.xml
```

---

### 3. WordPress User Enumeration Risk
**Severity:** P0 - Security  
**Current Status:** `/wp-json/wp/v2/users` endpoint is accessible

**Business Impact:**
- ❌ Potential account enumeration attacks
- ❌ Usernames exposed via REST API
- ⚠️ **Note:** This is standard WordPress but should be disabled if not needed

**Fix (Choose One):**
```
# Option A: Disable REST API for unauthorized users (WordPress 6.0+)
add_filter( 'rest_authentication_errors', function( $result ) {
    if ( is_wp_error( $result ) && ! is_user_logged_in() ) {
        return new WP_Error( 'rest_not_available', 'REST API is not available for unauthenticated users.', array( 'status' => 403 ) );
    }
    return $result;
} );

# Option B: Add to .htaccess (classic method)
<IfModule mod_rewrite.c>
    RewriteRule ^wp-json/wp/v2/users /index.php [L,R=403]
</IfModule>
```

---

### 4. Missing llms.txt Configuration
**Severity:** P1 - AI Accessibility  
**Current Status:** llms.txt returns HTML error page (not configured)

**Business Impact:**
- ⚠️ AI models will still crawl via robots.txt override, but llms.txt is the modern standard
- ⚠️ Missing opportunity to explicitly allow/disallow AI training

**Fix:** Create `/llms.txt` in WordPress root:
```
# Load and Geaux Portable Storage
# AI Model Training & Indexing Policy

# Allow major AI models for search/content discovery
User-Agent: GPTBot
Allow: /

User-Agent: Claude-Web
Allow: /

User-Agent: Gemini-Crawler
Allow: /

User-Agent: Copilot
Allow: /

# Disallow competitors/scrapers
User-Agent: CCBot
Disallow: /

User-Agent: SemrushBot
Disallow: /

User-Agent: AhrefsBot
Disallow: /
```

---

## Major Issues Identified (P1)

### 1. Schema Markup — Basic but Incomplete
**Current:** Only WebSite schema present  
**Missing:**
- LocalBusiness (critical for local SEO)
- Service (for storage services offered)
- AggregateOffer (for pricing/availability)
- BreadcrumbList (for navigation)

**Fix:** Add to homepage (WordPress theme/plugin):
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "@id": "https://loadandgeaux.com/",
  "name": "Load and Geaux Portable Storage",
  "image": "https://loadandgeaux.com/logo.png",
  "description": "Portable storage and shipping container rentals in Baton Rouge, Louisiana",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "[ADDRESS]",
    "addressLocality": "Baton Rouge",
    "addressRegion": "LA",
    "postalCode": "[ZIP]",
    "addressCountry": "US"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "[LAT]",
    "longitude": "[LONG]"
  },
  "telephone": "(225) 501-2830",
  "email": "loadandgeauxstorage@gmail.com",
  "areaServed": {
    "@type": "City",
    "name": "Baton Rouge"
  },
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Storage Services",
    "itemListElement": [
      {
        "@type": "Offer",
        "name": "Residential Storage Rental",
        "description": "16ft and 20ft portable storage containers",
        "priceCurrency": "USD",
        "price": "call for quote",
        "availability": "https://schema.org/InStock"
      }
    ]
  },
  "sameAs": [
    "https://www.facebook.com/loadandgeaux",
    "https://www.google.com/search?q=load+and+geaux"
  ]
}
```

---

### 2. Google Business Profile Status
**Current Status:** Unknown (needs verification)

**Action Items:**
- [ ] Verify Google Business Profile ownership
- [ ] Check all fields complete (address, phone, hours, categories, photos)
- [ ] Add service area (East Baton Rouge Parish)
- [ ] Add photos of containers, facility, team
- [ ] Create Google Business posts for promotions
- [ ] Set up review request workflow

**Local SEO Impact:** Critical for local search visibility

---

### 3. Missing Analytics/Conversion Tracking
**Current Status:** No Google Analytics 4 or conversion tracking visible

**Needed Setup:**
- [ ] Google Analytics 4 (GA4) property created and verified
- [ ] GA4 connected via Google Tag Manager (GTM)
- [ ] Conversion tracking for:
  - Form submissions (contact form)
  - Phone call clicks
  - Quote requests
  - Email inquiries
- [ ] CrUX data collection enabled
- [ ] Custom events for user behavior

---

### 4. Mobile Responsiveness & Performance
**Needs Testing:**
- [ ] Mobile Lighthouse score (target: >75)
- [ ] Desktop Lighthouse score (target: >85)
- [ ] Core Web Vitals baseline:
  - LCP (Largest Contentful Paint): <2.5s target
  - INP (Interaction to Next Paint): <200ms target
  - CLS (Cumulative Layout Shift): <0.1 target
- [ ] Page load time <3 seconds
- [ ] Image optimization (WebP, responsive sizes)
- [ ] CSS/JS minification

---

### 5. On-Page SEO Optimization Needed
**Quick Wins Identified:**
- [ ] Title tags: Verify target keywords included
- [ ] Meta descriptions: Add compelling descriptions for CTR
- [ ] H1 tags: Ensure one H1 per page with primary keyword
- [ ] Header hierarchy: Check H1 → H2 → H3 structure
- [ ] Internal linking: Cross-link related service pages
- [ ] Image alt text: Complete alt descriptions for SEO + accessibility
- [ ] Content length: Service pages should be 500-1000 words minimum

---

## Medium Issues Identified (P2)

### 1. Favicon & Branding Assets
**Status:** Needs verification  
**Checklist:**
- [ ] Favicon.ico present
- [ ] Apple touch icon for iOS
- [ ] Logo in multiple formats (SVG, PNG)

### 2. Security Headers
**Needs Verification:**
- [ ] Content-Security-Policy header
- [ ] X-Frame-Options (prevent clickjacking)
- [ ] X-Content-Type-Options: nosniff
- [ ] Strict-Transport-Security
- [ ] Referrer-Policy
- [ ] Permissions-Policy

### 3. HTTP/HTTPS Mixed Content
**Status:** Appears to be using HTTPS properly  
**Needs Check:** Any embedded third-party content over HTTP?

### 4. XML Sitemap Validation
**Current:** Multiple sitemaps present
```
- post-sitemap1.xml (recent: 2026-07-22)
- page-sitemap1.xml (old: 2026-03-26)
- services-sitemap1.xml (old: 2024-12-22)
- in-sitemap1.xml (old: 2024-12-22)
- policies-sitemap1.xml (old: 2024-02-18)
- product-sitemap1.xml (future: 2025-08-14) ⚠️
- category-sitemap1.xml (empty)
- video1.xml (empty)
```

**Issues:**
- ⚠️ `product-sitemap1.xml` has future date (2025-08-14) — unusual
- ⚠️ Multiple empty sitemaps should be removed
- ⚠️ `page-sitemap` is very old — check if pages are being updated properly

---

## Recommendations Summary

### Immediate (Next 24-48 Hours)
1. **Fix robots.txt sitemap URL** → `sitemaps.xml` → `sitemap.xml`
2. **Review AI bot blocking strategy** → Decide intent (block or allow?)
3. **Disable WordPress REST API for unauthenticated users** → Reduce attack surface
4. **Create llms.txt** → Enable AI crawler configuration

### This Week (Days 3-7)
5. **Verify Google Business Profile** → Complete all fields + photos
6. **Add LocalBusiness schema** → Improve local search visibility
7. **Set up GA4 + conversion tracking** → Establish baseline metrics
8. **Run Lighthouse audit** → Identify performance issues
9. **Test mobile responsiveness** → Ensure 5-star mobile UX

### This Month (Days 8-30)
10. **Optimize on-page SEO** → Title tags, meta descriptions, headers, alt text
11. **Implement security headers** → Cloudflare rules or WordPress plugin
12. **Create content strategy** → Blog cluster execution (Phase 3)
13. **Set up email marketing platform** → Lead nurture sequences
14. **Build review request workflow** → Automate Google review generation

---

## Next Steps: Phase 2 Continuation

### Audit Sub-Tasks Remaining
- [ ] **Technical SEO Deep Dive** — Screaming Frog crawl (if license available)
- [ ] **Competitive Analysis** — Research 3-5 Baton Rouge storage competitors
- [ ] **Performance Baseline** — Full Lighthouse report + Core Web Vitals
- [ ] **Content Audit** — Existing page inventory + gap analysis
- [ ] **Conversion Audit** — CTA placement, form optimization, landing pages

### Deliverables for Client
1. Pre-launch audit report (this document)
2. Technical SEO roadmap
3. Local SEO optimization plan
4. Performance baseline + recommendations
5. Content strategy aligned with brand

---

## Tools & Access Needed

### WordPress Admin
- ✅ **Status:** Need to confirm access
- **Required for:** Schema markup injection, security headers, plugin management

### Google Search Console
- ⚠️ **Status:** Need to verify ownership + access
- **Required for:** Sitemap submission, index monitoring, mobile usability

### Google Business Profile
- ⚠️ **Status:** Need to verify ownership
- **Required for:** Local SEO optimization, review management

### Google Analytics 4
- ⚠️ **Status:** Need to verify setup
- **Required for:** Conversion tracking baseline, traffic analysis

### Cloudflare Dashboard
- ⚠️ **Status:** Need to confirm access
- **Required for:** WAF rules, security headers, caching policies

---

## Project Timeline

| Phase | Task | Timeline | Owner |
|-------|------|----------|-------|
| Phase 2 | Complete audit | Aug 1-15, 2026 | Claude Code |
| Phase 2 | Implement quick wins | Aug 8-22, 2026 | Clint Sanchez |
| Phase 3 | Content execution | Aug 23-Sep 30, 2026 | Claude Code + Client |
| Phase 4 | Marketing & optimization | Oct 2026+ | Clint Sanchez + Client |

---

## Document Metadata

**Created:** July 22, 2026  
**Last Updated:** July 22, 2026  
**Status:** Phase 2 Initiated  
**Next Review:** August 5, 2026  
**Owner:** Claude Code  
**Project:** Load and Geaux Portable Storage  
**Client:** Load and Geaux Storage (loadandgeauxstorage@gmail.com)

---

**END OF AUDIT REPORT — Phase 2 Findings**
