# Manjahi Dev's — Portfolio & Services Website

**Owner:**   
**Brand:** Manjahi Dev's  
**Contact:** available on request ·   
**Location:** Kenya · Available Worldwide

---

## Overview

Manjahi Dev's is a professional portfolio and service website positioning Wilson Mburu Karanja as a practical technology specialist offering web development, software and system development, data analysis, task automation, UI/UX design, and digital branding solutions.

**Brand personality:** Practical · Elegant · Classy · Intelligent · Modern · Slightly Mysterious

---

## Current Build — Static HTML (v1.0)

### Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | Custom CSS (CSS custom properties, responsive) |
| Scripting | Vanilla JavaScript |
| Fonts | Google Fonts — Syne, DM Mono, DM Sans |
| Forms | Formspree (third-party form handler) |
| Deployment | Any static host — Netlify, Vercel, GitHub Pages |

### File Structure

```
MANJAHI/
├── index.html              # Homepage
├── about.html              # About — profile, objective, philosophy
├── services.html           # All 7 services with feature lists
├── projects.html           # 6 projects with problem/solution/impact
├── skills.html             # Technical, creative, professional skills
├── contact.html            # Contact form, CV download, WhatsApp
├── privacy-policy.html     # Privacy policy
├── terms.html              # Terms of use
├── styles.css              # Global stylesheet (all components)
├── script.js               # Global JS — cursor, animations, nav, form
├── Wilson_Karanja_CV.pdf   # CV file — ADD THIS before going live
└── README.md               # This file
```

### Pages & Sections

| Page | Key Sections |
|---|---|
| `index.html` | Hero · Services Preview · Featured Projects · About Preview · Skills Snapshot · Contact CTA |
| `about.html` | Professional Profile · Career Objective · Work Philosophy |
| `services.html` | Web Dev · System Dev · Data Analysis · Automation · UI/UX · Content · Branding |
| `projects.html` | 6 projects — CBIIC · Tithe System · Payroll · Photo Matching · Data QA · Digital Branding |
| `skills.html` | Technical Skills · Creative Skills · Professional Skills |
| `contact.html` | 8-field contact form · Contact info · CV download · WhatsApp |
| `privacy-policy.html` | Full privacy policy |
| `terms.html` | Full terms of use |

### Design System

| Token | Value | Usage |
|---|---|---|
| `--dark` | `#0f172a` | Nav, footer, dark sections |
| `--teal` | `#0d9488` | Primary accent, CTAs |
| `--teal-2` | `#0891b2` | Secondary accent, tags |
| `--teal-light` | `#ccfbf1` | Highlights, dark section tags |
| `--bg` | `#f8f9fb` | Page background |
| `--bg-alt` | `#f1f5f9` | Alternate section background |
| `--muted` | `#64748b` | Body text, descriptions |
| `--display` | Syne 800 | Headings, brand name |
| `--body` | DM Sans 300/400 | Paragraphs |
| `--mono` | DM Mono | Labels, tags, captions, nav |

---

## Setup — Before Going Live

### 1. Add CV

Place your CV PDF in the project root:

```
Wilson_Karanja_CV.pdf
```

The download button in `contact.html` and `skills.html` is already wired to this filename.

### 2. Activate the Contact Form (Formspree)

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form — set the email to `wmkaranja996@gmail.com`
3. Copy the form ID (e.g. `xpzgkqab`)
4. Open `contact.html` and replace `YOUR_FORM_ID`:

```html
<!-- Before -->
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">

<!-- After -->
<form action="https://formspree.io/f/xpzgkqab" method="POST">
```

5. In your Formspree dashboard, add your domain to the **allowed domains** list for security.

### 3. Add LinkedIn and GitHub Links

In `contact.html`, replace the `#` placeholders:

```html
<a href="https://linkedin.com/in/YOUR-PROFILE" ...>LinkedIn ↗</a>
<a href="https://github.com/YOUR-USERNAME" ...>GitHub ↗</a>
```

### 4. Deploy

Push to any static host:

```bash
# Netlify (drag and drop the folder at netlify.com/drop)

# GitHub Pages
git init
git add .
git commit -m "Initial build — Manjahi Dev's v1.0"
git remote add origin https://github.com/USERNAME/manjahi-devs.git
git push -u origin main
# Then enable GitHub Pages in repo Settings → Pages

# Vercel
npm install -g vercel
vercel
```

### 5. Connect a Custom Domain

Once hosted, point your domain (e.g. `manjahidevs.com`) to the host via your domain registrar's DNS settings. Most hosts (Netlify, Vercel) provide step-by-step instructions in their dashboard.

---

## SEO

Each page includes:
- Unique `<title>` tag
- Unique `<meta name="description">` tag
- Open Graph `og:title` and `og:description` tags

### Suggested Keywords (from spec)
```
Wilson Mburu Karanja portfolio
Manjahi Dev's
Web developer Kenya
Software developer Kenya
System developer Kenya
Data analyst Kenya
ICT specialist Kenya
VBA payroll system developer
Task automation Kenya
Database management Kenya
Freelance web developer Kenya
```

### To Add (post-launch)
- `sitemap.xml` — list all page URLs for search engines
- `robots.txt` — allow all crawlers
- Google Analytics 4 tracking ID in `<head>` of each page
- Google Search Console — verify domain ownership and submit sitemap

---

## Future Specification — v2.0 (Next.js Build)

The current static HTML build is production-ready. The following is the planned upgrade path to a full-featured, CMS-backed website.

### Target Stack

| Layer | Technology | Reason |
|---|---|---|
| Framework | Next.js 14+ (App Router) | SEO, routing, server components |
| Styling | Tailwind CSS | Utility-first, consistent design tokens |
| CMS | Sanity CMS | Headless CMS for easy content editing |
| Deployment | Vercel | Native Next.js hosting, edge network |
| Forms | Resend or EmailJS | Server-side form handling with API routes |
| Analytics | Google Analytics 4 | Traffic and conversion tracking |
| Images | Next.js Image (WebP/AVIF) | Optimised, lazy-loaded images |
| SEO | next-seo or metadata API | Dynamic per-page SEO |

### Planned Features — v2.0

#### Content Management (Sanity Studio)
Editable from a browser dashboard without touching code:
- Homepage hero text and tagline
- Services — titles, descriptions, feature lists
- Projects — all fields (problem, solution, tools, impact, images)
- Skills — add/remove tags per category
- CV file — upload and replace
- Blog posts (optional)
- Testimonials
- Contact details

#### New Pages & Routes

```
/                                   # Homepage
/about                              # About
/services                           # Services overview
/services/web-development           # Individual service pages
/services/system-development
/services/data-analysis
/services/task-automation
/services/ui-ux-design
/services/content-creation
/services/branding
/projects                           # All projects
/projects/[slug]                    # Individual project detail pages
/skills                             # Skills
/contact                            # Contact
/blog                               # Optional blog
/blog/[slug]                        # Individual posts
/privacy-policy                     # Legal
/terms                              # Legal
```

#### Individual Project Detail Pages
Each project gets a full-page case study with:
- Hero image / screenshot
- Full problem statement
- Detailed solution description
- Process / approach section
- Tools and technologies used
- Results and measurable impact
- Related projects
- CTA — "Request a similar solution"

#### Blog (Optional Phase)
A simple blog for publishing articles on topics such as:
- Data analysis insights
- Automation tips for Kenyan businesses
- ICT project case studies
- Tech commentary

Improves SEO and demonstrates expertise.

#### Testimonials Section
Client testimonials displayed on homepage and project pages — editable via Sanity CMS.

#### Dark Mode
Toggle between light and dark themes, with preference saved to `localStorage`.

#### Server-Side Contact Form
Replace Formspree with a Next.js API route (`/api/contact`) using Resend or Brevo:
- Full server-side validation
- Rate limiting
- Auto-reply to enquirer
- Slack/email notification to Wilson

#### Performance Targets

| Metric | Target |
|---|---|
| Lighthouse Performance | 95+ |
| Lighthouse SEO | 100 |
| Lighthouse Accessibility | 95+ |
| Core Web Vitals — LCP | < 2.5s |
| Core Web Vitals — CLS | < 0.1 |
| Image formats | WebP / AVIF |

#### Environment Variables (v2.0)

```env
# .env.local — never commit to git

NEXT_PUBLIC_SITE_URL=https://manjahidevs.com
SANITY_PROJECT_ID=your_project_id
SANITY_DATASET=production
SANITY_API_TOKEN=your_read_token
RESEND_API_KEY=your_resend_key
CONTACT_EMAIL=wmkaranja996@gmail.com
NEXT_PUBLIC_GA_ID=G-XXXXXXXXXX
```

### v2.0 Build Checklist

#### Phase 1 — Planning
- [ ] Confirm domain name and purchase
- [ ] Set up Sanity CMS project
- [ ] Define content schema for all types
- [ ] Gather project screenshots and images
- [ ] Write testimonials (if available)
- [ ] Prepare service pricing / package structure

#### Phase 2 — Design
- [ ] Migrate design tokens from CSS to Tailwind config
- [ ] Design individual project detail page layout
- [ ] Design blog post layout
- [ ] Design testimonials component
- [ ] Design dark mode variants
- [ ] Prepare mobile layouts for all new pages

#### Phase 3 — Development
- [ ] Scaffold Next.js 14 project with Tailwind
- [ ] Connect Sanity CMS and define schemas
- [ ] Build shared layout (nav, footer)
- [ ] Build homepage with dynamic CMS content
- [ ] Build services pages (overview + individual)
- [ ] Build projects pages (grid + detail)
- [ ] Build about, skills, contact pages
- [ ] Implement server-side contact form (API route)
- [ ] Add CV download from CMS-managed asset
- [ ] Implement dynamic SEO metadata per page
- [ ] Generate `sitemap.xml` and `robots.txt`
- [ ] Add Google Analytics 4
- [ ] Implement dark mode toggle

#### Phase 4 — Testing & Launch
- [ ] Test all pages on mobile, tablet, desktop
- [ ] Test contact form (delivery + auto-reply)
- [ ] Test CV download
- [ ] Run Lighthouse audit — hit all targets
- [ ] Test all internal links
- [ ] Test SEO metadata in browser and social preview tools
- [ ] Test accessibility — keyboard nav, screen reader, colour contrast
- [ ] Deploy to Vercel
- [ ] Connect custom domain
- [ ] Submit sitemap to Google Search Console
- [ ] Enable Google Analytics and verify data

---

## Services Offered

| Service | Description |
|---|---|
| Web Design & Development | Portfolio, business, and landing page websites |
| Software & System Development | Management systems, payroll, workflow platforms |
| Data Analysis & Database Management | Python, R, SQL — analysis, cleaning, QA |
| Task Automation | VBA, Google Workspace, automated responses |
| UI/UX Design | Interfaces, dashboards, wireframes |
| Content Creation & Digital Marketing | Campaigns, social media, channel strategy |
| Branding & Creative Design | Visual identity, event branding, outdoor concepts |

---

## Projects

| # | Project | Category |
|---|---|---|
| 01 | CBIIC Incubate Management System | System Development |
| 02 | Tithe Management & Automated Response System | Automation |
| 03 | Payroll Management & Processing System | Business Automation |
| 04 | Photo-Name Matching Model | Data Processing / ML |
| 05 | Data Management & Quality Assurance | Data Management |
| 06 | Digital Channel Growth & Creative Branding | Marketing / Branding |

---

## License & Usage

All content, design, and code in this repository is the intellectual property of Wilson Mburu Karanja / Manjahi Dev's. Unauthorised reproduction or redistribution is not permitted. See [terms.html](terms.html) for full terms.

---

*Manjahi Dev's — Web, Software, Data & Digital Solutions*  
*Nairobi, Kenya · Available Worldwide*
