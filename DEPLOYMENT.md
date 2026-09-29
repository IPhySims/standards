# Domain Registration & Deployment Plan

## Domain Name Strategy

### Recommended Primary Domain

| Domain | Status | Recommendation |
|--------|--------|----------------|
| **iphysim.com** | ✅ Available | **Primary domain** — Register immediately |
| **iphysim.org** | ❌ Taken (parked) | Attempt to acquire; use as redirect |
| **iphysim.net** | ✅ Available | Register as backup/redirect |
| **iphysim.io** | ✅ Available | Register for tech/developer audience |
| **physicsimulations.org** | ✅ Available | Register for SEO value |

### Recommended Registration

**Register immediately:**
1. `iphysim.com` — Primary website
2. `iphysim.org` — Redirect to .com (if available for purchase)
3. `iphysim.io` — For API/developer resources

**Optional:**
4. `iphysim.net` — Redirect
5. `physicsimulations.org` — Redirect for SEO

### Domain Registrars (Recommended)

| Registrar | .com Price | Notes |
|-----------|-----------|-------|
| **Cloudflare Registrar** | ~$9.15/yr | At-cost pricing, free DNS, free WHOIS privacy |
| **Namecheap** | ~$8.88/yr (1st yr) | Good support, free WHOIS privacy |
| **Google Domains** | ~$12/yr | Clean interface, free WHOIS privacy |
| **Porkbun** | ~$8.73/yr | Cheap, free WHOIS privacy |

**Recommendation**: Use **Cloudflare Registrar** for at-cost pricing and integrated DNS/CDN.

---

## Technical Infrastructure

### Architecture Overview

```
┌─────────────────────────────────────────────────┐
│                  IPhySims Ecosystem                │
├─────────────────────────────────────────────────┤
│                                                 │
│  ┌──────────┐  ┌──────────┐  ┌──────────────┐  │
│  │ Website  │  │  GitHub  │  │  Submission  │  │
│  │ (Static) │  │   Org    │  │   Portal     │  │
│  └────┬─────┘  └────┬─────┘  └──────┬───────┘  │
│       │              │               │          │
│  ┌────┴──────────────┴───────────────┴───────┐  │
│  │            Cloudflare CDN/DNS             │  │
│  └────┬──────────────┬───────────────┬───────┘  │
│       │              │               │          │
│  ┌────┴─────┐  ┌────┴─────┐  ┌─────┴───────┐  │
│  │  Vercel  │  │  GitHub  │  │   Supabase  │  │
│  │ (Static) │  │  Pages   │  │  (Database) │  │
│  └──────────┘  └──────────┘  └─────────────┘  │
│                                                 │
└─────────────────────────────────────────────────┘
```

### Hosting Stack (Recommended — Free Tier)

| Component | Service | Cost | Notes |
|-----------|---------|------|-------|
| **Website** | Vercel or GitHub Pages | Free | Static site, global CDN |
| **DNS** | Cloudflare | Free | Fast DNS, DDoS protection |
| **Code Repos** | GitHub Organization | Free | Open-source repos |
| **Submission Portal** | GitHub Issues + Forms | Free | Structured submissions |
| **Database** | Supabase (free tier) | Free | Simulation metadata, member data |
| **Email** | Zoho Mail (free tier) or Google Workspace | Free–$6/mo | contact@iphysim.com |
| **Communication** | Discord | Free | Community chat |
| **CI/CD** | GitHub Actions | Free | Automated testing/deployment |

### Estimated Annual Cost (Minimum)

| Item | Cost |
|------|------|
| Domain (iphysim.com) | ~$9 |
| Domain (iphysim.io) | ~$35 |
| Hosting | $0 (free tier) |
| Email | $0–$72 |
| **Total** | **~$44–$116/year** |

---

## Deployment Plan

### Phase 1: Immediate (Week 1)

#### 1.1 Register Domains
```bash
# Go to Cloudflare Registrar (or Namecheap) and register:
# 1. iphysim.org
# 2. iphysim.io
# 3. iphysim.net (optional)
```

#### 1.2 Set Up GitHub Organization
1. Create GitHub organization: `github.com/IPhySims`
2. Create repositories:
   - `IPhySims/.github` — Organization profile and community health files
   - `IPhySims/website` — Main website source
   - `IPhySims/submissions` — Simulation submission tracker
   - `IPhySims/simulations` — Curated simulation repository
   - `IPhySims/infrastructure` — Internal tools and automation
   - `IPhySims/community` — Discussion forum and community resources
   - `IPhySims/docs` — Organizational documentation

#### 1.3 Set Up Email
1. Register `contact@iphysim.com`
2. Create aliases:
   - `contact@iphysim.com` — General inquiries
   - `conduct@iphysim.com` — Code of Conduct reports
   - `reviewers@iphysim.com` — Reviewer applications
   - `board@iphysim.com` — Governing Board

#### 1.4 Deploy Website
1. Set up static site generator (Hugo, Astro, or Next.js)
2. Deploy to Vercel/GitHub Pages
3. Configure DNS
4. Set up Cloudflare CDN

### Phase 2: Short-term (Weeks 2–4)

#### 2.1 Website Content
- Home page with mission statement
- About page with organizational structure
- Simulation browser/search
- Submission portal
- Review standards documentation
- Member directory (opt-in)
- Blog/news section

#### 2.2 Community Setup
- Discord server with channels:
  - `#general` — General discussion
  - `#submissions` — Submission questions
  - `#reviews` — Reviewer coordination
  - `#domains/{physics-domain}` — Domain-specific channels
  - `#announcements` — Official announcements
- GitHub Discussions for async conversation

#### 2.3 Automation
- GitHub Actions for:
  - Automated submission intake
  - Reviewer assignment
  - CI testing for submitted simulations
  - Website deployment

### Phase 3: Medium-term (Months 2–6)

#### 3.1 Simulation Repository
- Structured catalog with metadata
- Search by domain, language, educational level
- Simulation detail pages with documentation
- Download/clone instructions
- Validation reports

#### 3.2 Review Management
- Automated reviewer assignment based on domain
- Review tracking dashboard
- Notification system
- Review history and analytics

#### 3.3 Member Management
- Member registration system
- Membership tier tracking
- Voting system for governance
- Member directory

---

## Website Technology Stack

### Recommended: Astro + React

| Technology | Purpose |
|-----------|---------|
| **Astro** | Static site generator (fast, SEO-friendly) |
| **React** | Interactive components (simulation browser) |
| **Tailwind CSS** | Styling |
| **Supabase** | Backend database (members, submissions) |
| **Algolia** | Search functionality |
| **Vercel** | Hosting and deployment |

### Alternative: Next.js

If more dynamic features are needed:
- Next.js with App Router
- Server-side rendering for SEO
- API routes for backend functionality
- Deploy on Vercel

### Alternative: Hugo (Simplest)

For minimal technical overhead:
- Hugo static site generator
- Markdown-based content
- Deploy on GitHub Pages
- Minimal JavaScript

---

## Legal Considerations

### Non-Profit Registration

To operate as a formal non-profit:

| Jurisdiction | Type | Notes |
|-------------|------|-------|
| **USA** | 501(c)(3) | Tax-exempt non-profit; requires IRS application |
| **UK** | Charitable Incorporated Organisation (CIO) | Registered charity |
| **International** | International Non-Profit Organization | Complex; requires legal counsel |

**Recommendation**: Start as an informal open-source organization. Pursue formal non-profit status once the community is established and funding is secured.

### Required Legal Documents
- [x] Charter/Constitution
- [x] Code of Conduct
- [x] Privacy Policy (to be created)
- [x] Terms of Service (to be created)
- [ ] Non-Profit Registration (when ready)

---

## Action Items (Priority Order)

### This Week
1. **Register `iphysim.com`** — Do this first before someone else does!
2. **Register `iphysim.io`** — Secondary domain
3. **Create GitHub organization** — `github.com/IPhySims`
4. **Set up basic email** — `contact@iphysim.com`

### Next Week
5. **Deploy initial website** — Even a placeholder page
6. **Create Discord server** — Community building
7. **Set up social media** — Twitter/X, LinkedIn

### Within a Month
8. **Recruit founding members** — 5–10 committed individuals
9. **Finalize review standards** — Already drafted
10. **Open for submissions** — Start building the repository

---

## Social Media Handles to Reserve

| Platform | Handle | Status |
|----------|--------|--------|
| Twitter/X | @IPhySims | Check availability |
| LinkedIn | /company/iphysim | Check availability |
| GitHub | @IPhySims | Check availability |
| Discord | IPhySims | Create server |
| YouTube | @IPhySims | Check availability |
| Mastodon | @IPhySims@phys.social | Check availability |

---

*This document should be updated as decisions are made and infrastructure is deployed.*
