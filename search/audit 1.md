Let me check competitive keyword rankings — branded searches like "salamivf.com" obviously return your own site, so the real signal comes from the queries patients actually use.Now let me audit the actual site to see what on-page SEO factors are working for or against you.Let me verify whether the old indexed pages are still accessible — this is important.# Salam IVF SEO audit & ranking plan

## Current ranking snapshot

| Search query | salamivf.com position | Top competitor in slot #1 |
|---|---|---|
| `salamivf.com` (branded) | #1 — but **all results lead to 404 pages** | — |
| `IVF clinic Bahrain` | ~#6 | janeen-ivf.org |
| `best fertility clinic Bahrain` | ~#4 | bgf-centre.com |
| `egg freezing Bahrain` | **Not in top 10** | bsalaw.com (legal article) |
| `IVF Bahrain` | Not visible in top 10 | bgf-centre.com / janeen-ivf.org |

**Main competitors outranking you:** Bahrain Gynaecology & Infertility Centre (`bgf-centre.com`), Janeen Fertility (`janeen-ivf.org`), Al-Baraka Fertility Hospital (`albarakahospital.bh`), King Hamad University Hospital (`khuh.org.bh`), and Ibn Al-Nafees Hospital (`ibnalnafees.com`).

---

## The single biggest finding: your Google index is stale and broken

Every URL Google currently has indexed for your domain is from the **old WordPress site** and **now returns 404**:

- `/our-lab/` → 404
- `/ivf-process/` → 404
- `/goprocedures/` → 404
- `/gynecology/`, `/insemination-2/`, `/contactus/`, `/doctors/`, `/articles/`, `/endocrinology/`, `/ourteam/`, `/generalsurgery/` → all 404

Your new Hugo site lives at `/en/` and `/ar/` paths, so Google has not connected the old indexed pages to the new ones. This is causing four compounding problems:

1. **Patients clicking your top-ranked branded results land on broken pages.** Anyone searching "Salam IVF" right now hits a dead end.
2. **Crawl budget is being wasted** on 404s instead of discovering your new content.
3. **All link equity** from any external site that ever linked to `/our-lab/`, `/ivf-process/` etc. is being thrown away.
4. **Google demotes domains with high 404 rates**, which explains why you're ranking below competitors who arguably have weaker content.

This is the highest-leverage fix on the entire list. Everything else compounds from here.

---

## On-page issues found on the new Hugo homepage

| Issue | What's there now | What it should be |
|---|---|---|
| `<title>` tag | "Dr Salam Jibrel Medical Center" | "IVF & Fertility Clinic in Bahrain — Dr. Salam Jibrel Medical Center" |
| H1 | "Welcome to Dr Salam Jibrel Medical Center" | "IVF, ICSI & Fertility Treatment in Manama, Bahrain" |
| Meta description | (not set / generic) | Geo + service-led, with phone/WhatsApp |
| NAP (name/address/phone) | Footer only | Above-the-fold + footer + schema |
| Structured data | None visible | `MedicalClinic` + `Physician` + `FAQPage` schema |
| Doctor credentials | Not on homepage | Featured prominently (BGF & Janeen win on this) |
| Patient testimonials | None on homepage | Required — competitors lead with them |
| Success rates / stats | None | "1,000+ cycles", "X% success rate", etc. |
| WhatsApp CTA | Footer link only | Sticky button + above-the-fold CTA |
| Arabic version (`/ar/`) | Exists | Verify `hreflang` tags are present and correct |

---

## Action plan, ordered by impact

### Week 1 — stop the bleeding (highest ROI, lowest effort)

**1. Set up 301 redirects from every old WordPress URL to the new Hugo equivalent.**
Add a redirects map in your Cloudron Surfer config or via `_redirects` if Netlify-served. The mapping:

```
/our-lab/         → /en/services/ivf-lab/
/ivf-process/     → /en/services/ivf-treatment/
/whatisivf/       → /en/services/ivf-treatment/
/insemination-2/  → /en/services/iui/
/gynecology/      → /en/services/gynecology/
/goprocedures/    → /en/services/gynecology/
/generalsurgery/  → /en/services/
/endocrinology/   → /en/services/
/doctors/         → /en/about/
/ourteam/         → /en/about/
/articles/        → /en/blog/
/contactus/       → /en/contact/
```

**2. Verify Google Search Console is set up** for both `salamivf.com` and `www.salamivf.com` (they're treated as separate properties). Submit your `/sitemap.xml` and request re-indexing of the homepage and key service pages.

**3. Fix the `www` redirect.** A `www.salamivf.com` request returns just the redirect URL as text, not an HTTP 301 — that's not how a redirect should work for a search engine. Make sure it's a proper 301 response with a `Location` header.

**4. Check `robots.txt` and `sitemap.xml` are accessible** at the root domain and listed in Search Console.

### Weeks 2–3 — on-page fundamentals

**5. Rewrite title tags & meta descriptions** for every page. Format:
- Homepage: `IVF & Fertility Clinic in Bahrain — Dr. Salam Jibrel Medical Center`
- IVF page: `IVF Treatment in Bahrain | Cost, Process & Success Rates — Salam IVF`
- Egg freezing page: `Egg Freezing in Bahrain | Oocyte Cryopreservation — Salam IVF`
- Doctor page: `Dr. Salam Jibrel — Fertility Specialist, Manama Bahrain`

**6. Add `MedicalClinic` JSON-LD schema** to every page (homepage especially), including:
- `name`, `address` (full Manama address), `telephone`, `openingHours`
- `medicalSpecialty: ["Reproductive Medicine", "Gynecology", "Obstetrics"]`
- `availableService` array listing IVF, ICSI, IUI, egg freezing, etc.
- `aggregateRating` once you have Google reviews live

**7. Add `Physician` schema** for Dr. Salam Jibrel and any other doctors — this is what gets clinics into Google's knowledge panel.

**8. Add a visible NAP block above the fold** with the address, phone, WhatsApp link, and hours. Currently this only exists in the footer.

**9. Add patient testimonials** to the homepage. BGF's homepage is dominated by them and that's a primary reason they rank above you. PDPL-conscious approach: get written consent, anonymize where preferred.

### Month 2 — Google Business Profile + local SEO

**10. Optimize Google Business Profile (GBP)** — this drives the Maps Pack which sits above organic results for "IVF Bahrain" type queries:
- Verify your listing if not already done
- Add the full address (Building 55, Road 200, Block 373, Bughazal, Manama)
- Upload 20+ high-quality photos (lab, reception, doctor, exterior, signage)
- Add all four phone numbers and primary WhatsApp line
- Set categories: `Fertility clinic` (primary), `Obstetrician-gynecologist`, `Medical clinic`
- Post weekly updates (Google ranks active profiles higher)
- Solicit Google reviews systematically — your competitors have hundreds, this is the biggest local-pack ranking lever

**11. Build NAP consistency across local directories:**
- ovu.com (already lists competitors)
- bahrainhealth.com
- whatclinic.com
- yellowpages.com.bh
- bahrainyellowpages.com
- lookbahrain.com

**12. Add the `.bh` country code TLD** as a redirect to `salamivf.com` if available — Google treats `.bh` as a strong local signal for Bahrain searches.

### Months 2–4 — content that targets buying intent

Your competitors mostly have brochure content. The opening to outrank them is **patient-question-driven content**. For each of these, write a 1,500–2,500 word page in both English and Arabic:

- "Cost of IVF in Bahrain" (no competitor owns this — it's the highest-intent commercial keyword)
- "IVF success rates in Bahrain by age"
- "IVF vs ICSI: which is right for you?"
- "Egg freezing in Bahrain: process, cost, and PDPL on storage"
- "How to prepare for your first IVF cycle"
- "PCOS and fertility treatment in Bahrain"
- "Male infertility testing in Bahrain"
- "Insurance coverage for IVF in Bahrain"
- "What to expect at your first fertility consultation"
- "Bahrain IVF law: what married couples need to know" (you cover this, BGF doesn't)

Each page should have FAQ schema for the 5–10 most common patient questions — these often win featured snippets.

### Ongoing — links and authority

**13. Link-building targets** (in priority order):
- Bahrain healthcare directories (above)
- NHRA listing (`nhra.bh`) — government link is gold
- Guest articles in Gulf Daily News, Bahrain News Agency, Tribune Bahrain on fertility topics
- Partnerships with women's wellness blogs in GCC
- Doctor profile listings on global IVF directories (IVF.net, FertilityIQ, EuroCare IVF)
- Press releases on any clinic milestones (new equipment, success stories with consent, doctor awards)

**14. Reviews flywheel:**
- After every successful cycle, ask for a Google review via WhatsApp follow-up
- Aim for 5+ new reviews per month
- Respond to every review within 48 hours (positive AND negative)

---

## Theme decision is now urgent

Docsy is a documentation theme. It's mobile-imperfect, lacks strong trust-signal modules (testimonial sliders, doctor cards, trust badges), and doesn't feel like a clinic site. For an SEO/conversion-driven medical site competing with bgf-centre.com and janeen-ivf.org, I'd consider migrating to a healthcare-oriented theme — either a Hugo theme like **Blowfish** (mobile-first, clean) with custom medical components, or a switch to a self-hosted **WordPress** with a medical theme (Medical Express, MedicalPress) given that the entire competitive set runs WordPress. WordPress also gives you Yoast/RankMath for ongoing SEO management, which Hugo lacks natively.

---

## What to do first this week

1. Deploy the 301 redirect map (above) — this alone will recover ranking for branded search within 2–3 weeks
2. Set up Google Search Console + Bing Webmaster Tools and submit sitemap
3. Claim and optimize Google Business Profile
4. Rewrite the homepage title tag, meta description, and H1 to include "IVF Bahrain" / "Fertility Clinic Bahrain"

Want me to draft the actual `_redirects` file (or Cloudron/Caddy/Nginx config block depending on what your Hugo site is served by), and the JSON-LD schema blocks for the homepage and key service pages?