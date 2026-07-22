# Phase 2 Action Items — Website Audit & Strategy
**Load and Geaux Portable Storage**

**Status:** Phase 2 Initiated  
**Date:** July 22, 2026  
**Next Review:** August 5, 2026

---

## Quick Summary

✅ **Stack detected:** WordPress + WP Engine + Cloudflare  
✅ **Website status:** Live and functioning, but needs optimization  
🔴 **Critical issues found:** 4 P0 issues + 5 P1 issues requiring attention  
📊 **Audit report:** See `docs/AUDIT-PHASE-2-REPORT.md`

---

## Priority 1: CRITICAL (Fix Next 24-48 Hours)

### 1. Fix robots.txt Sitemap URL
- **File:** WordPress root robots.txt
- **Change:** Line 26 `Sitemap: https://loadandgeaux.com/sitemaps.xml` → `sitemap.xml`
- **Status:** ⏳ Pending
- **Assigned to:** Clint (WordPress admin access)

### 2. Review AI Bot Blocking Strategy
- **Question:** Why are GPTBot, Google-Extended, AhrefsBot, SemrushBot blocked?
- **Options:**
  - A) Allow all (maximize visibility in AI/SEO tools)
  - B) Allow Google but block competitors (balanced approach)
  - C) Keep current (privacy-first approach)
- **Status:** ⏳ Awaiting client decision
- **Assigned to:** Client consultation required

### 3. Disable WordPress User Enumeration
- **Risk:** `/wp-json/wp/v2/users` endpoint exposes usernames
- **Fix:** Add REST API restriction via WordPress plugin or .htaccess
- **Status:** ⏳ Pending
- **Assigned to:** Clint (WordPress admin access)

### 4. Create llms.txt Configuration
- **File:** `/llms.txt` in WordPress root
- **Purpose:** Enable AI crawler configuration (modern standard)
- **Template:** Provided in audit report
- **Status:** ⏳ Pending
- **Assigned to:** Clint (WordPress admin access)

---

## Priority 2: HIGH (Fix Within 7 Days)

### 5. Google Business Profile Optimization
- [ ] Verify GBP ownership
- [ ] Complete all profile fields (address, hours, categories)
- [ ] Add service area (East Baton Rouge Parish + zip codes)
- [ ] Upload 10+ photos (containers, facility, team, vehicles)
- [ ] Create 2-3 GBP posts with promotions/updates
- [ ] Set up review request workflow
- **Status:** ⏳ Needs GBP access
- **Assigned to:** Clint or Client

### 6. Add LocalBusiness Schema Markup
- **Location:** Homepage (and all key pages)
- **Add:** LocalBusiness, Service, AggregateOffer schemas
- **Template:** Provided in audit report
- **Status:** ⏳ Pending
- **Assigned to:** Clint (WordPress plugin or theme injection)

### 7. Set Up Google Analytics 4
- [ ] Create GA4 property (if not exists)
- [ ] Connect via Google Tag Manager
- [ ] Add conversion tracking (form submissions, calls, quotes)
- [ ] Enable CrUX data collection
- [ ] Create custom events for user behavior
- **Status:** ⏳ Needs access
- **Assigned to:** Clint

### 8. Run Lighthouse Performance Audit
- [ ] Mobile score (target: >75)
- [ ] Desktop score (target: >85)
- [ ] Identify performance bottlenecks
- [ ] Create optimization plan
- **Status:** ⏳ Pending
- **Tool:** Lighthouse (browser) or DataForSEO API

### 9. Test Mobile Responsiveness
- [ ] iPhone test
- [ ] Android test
- [ ] Tablet test
- [ ] Identify layout issues
- **Status:** ⏳ Pending

---

## Priority 3: MEDIUM (Complete Within 2 Weeks)

### 10. On-Page SEO Optimization
- [ ] Audit and update title tags (add target keywords)
- [ ] Write/improve meta descriptions (add CTAs)
- [ ] Verify H1 tags (one per page, with primary keyword)
- [ ] Check header hierarchy (H1 → H2 → H3)
- [ ] Add/improve alt text on all images
- [ ] Expand service page content (500-1000 words minimum)
- [ ] Create internal linking strategy
- **Assigned to:** Claude (content optimization)

### 11. Security Headers Audit
- [ ] Verify CSP (Content-Security-Policy)
- [ ] Check X-Frame-Options
- [ ] Verify X-Content-Type-Options: nosniff
- [ ] Check HSTS header
- [ ] Review Referrer-Policy
- [ ] Check Permissions-Policy
- **Status:** ⏳ Needs Cloudflare/WordPress config review
- **Assigned to:** Clint

### 12. XML Sitemap Cleanup
- [ ] Remove empty sitemaps (category-sitemap1.xml, video1.xml)
- [ ] Fix future-dated product-sitemap
- [ ] Update old pages sitemap (from March 2026)
- [ ] Verify all active content is included
- **Status:** ⏳ Pending
- **Assigned to:** Clint (WordPress SEO plugin)

### 13. Competitive Analysis (3-5 Competitors)
- [ ] Identify top local competitors (Baton Rouge storage)
- [ ] Analyze their messaging and positioning
- [ ] Document content gaps we can fill
- [ ] Note pricing transparency and CTAs
- [ ] Create competitive positioning strategy
- **Status:** ⏳ Pending
- **Assigned to:** Claude (research agent)

---

## Priority 4: ONGOING (Phase 2 + Phase 3)

### Blog Content Strategy
- [ ] Finalize 4 blog clusters (from BACKLOG.md)
- [ ] Create content calendar (3+ months)
- [ ] Write cluster 1: Container Types & Selection (3 articles)
- [ ] Write cluster 2: Sustainability & Innovation (3 articles)
- [ ] Write cluster 3: Local Authority (3 articles)
- [ ] Write cluster 4: Success Stories & Case Studies (3 articles)
- **Assigned to:** Claude (content writing)

### Email Marketing Setup
- [ ] Select email platform (MailChimp, ConvertKit, etc.)
- [ ] Create welcome sequence (3-5 emails)
- [ ] Create nurture sequence for leads
- [ ] Set up automated follow-ups
- **Assigned to:** Clint

### Social Media Planning
- [ ] Create 3-month content calendar
- [ ] Design social media templates
- [ ] Set up posting schedule (3x/week minimum)
- [ ] Create hashtag strategy
- **Assigned to:** Claude or Clint

---

## Access & Permissions Needed

### WordPress Admin
- ⏳ **Status:** Need to confirm
- **Required for:**
  - Editing robots.txt and llms.txt
  - Schema markup injection
  - Plugin management
  - Performance optimization

### Google Search Console
- ⏳ **Status:** Need to verify ownership
- **Required for:**
  - Sitemap submission
  - Index monitoring
  - Mobile usability report

### Google Business Profile
- ⏳ **Status:** Need to verify ownership
- **Required for:**
  - Local SEO optimization
  - Review management
  - Photos and posts

### Google Analytics 4
- ⏳ **Status:** Need to verify setup
- **Required for:**
  - Conversion tracking baseline
  - Traffic analysis

### Cloudflare Dashboard
- ⏳ **Status:** Need to confirm access
- **Required for:**
  - Security headers configuration
  - WAF rules
  - Caching policies

---

## Success Metrics for Phase 2

| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|
| Website Status | 200 OK | 200 OK (maintained) | Aug 1 |
| Technical SEO Score | TBD | >85/100 | Aug 15 |
| Lighthouse (Mobile) | TBD | >75 | Aug 15 |
| Lighthouse (Desktop) | TBD | >85 | Aug 15 |
| Google Index Count | TBD | +20% | Aug 30 |
| GBP Completion | <50% | 100% | Aug 15 |
| Schema Coverage | 10% | 90% | Aug 15 |
| Analytics Setup | Not started | Full GA4 + conversions | Aug 15 |

---

## Weekly Checklist

### Week 1 (July 22-28)
- [ ] Complete all P0 fixes (robots.txt, llms.txt, user enum, bot decision)
- [ ] Verify access to WordPress, GSC, GBP, GA4, Cloudflare
- [ ] Begin competitive analysis
- [ ] Start GBP optimization

### Week 2 (July 29 - Aug 4)
- [ ] Complete GBP optimization
- [ ] Add LocalBusiness schema
- [ ] Set up GA4 + conversion tracking
- [ ] Run Lighthouse audit
- [ ] Complete competitive analysis

### Week 3 (Aug 5-11)
- [ ] Review audit findings with client
- [ ] Optimize on-page SEO (titles, descriptions, headers)
- [ ] Complete security headers configuration
- [ ] Test mobile responsiveness

### Week 4 (Aug 12-18)
- [ ] Clean up XML sitemaps
- [ ] Implement performance optimizations
- [ ] Final audit review and sign-off
- [ ] Transition to Phase 3 (content execution)

---

## Phase 2 Deliverables (Expected by Aug 30)

1. ✅ Complete pre-launch audit report (AUDIT-PHASE-2-REPORT.md)
2. ⏳ Technical SEO roadmap with specific fixes
3. ⏳ Local SEO optimization plan
4. ⏳ Performance baseline and recommendations
5. ⏳ Content audit and gap analysis
6. ⏳ Competitive positioning strategy
7. ⏳ Phase 3 content strategy (blog clusters, keywords, timeline)

---

## Contact & Escalation

**Client:** loadandgeauxstorage@gmail.com | (225) 501-2830  
**Project Manager:** Clint Sanchez (clint@clintsanchez.com)  
**Auditor:** Claude Code  

**If blocked on:**
- WordPress access → Contact Clint
- GBP access → Contact Client
- GA4 setup → Contact Clint
- Design decisions → Contact Client via Clint

---

## Document Metadata

**Created:** July 22, 2026  
**Status:** Phase 2 In Progress  
**Next Update:** July 29, 2026  
**Owner:** Claude Code + Clint Sanchez  
**Project:** Load and Geaux Portable Storage

---

**For detailed findings, see: `docs/AUDIT-PHASE-2-REPORT.md`**
