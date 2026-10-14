AUREA STUDIO — PREMIUM INTERIOR DESIGN WEBSITE (PITCH DEMO)
===========================================================

WHAT THIS IS
A complete, production-quality single-page website for an interior design &
construction studio, built to the "luxury architectural editorial" direction:
ivory/beige/terracotta/sage/walnut palette, Cormorant Garamond serif headings,
Manrope body, cinematic hero, editorial portfolio, 6-step enquiry wizard,
WhatsApp hand-off, mobile sticky CTA, reduced-motion support, SEO meta +
JSON-LD, and an honest privacy section.

FILES
  index.html   the whole site (HTML + CSS + JS in one file)
  img/         8 licensed demonstration photographs (hero, about, 6 portfolio)
  README.md    this file

IMPORTANT — WHAT IS REAL vs WHAT IS PENDING
Real and working right now:
  * Full page design, navigation, animations, responsive layout
  * 6-step enquiry wizard with validation (Indian mobile, email, area limits),
    step progress, review screen, localStorage progress save/restore
  * WhatsApp message builder: uses the visitor's actual selections, opens a
    correctly encoded wa.me link, honest fallback message if no number set
  * Video hero slot: drop a file at img/hero-walkthrough.mp4 and it plays
    automatically; until then the poster image shows (already works)

Pending configuration (marked clearly in the code):
  * CONFIG at the top of the <script> in index.html:
      - businessName / phone / email  -> the studio's real details
      - whatsappNumber                -> e.g. "919876543210" (digits only)
      - apiEndpoint                   -> backend URL that saves enquiries
  * The lead-capture backend (Supabase "project_enquiries" table + server
    validation + email notification + /admin dashboard) is designed and
    documented but needs hosting + credentials to go live. Until then a
    submitted enquiry shows a demo confirmation, clearly labelled.
  * Portfolio images are licensed stock photos, labelled "Case study —
    placeholder". They are NOT presented as completed client projects.
  * No testimonials are fabricated; the section says words go in when real.

HOW TO USE IT AS A PITCH
  1. Unzip, double-click index.html — it opens and works offline.
  2. To demo a specific studio: open index.html, edit the CONFIG block and
     the <title>, swap logo text "Aurea." for their name (2-minute change).
  3. Offer: their real photos + details drop in; Supabase lead backend and
     /admin dashboard are the paid scope.

DEPLOYMENT (when a studio says yes)
  * Static hosting (Netlify / Vercel / Cloudflare Pages): upload the folder.
  * For the full backend: Next.js + Supabase — create the project_enquiries
    table (id, lead_reference, name, email, phone, preferred_contact_method,
    project_type, property_type, area_sqft, budget_range, location, timeline,
    requirements, attachment_references, consent_status, consent_timestamp,
    lead_source, lead_status, created_at, updated_at), keep the service-role
    key in server env vars only, add rate limiting + a staff-auth /admin.
