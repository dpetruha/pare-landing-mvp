# Pare — Phone Plan Savings MVP

A smoke-test landing page that lets users upload a usage screenshot and promises personalized plan recommendations. Validates demand before building a real backend.

## Tech Stack

- **Static HTML** — single file, no build step
- **Tailwind CSS** (via CDN)
- **Tally.so** — form builder for email + file upload, Google Sheets sync
- **Hosting** — Netlify / Vercel / Cloudflare Pages (free tier)

## Session Log (2026-07-03)

### Built
- Complete landing page (`index.html`) with: hero, usage screenshot accordion (vanilla JS), how-it-works, privacy promise, testimonial, final CTA, footer
- Added Pare to Devapa entrypoint (`~/Projects/MyDev/Devapa/apps/pare/`)

### Design Decisions Made
- **Usage screenshot, not a bill** — asking for a screenshot of data usage (GB/minutes/texts) removes friction and privacy anxiety vs. a full bill PDF
- **No "we don't read contacts" language** — since we only ask for a usage screenshot (which has no contacts/messages), mentioning it plants unnecessary doubt
- **Name: Pare** — short (4 letters, 1 syllable), verb-form, means "trim by cutting off the outer layer" — exactly what the app does. Low trademark risk (common English word used descriptively)
- **Email: Namecheap Private Email ($14.88/yr) over Zoho Free** — single dashboard with domain registrar, IMAP support for Gmail integration, 10 free aliases

### Domain & Email Setup
- **Domain:** `devapa.com` registered at Namecheap
- **Website:** GitHub Pages (devapa.com)
- **Email hosting:** Namecheap Private Email Starter — `$14.88/yr`
- **DNS configured:** ✅ MX (mx1/mx2.privateemail.com), ✅ SPF, ✅ DKIM
- **Primary mailbox:** `admin@devapa.com`
- **Aliases (free):** `pare@devapa.com`, `support@devapa.com` (more as needed)
- **Landing page subdomain:** `pare.devapa.com` (TBD — deploy to Netlify + CNAME)

### TODO

**Immediate (before launch):**
- [x] Create Tally form with: Email (required) + File upload (images/PDF, required)
- [x] Replace Tally URL in `index.html`
- [x] Create mailbox in Namecheap Private Email dashboard
- [ ] Deploy landing page to Netlify
- [ ] Point `pare.devapa.com` DNS CNAME to Netlify
- [ ] Set up Typeform → Google Sheets sync

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