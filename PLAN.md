# Deposit Saver Kit — Plan

Status: **DRAFT for Evan's approval.** Nothing below is built yet. Approving this doc unblocks Marketing to build the PDF (see `SPEC.md`).

Scope guard: this is **Deposit Saver Kit only**. Subscription Kill Pack is dead and stays dead. See the kill list at the bottom.

---

## 1. Business one-pager

| | |
|---|---|
| **Product** | Deposit Saver Kit — a printable move-in/move-out inspection kit for renters |
| **Price** | **$4.99 one-time** (see pricing note) |
| **Format** | Instant digital download: US Letter PDF (~12 pages) + optional Google Sheet (photo log + deposit-deadline countdown) |
| **Buyer** | Apartment renter, 22–40, moving out or just got keys, anxious about losing the deposit. Secondary: the roommate who runs the walkthrough |
| **Job to be done** | Walk out with dated proof, a clean unit, and a paper trail that makes "we're keeping your deposit" harder to pull |
| **Why they pay** | $5 to protect $800–$2,000. One kept deposit pays back 100–400x |
| **Why now** | Move time = highest intent, shortest decision. They buy the night before the walkthrough |
| **Role in Evan's business** | Second cash lane. DFW HVAC AI retainers stay #1. This ships once and sells passively with near-zero babysitting |
| **First audience** | DFW / Texas renters (Evan's local network, no ads). Kit works anywhere; Texas gets a 30-day-deadline reminder |
| **Channels** | Etsy digital listing and/or Stripe Payment Link. Same-day setup. No Printify, no ads, no email sequences |
| **Ops after launch** | Zero scheduled work. Answer the occasional buyer message. Re-check the Texas timeline once a year |

### Pricing note

Recommend **$4.99** at launch, one SKU, Sheet included (not a paid upsell).

- Comps: Etsy/Payhip move kits sell at ~$3–$6. $4.99 sits in-band and reads as "obviously cheap vs. the deposit."
- $5.99 is defensible (we bundle photo protocol + wear-vs-damage + templates, which free checklists don't) but adds friction for a pure-impulse buy. Test it later only if conversion is fine and reviews are good. Not a launch decision.
- Approximate net per sale: Etsy ≈ $4.00 (listing $0.20 + 6.5% transaction + 3% + $0.25 processing); Stripe ≈ $4.55 (2.9% + $0.30). Both are fine. Volume, not margin, is the game.

### Pain (the reason the product exists)

- Texas has no statewide cap on deposits. 1x rent is common; weak credit pushes 1.5–2x. So $800–$2,000 is at stake for the target buyer.
- Texas generally requires the landlord to refund (or itemize deductions in writing) within 30 days after the tenant surrenders the unit **and** gives a written forwarding address. Normal wear and tear is not a chargeable deduction. (Practical summary, not legal advice; see `DISCLAIMER.md`.)
- Where renters actually lose money: no dated move-in photos, cleaning the wrong things, missing keys/fobs, and never sending the forwarding address in writing. Every one of those is a checklist problem, not a legal problem. That is the product.

### Promise (copy anchor)

> Walk out with dated proof, a clean unit checklist, and the paperwork trail that makes "we're keeping your deposit" harder to pull.

---

## 2. Product scope (v1)

### Must-haves (non-negotiable for v1)

1. **Side-by-side move-in / move-out columns** on every room sheet
2. **Photo ID#** column tying each line item to a specific photo
3. **Keys / fobs / remotes log** (issued vs. returned)
4. **Written forwarding-address email template** (the single highest-value page)
5. **Wear-vs-damage cheat sheet** with a visible "not legal advice" footer

### Included

- PDF, US Letter, ~12 pages, high-contrast, prints clean in black and white
- Notebook aesthetic (ruled lines, checkbox squares, generous write-in space). Looks good on a phone, works on paper
- Google Sheet template (view-only link, buyer makes a copy) with `Photo_Log`, `Deadline`, `Instructions` tabs
- Three email templates: move-in condition report, move-out notice + forwarding address, post-deadline follow-up
- Texas-aware 30-day timeline with a "check your state/lease" line for everyone else
- Personal-use license (one household) and disclaimer, printed in the PDF

### Not in v1 (explicitly)

- Bank sync, budgeting, or any financial data
- Lawyer letters or demand letters for sale
- State-by-state law database (one Texas line + "check your state" is the whole feature)
- Landlord CRM, tenant portal, accounts, logins
- Web app of any kind. Delivery is a file link, full stop
- Fillable-form PDF (nice-to-have for v1.1; v1 is print-or-annotate)
- Video walkthroughs, courses, community
- Anything requiring weekly content

Detailed page-by-page and tab-by-tab spec: **`SPEC.md`**.

---

## 3. PDF + Sheet spec (summary)

Full spec with field lists and draft copy lives in `SPEC.md`. Summary so the plan can be approved on its own:

| Page | Content |
|---|---|
| P1 | Cover, promise, "30–60 minute path" callout |
| P2 | How to use: Move-IN (within 48h of keys) and Move-OUT (7 days before, day-of, after keys) |
| P3 | Property info: address, unit, landlord/PM contact, lease dates, deposit amount, notice requirement, key count |
| P4 | Room sheet: Living / entry |
| P5 | Room sheet: Kitchen |
| P6 | Room sheet: Bedroom(s) |
| P7 | Room sheet: Bathroom(s) |
| P8 | Other areas (closets, laundry, balcony/patio, garage/storage) + meter readings + keys/fobs log |
| P9 | Move-out cleaning checklist (what landlords actually charge for) |
| P10 | Wear vs. damage cheat sheet, with disclaimer footer |
| P11 | Photo protocol + blank photo log |
| P12 | Timeline, three email templates, disclaimer, license, Sheet link |

Room sheet columns (P4–P8): **Area | Move-in condition | Move-out condition | Notes | Photo ID#**

Google Sheet tabs:

- **A `Photo_Log`**: Date | Time | Room | Filename | What it shows | Shared with landlord? | Link
- **B `Deadline`**: Move-out date | Forwarding address sent? | Deposit amount | State deadline days (default 30) | Target return date (formula) | Received? | Notes
- **C `Instructions`**: how to copy the sheet, how to name photos, when to fill each tab

### Build approach (for Marketing)

- Source of truth for the PDF lives in `/pdf` in this repo. Preferred: HTML + CSS rendered to PDF (reproducible, diffable, easy to fix a typo and re-export). Canva/Google Docs is acceptable if faster, but export the source file into `/pdf` too.
- Sheet template lives as a Google Sheet owned by Evan's account; a CSV export of each tab is committed to `/sheet` so the structure is versioned.
- The Sheet link is printed inside the PDF (P2 and P12) so **the PDF is the only file that needs to be uploaded** to Etsy/Stripe.
- Print test on a home printer in black and white before publishing. If it is unreadable in grayscale, it fails.

---

## 4. Go-to-market (week 1)

Goal for the week: **listed and purchasable, then stop.**

### Day 1 — List it

Pick one or both. Both are same-day tasks.

**Etsy digital listing (recommended primary)**
- Built-in file delivery, built-in discovery traffic for "move out checklist," reviews accumulate.
- Upload the PDF (Etsy max 20 MB per file; keep it well under).
- Title, bullets, FAQ, tags: use `LISTING.md`.
- 5 listing images: cover, room sheet, wear-vs-damage, photo log, Sheet screenshot. Export straight from the PDF; no new design work.

**Stripe Payment Link (secondary / for direct shares)**
- One product, $4.99, one Payment Link.
- After-payment behavior: redirect to an unlisted download page (or use Stripe's confirmation-page custom message) containing the PDF link. Turn on receipt emails so the link is also in their inbox.
- Delivery link = unlisted file host (e.g., Drive/Dropbox share or a GitHub release asset). Accept that a $5 link can be shared; the personal-use license covers it and enforcement is not worth Evan's time.
- Business-logic code, webhooks, or a storefront are **out of scope**. If it needs more than the Stripe dashboard, don't build it.

### Day 1–2 — Announce once

- One X post from Evan: the promise, one screenshot of the wear-vs-damage page, the link.
- One post in a local DFW renters / apartments Facebook group (if rules allow), framed as "made this for my own move, $5, here it is." Optional.
- Then **ignore it.** No reply campaigns, no threads, no follow-ups.

### Not doing (week 1 or ever, unless Evan re-scopes)

- Printify or any physical product
- Paid ads
- Email list or sequences
- Affiliate program
- Second listing variants, bundles, or seasonal versions

---

## 5. Ops rules (post-launch)

1. **Zero recurring calendar work.** No content schedule, no posting cadence, no weekly check.
2. **Support = the FAQ.** Buyer messages get a copy-paste FAQ answer (in `LISTING.md`). Target under 5 minutes per message. If a question comes up three times, add it to the FAQ in the listing, not to the product.
3. **Refunds:** digital, so default no-refund on Etsy. On Stripe, refund anyone who asks within 7 days, no questions. A $4.99 argument is never worth having.
4. **Typos and fixes:** batch them. Re-export the PDF at most once a quarter unless something is actually wrong (a broken link, a factual error in the Texas timeline).
5. **Annual check (one calendar reminder, ~30 minutes):** confirm the Texas 30-day timeline and forwarding-address rule still read correctly; confirm the Sheet link still works; confirm the Payment Link / listing is live.
6. **No feature requests get built** unless they (a) are a must-have above that turned out to be broken, or (b) Evan decides to re-scope in writing. "Can you add a version for [state]?" is a no.
7. **Time cap:** if lifetime ops exceed ~2 hours in any quarter, something is wrong with the product, not the buyer. Fix the root cause once or delist.

---

## 6. Success criteria

Modest on purpose. This is a passive lane, not a startup.

| Milestone | Target |
|---|---|
| Listed and purchasable | Within 7 days of plan approval |
| First sale to a stranger (not Evan's network) | Within 30 days of listing |
| Sales in first 90 days | 10+ |
| Refund / dispute rate | Under 5% |
| Buyer support time | Under 30 minutes per month after launch |
| Etsy reviews at 90 days | 3+, average 4.5+ |
| Evan's build+launch time budget | Under 8 hours total for PDF + Sheet + listing |

Kill criteria: if it has zero sales at 90 days **and** the listing has had normal Etsy exposure, either fix the listing images/title once or leave it listed and stop thinking about it. Do not add features to rescue it.

---

## 7. Decisions needed from Evan

Answering these approves the plan.

1. **Price:** $4.99 (recommended) or $5.99?
2. **Channel:** Etsy only, Stripe only, or both? (Recommend both; Etsy primary.)
3. **PDF build tool:** HTML/CSS in repo (reproducible) or Canva (faster)? Either is fine; pick one.
4. **Announce posts:** X only, or X + one DFW FB group post?
5. **Sheet:** ship in v1 (recommended, it's ~30 minutes of work) or defer to v1.1?

---

## 8. Repo layout (target)

```
/pdf            PDF source (HTML/CSS or design source) + exported PDF, once built
/sheet          CSV export of each Sheet tab + link to the live template
README.md       what this is, for anyone landing on the repo
PLAN.md         this document
SPEC.md         page-by-page PDF spec, Sheet tab spec, draft copy and templates
LISTING.md      Etsy/Stripe listing title, bullets, tags, FAQ, support replies
DISCLAIMER.md   not-legal-advice + personal-use license text (also printed in the PDF)
LICENSE         personal-use license for buyers (to be added when the PDF is built)
```

This run writes the plan docs only. No PDF, no Sheet, no Stripe, no code.

---

## 9. Kill list

Do not build, propose, or "just quickly add" any of these:

Subscription Kill Pack · budget planners · van budget (this sprint) · meal planners · chore charts · Printify · KDP journals · landlord legal packs · lawsuit/demand letters as a product · web apps · coder tools · state-law database · landlord CRM · bank sync · anything needing weekly content
