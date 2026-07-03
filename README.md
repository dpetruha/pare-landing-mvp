# Pare — Phone Plan Savings MVP

A smoke-test landing page that lets users upload a usage screenshot and promises personalized plan recommendations. Validates demand before building a real backend.

## Tech Stack

- **Static HTML** — single file, no build step
- **Tailwind CSS** (via CDN)
- **Tally.so** — form builder for email + file upload, Google Sheets sync
- **Hosting** — GitHub Pages (free, custom domain)

## Session Log (2026-07-03)

### Built
- Complete landing page (`index.html`) with: hero, usage screenshot accordion (vanilla JS), how-it-works, privacy promise, testimonial, final CTA, footer
- Added Pare to Devapa entrypoint (`~/Projects/MyDev/Devapa/apps/pare/`)

### Design Decisions Made
- **Usage screenshot, not a bill** — asking for a screenshot of data usage (GB/minutes/texts) removes friction and privacy anxiety vs. a full bill PDF
- **No "we don't read contacts" language** — since we only ask for a usage screenshot (which has no contacts/messages), mentioning it plants unnecessary doubt
- **Name: Pare** — short (4 letters, 1 syllable), verb-form, means "trim by cutting off the outer layer" — exactly what the app does. Low trademark risk (common English word used descriptively)
- **Email: Namecheap Private Email ($14.88/yr) over Zoho Free** — single dashboard with domain registrar, IMAP support for Gmail integration, 10 free aliases
- **Form: Tally.so over Typeform** — free tier, simpler, native Google Sheets sync
  - Tally form URL: `https://tally.so/r/J9Y107`

### Domain & Email Setup
- **Domain:** `devapa.com` registered at Namecheap
- **Website:** GitHub Pages (devapa.com)
- **Email hosting:** Namecheap Private Email Starter — $14.88/yr
- **DNS configured:** ✅ MX (mx1/mx2.privateemail.com), ✅ SPF, ✅ DKIM
- **Primary mailbox:** `admin@devapa.com`
- **Aliases (free):** `pare@devapa.com`, `support@devapa.com` (more as needed)
- **Landing page:** `pare.devapa.com` → CNAME → `dpetruha.github.io` (GitHub Pages)
- **SSL cert:** ⏳ Provisioning (GitHub Pages, up to 15-60 min)

### TODO

**Immediate (before launch):**
- [x] Create Tally form with: Email (required) + File upload (images/PDF, required)
- [x] Replace Tally URL in `index.html`
- [x] Create mailbox in Namecheap Private Email dashboard
- [x] Deploy landing page to GitHub Pages
- [x] Point `pare.devapa.com` DNS CNAME to GitHub Pages
- [ ] Wait for SSL certificate to provision
- [ ] Set up Tally.so → Google Sheets sync

**Second priority (nice to have before launch):**
- [ ] Set up Gmail integration — forward Private Email to Gmail inbox, add "Send mail as" for `admin@devapa.com` and `pare@devapa.com`

**Post-launch:**
- [ ] Test full flow: landing page → Tally submission → email notification
- [ ] Manually reply to first submissions with plan recommendations
- [ ] Evaluate demand signal to decide on backend build

## File Structure

```
pare-landing-mvp/
├── index.html         ← The landing page (self-contained)
├── init.ai.md         ← Original build spec
└── README.md          ← This file
```