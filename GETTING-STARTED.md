# Getting Started — Load and Geaux Portable Storage

A quick reference guide to jump into this project.

---

## 1. First Time Setup (5 minutes)

### Read These Files (in order)
```
1. CLAUDE.md (project context and workflow)
2. 00-Client-Brief.md (who is this client?)
3. brand-style-guide.md (how do we talk about them?)
4. BACKLOG.md (what are we building?)
```

### Check Out the Assets
```bash
# View available logos
ls brand/logos/

# See what infographics we have
ls assets/graphics/infographics/

# Check customer testimonials
ls assets/graphics/reviews/ | head -20

# Browse photography
ls assets/photography/
```

### Explore the Strategy
```bash
# Read the blog cluster strategy
open docs/load-and-geaux-blog-cluster-strategy.xlsx

# Review customer feedback
open docs/load-geaux-google-reviews\ \(GOOD\).xlsx

# Check brand strategy
open docs/Load\ and\ Geaux\ —\ Comprehensive\ Brand\ Strategy.docx
```

---

## 2. Project Structure at a Glance

```
Load and Geaux Portable Storage/
│
├── CLAUDE.md                          ← START HERE (project instructions)
├── 00-CLIENT-BRIEF.md                 ← Client overview & deliverables
├── brand-style-guide.md               ← Brand voice & visual standards
├── BACKLOG.md                         ← Work items & timeline
├── README.md                          ← Project summary
├── ONBOARDING-SUMMARY.md              ← What's been done (this file)
│
├── brand/
│   ├── logos/                         ← 30+ logo variations
│   ├── load---geaux-portable-storage-brand-guide.html
│   └── load---geaux-portable-storage_brand_guide.pdf
│
├── docs/
│   ├── Load and Geaux Brand Information Document.docx
│   ├── Load and Geaux — Comprehensive Brand Strategy.docx
│   ├── Business Research Report.docx
│   ├── load-and-geaux-blog-cluster-strategy.xlsx
│   ├── load-geaux-google-reviews (GOOD).xlsx
│   ├── facts-about-shipping-containers.csv
│   └── [more strategy & research files]
│
├── assets/
│   ├── photography/                   ← 50+ product & lifestyle photos
│   ├── graphics/
│   │   ├── infographics/             ← 12+ data visualizations
│   │   └── reviews/                  ← 40+ customer testimonial cards
│
├── blog/
│   ├── clusters/                      ← Organized by blog cluster topic
│   ├── drafts/                        ← In-progress articles
│   └── published/                     ← Live articles
│
├── website/                           ← Website code (to be set up)
├── marketing/                         ← Campaigns, templates
├── seo/                               ← Keyword research, optimization
├── social/                            ← Social media content
└── memory/                            ← Project memory & context
```

---

## 3. Quick Facts About the Client

**Load and Geaux Portable Storage**
- **Type:** Portable storage & shipping container rentals/sales
- **Location:** Baton Rouge, Louisiana
- **Contact:** loadandgeauxstorage@gmail.com | (225) 501-2830
- **Primary Market:** Residential + Commercial (B2C + B2B)
- **Brand Voice:** Friendly + Professional + Locally Rooted

**Brand Colors:**
- Forest Green: #2D5016 (primary)
- Louisiana State Green: #004D40 (accent)
- White: #FFFFFF (background)

**Key Services:**
- Portable storage containers
- Climate-controlled storage
- Shipping container rentals & sales

---

## 4. What's Already Done ✅

### Documentation (All Ready)
- ✅ Complete client brief and business overview
- ✅ Comprehensive brand strategy and positioning
- ✅ Detailed brand style guide with tone examples
- ✅ Blog content cluster strategy (4 clusters, 10+ articles planned)
- ✅ Market research and competitive analysis
- ✅ Customer feedback and testimonial data

### Assets (All Organized)
- ✅ 30+ logo variations (SVG, PNG at multiple scales)
- ✅ 50+ photography files (products, lifestyle, branded)
- ✅ 12+ data visualization infographics
- ✅ 40+ customer testimonial cards (HTML + PNG)
- ✅ Brand guides (HTML & PDF)
- ✅ Container specifications and technical docs

### Project Setup (All Complete)
- ✅ GitHub repository initialized
- ✅ Organized folder structure
- ✅ Project documentation (CLAUDE.md, briefs, guides)
- ✅ Git repository with initial commit
- ✅ Configuration files (.claude/settings.json, .gitignore)

---

## 5. What Needs to Be Done Next

### Phase 2: Website Audit (August 2026)
- [ ] Run comprehensive pre-launch audit
- [ ] Check current website (tech stack, SEO, UX)
- [ ] Verify Google Business Profile
- [ ] Document optimization opportunities

### Phase 3: Content (August-September 2026)
- [ ] Write 10+ blog articles (4 content clusters)
- [ ] Create landing pages for each service
- [ ] Build testimonial showcase
- [ ] Develop lead magnets

### Phase 4: Marketing (September 2026+)
- [ ] Set up email marketing sequences
- [ ] Create social media calendar
- [ ] Optimize for conversions
- [ ] Launch campaigns

---

## 6. Important Rules to Follow

### Brand Compliance ⚠️
- **NO clip art** — Never hand-draw SVGs of real objects
- **AI from photos** — Use Gemini/Claude image gen from client's real photos
- **Check assets first** — Always see if it exists in `/assets/` before creating new

### Design Standards
- **Repo is truth** — GitHub repo is the source of truth
- **Landing pages** — Must pass 16-element conversion checklist
- **Brand colors** — Forest Green primary, Louisiana State Green accents

### Workflow
- Create feature branches: `git checkout -b feature/name`
- Write clear commit messages
- All PRs require review
- Test before marking done

---

## 7. How to Start a Task

### 1. Pick a Task
Go to `BACKLOG.md` and pick a task from the appropriate phase.

### 2. Create a Feature Branch
```bash
git checkout -b feature/task-name
```

### 3. Check Brand Standards
Read `brand-style-guide.md` for tone, voice, and visual guidelines.

### 4. Use Existing Assets
Check `/assets/` for photos, logos, infographics you can use.

### 5. Do Your Work
Write the content, create the graphic, code the feature.

### 6. Commit & Push
```bash
git add .
git commit -m "Clear description of what changed"
git push -u origin feature/task-name
```

### 7. Create Pull Request
Go to GitHub and create a pull request with a clear description.

---

## 8. Where to Find Things

**Brand Logos?**
→ `brand/logos/` (30+ variations)

**Customer Testimonials?**
→ `assets/graphics/reviews/` (40+ cards ready to use)

**Infographics?**
→ `assets/graphics/infographics/` (12+ data visualizations)

**Photos?**
→ `assets/photography/` (50+ product & lifestyle images)

**Customer Reviews/Feedback?**
→ `docs/load-geaux-google-reviews (GOOD).xlsx`

**Blog Content Strategy?**
→ `docs/load-and-geaux-blog-cluster-strategy.xlsx`

**Brand Rules?**
→ `brand-style-guide.md`

**Project Instructions?**
→ `CLAUDE.md`

**Client Info?**
→ `00-CLIENT-BRIEF.md`

---

## 9. Quick Command Reference

### View Project
```bash
cd "/Users/clintsanchez/Documents/Claude/Projects/Load and Geaux Portable Storage"
ls -la
```

### Check Status
```bash
git status
git log --oneline | head -10
```

### Create a Branch
```bash
git checkout -b feature/your-feature-name
```

### Make Changes & Commit
```bash
# Make your changes...
git add .
git commit -m "Your commit message"
git push -u origin feature/your-feature-name
```

### View Documentation
```bash
cat CLAUDE.md                    # Project instructions
cat 00-CLIENT-BRIEF.md           # Client overview
cat brand-style-guide.md         # Brand standards
cat BACKLOG.md                   # Work items
```

---

## 10. When You're Stuck

### Can't find something?
1. Check `CLAUDE.md` for project context
2. Check `README.md` for folder structure
3. Search `/docs/` for reference materials
4. Ask Clint Sanchez (clint@clintsanchez.com)

### Not sure about brand voice?
→ Read `brand-style-guide.md` + examples

### Not sure what to work on?
→ Check `BACKLOG.md` for prioritized tasks

### Need permission to do something?
→ Check `.claude/settings.json` or ask Clint

### Technical question?
→ Check `CLAUDE.md` development section or docs in `/docs/`

---

## 11. Success Checklist

Before considering a task "done":

- [ ] Follows brand voice & style guide
- [ ] Uses existing assets where possible
- [ ] All links checked and working
- [ ] Mobile responsive (if applicable)
- [ ] Clear, descriptive commit message
- [ ] Tested locally (if code)
- [ ] PR created with description
- [ ] Follows project standards

---

## 12. Next Immediate Action

1. Read **CLAUDE.md** (15 minutes)
2. Skim **00-Client-Brief.md** (10 minutes)
3. Bookmark **brand-style-guide.md** (reference)
4. Open **BACKLOG.md** and pick Phase 2 tasks
5. Start with website audit (see Phase 2 in BACKLOG.md)

---

## 13. Helpful Reminders

✅ **This is a real client** — Load and Geaux Portable Storage is a legitimate business in Baton Rouge, LA. They have real customers, real reviews, and real business needs.

✅ **Quality matters** — This isn't a test project. The work you do will be live on their website and seen by their customers.

✅ **All assets are ready** — You have logos, photos, infographics, testimonials, and strategy docs. Use them!

✅ **Documents are your friend** — The docs in this repo (CLAUDE.md, brand-style-guide.md, BACKLOG.md) have most answers.

✅ **Brand consistency is key** — Especially important for a growing local business. Every piece should feel like "Load and Geaux."

---

## 14. File Locations Reference

### Local Project (Work Here)
```
/Users/clintsanchez/Documents/Claude/Projects/Load and Geaux Portable Storage
```

### pCloud Original Assets (Reference)
```
/Users/clintsanchez/pCloud Drive/Documents/BlakSheep Creative/Clients/Load and Geaux Portable Storage
```

### Client Contact
```
Email: loadandgeauxstorage@gmail.com
Phone: +1 (225) 501-2830
```

---

**Ready to start?**

1. ✅ Read CLAUDE.md
2. ✅ Review brand-style-guide.md
3. ✅ Pick a task from BACKLOG.md
4. ✅ Create a feature branch
5. ✅ Do the work
6. ✅ Commit and push
7. ✅ Create a pull request

**Questions?** Check CLAUDE.md or ask Clint (clint@clintsanchez.com)

---

**Last Updated:** July 22, 2026  
**Quick Start Guide**  
**Load and Geaux Portable Storage Project**
