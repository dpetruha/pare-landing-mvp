Build a static landing page MVP for a mobile plan savings app.

**Tech Stack:**
- Static HTML + Tailwind CSS (via CDN – no build step needed)
- Typeform for the file upload + email capture
- Host on Netlify, Vercel, or Cloudflare Pages (free tier)

**Business Model:**
- Typeform captures: email address + uploaded bill screenshot
- I view submissions in Typeform dashboard or Google Sheets (real-time sync)
- I manually reply to users with personalized plan recommendations
- This is a smoke test to validate demand before building the real backend

**Page Title (SEO / Browser Tab):**
"Stop Overpaying for Your Phone Plan. Upload Your Bill & Save."

---

**Exact Copy & Sections for the Landing Page:**

**Hero Section (Above the Fold):**
- Headline (H1): "You're wasting $500 a year on your cell phone bill."
- Sub-headline: "Carriers bank on you not checking your usage. Stop guessing. Upload your latest bill or screenshot, and we'll instantly show you the exact plan that fits your real habits—without the hidden fees."
- Primary CTA button: "📸 Upload My Bill & See My Savings"
- This button should open the Typeform in a new tab or as an embedded popup.
- Below button in tiny text: "🔒 No credit card required. We only count your data/minutes. We never read your texts or contacts."

**"Don't have your bill?" Accordion (below hero):**
- Trigger link: "❓ Don't have your bill handy? Tap here to find your usage in 30 seconds."
- Expandable content with 3 accordion items (use pure JavaScript to toggle):
  - iPhone Users: Settings > Cellular > Current Period. Screenshot that screen.
  - Android Users: Settings > Network & Internet > SIMs > App data usage.
  - Carrier App Users: Log in > Usage or My Plan. Screenshot the breakdown.

**How It Works (3 steps):**
- Headline: "No math. No guessing. 100% free to check."
- Step 1: "Snap & Upload" – Take a screenshot of your carrier app's usage page or grab your monthly PDF bill.
- Step 2: "We Parse the Fine Print" – Our AI extracts your actual monthly usage (data, minutes, texts) and ignores the fluff.
- Step 3: "Get Your Top 3 Matches" – We compare your real usage against 50+ carriers to show you the cheapest plan.

**Privacy Promise Section:**
- Headline: "We don't want your contacts. We just want your overages."
- Bullet points:
  - "We only count numbers: Our system scans for quantities (GB, Minutes, Texts). It literally cannot read the content of your messages or call history."
  - "Auto-delete: Your uploaded screenshot is deleted immediately after analysis."
  - "No carrier login: We never ask for your carrier username or password."
  - "No spam: Enter your email only when ready. Unsubscribe with one click."

**Social Proof / Testimonial:**
- Headline: "Real people. Real savings. No contract tricks."
- Testimonial: "I was paying $90/month for 'Unlimited' but only used 6GB. This tool found me a $35 plan on the exact same network. I literally saved $660 this year." — Mark R., Chicago (Saved $55/mo)
- Trust badge strip: "Trusted by 2,000+ savvy savers"

**Final CTA Section (bottom of page):**
- Headline: "Stop donating money to your carrier."
- Sub-headline: "Find out in 2 minutes if you're overpaying. If you're not, we'll tell you that too. No hard feelings."
- Button: "📸 Upload My Screenshot – It's Free"
- This button also opens the Typeform.
- Below button: "🔒 Your data is safe. We don't store your bill or share your email."

**Footer disclaimer:**
"We never read your messages or contacts. We only count minutes and megabytes."

---

**Typeform Setup Instructions (to be done manually outside the code):**
1. Create a Typeform with two fields:
   - Field 1: Email address (required)
   - Field 2: File upload (accepts images and PDFs) – make it required
2. Get the Typeform embed link (or direct URL).
3. Connect Typeform to Google Sheets for auto-syncing submissions.

**Technical Requirements for the Static Page:**
- Single HTML file (or minimal HTML + CSS + JS).
- Use Tailwind CSS CDN for styling.
- Mobile-first design.
- The CTA buttons should link directly to the Typeform URL (open in new tab: target="_blank").
- Optional: Use Typeform's embed popup script for a smoother UX.
- The "No bill?" accordion must use vanilla JavaScript (no libraries) for toggling.
- Include smooth scrolling, clean typography, and subtle hover animations on buttons.

**Deliverables:**
Generate a complete, self-contained index.html file (or a set of static assets) that implements this exact design and copy. Include all necessary CDN links and inline JavaScript.