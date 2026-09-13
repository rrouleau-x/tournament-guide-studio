# Field Guide — Business Case & Build Plan
**Status:** draft for Rich's review · not distributed · prepared 2026-09-13

---

## 1. The market check (what I actually found)

### The B2C idea is dead on arrival
Selling guides directly to parents does not work. Evidence:

- The information parents want is already free and everywhere — Trace, Youth
  Inc., SoccerWire, Northeast Rush, and even hotel chains publish "tournament
  travel tips" content.
- Team management apps are commoditized: Spond and Vanta are free, TeamSnap
  runs roughly $10–$21 per team per month, and TeamSnap for Business bundles
  parent communication at no incremental cost.
- The only paid parent-facing products that exist are generic $4–$25 Etsy
  printable planners ("sports mom planner," "tournament weekend itinerary").
  That is a hobby business, not a service business.

**Conclusion: parents will not pay for information. Do not build this.**

### The B2B2C idea is wide open
Nobody is producing the parent-facing operational guide as a service. The
competitive set splits cleanly:

| Player type | What they own | What they don't do |
|---|---|---|
| Scheduling platforms (GotSport, SincSports, Tourney Machine) | Brackets, scores, results | Write anything for parents |
| Team apps (TeamSnap, Spond, SportsYou, Vanta) | Roster, calendar, chat | Travel logistics content |
| Housing bureaus (Traveling Teams, etc.) | Hotel blocks, room revenue | Parent-facing trip guide |
| Tournament software (Fastbreak AI, Tournated, Live Tourney) | Registration, revenue ops | The parent document itself |

Every one of these hands the club a tool and leaves the actual *writing and
research* to a volunteer. That volunteer is the customer.

### Where the money already is
This matters more than the guide itself. Clubs and tournaments already sell
exactly the audience a guide delivers:

- **Club sponsorship tiers:** $500 Bronze / $1,000 Silver / $2,500 Gold /
  $3,000–$5,000 Platinum — published rates, Cape Express Soccer Club.
- **Printed program ads:** $500 half page / $1,000 full page (high school
  media kit); small events around $170 full page.
- **Vendor booths:** $350 for a four-day youth soccer tournament (Murrieta
  Youth Soccer League rate card).
- **Housing rebates:** Traveling Teams advertises increasing organizer revenue
  "by an average of 50% for new clients." Stay-to-play is a major revenue line
  — and is under legal pressure (a class action was filed in May 2026 over a
  stay-to-play policy), which makes clear, compliant parent communication
  *more* valuable, not less.

### The pain, quantified
- Sports parents spend an average of **3 hours 23 minutes per day** on their
  child's sport on game or practice days (Aspen Institute Project Play).
- Volunteer parent managers carry tournament logistics on top of that, on top
  of a job. This is burnout labor the club is not paying for.

---

## 2. The offer

**Turn a tournament packet into a branded parent guide + offline app, in 48 hours.**

Already built and proven — this is not a concept:
- The 17-section parent guide structure (status-labelled: Official /
  Confirmed / Recommended / Pending).
- The offline-capable PWA with QR distribution.
- Live production example: `rrouleau-x.github.io/sporting-jax-guide/app/`
- Current draft offer page: `rrouleau-x.github.io/tournament-guide-studio/`

What gets automated: intake, research assembly, guide generation, PDF export,
PWA deploy, live refresh of hotels/schedule/weather.
What stays human: the sales conversation and the final quality review.

---

## 3. Pricing (proposed — not yet market-tested)

| Plan | Price | Scope |
|---|---|---|
| Per Event | $750 | One tournament, up to 3 team variants, HTML + PDF + PWA |
| Club Season | $2,000 / season | Up to 8 events, white-label, priority turnaround |
| Tournament Organizer | $1,500 / event | Hosted event, sponsor directory, housing messaging |

Sponsorship inventory (revenue the club keeps):
- Presented by — $1,500 (one per event)
- Guide sponsor — $500
- Local directory listing — $150

**The anchor that closes it:** one Gold sponsorship at $2,500 covers a full
Club Season plan with $500 left over. A 12-team club already pays more than
this annually for scheduling software that writes nothing for parents.

---

## 4. Honest unit economics

- Delivery cost per guide after automation: near zero (static hosting + LLM
  research time).
- Gross margin is very high; the constraint is **sales**, not production.
- Realistic season one: 5–10 clubs × $2,000 = $10,000–$20,000, plus any
  sponsorship rev-share. This is a real side income, not a passive one — the
  first ten customers require actual outreach.
- Timeline to first dollar: 3–8 weeks of outreach, assuming warm intros.

### The deal-breaker risk
Not production. **Distribution.** This only works if clubs and organizers are
actually reachable. They are — directories of sanctioned tournaments are
published by Georgia Soccer and US Club Soccer — but the outreach still has to
be done by a human.

---

## 5. Target list

`prospects-southeast.csv` — 30 real, verified events with host clubs and URLs,
sourced from the Georgia Soccer sanctioned tournament list and the US Club
Soccer national sanctioned list.

**Warm targets first** (clubs Rich already has a relationship with through
Niko's season):
1. Savannah United — hosts 5 events/year, deepest relationship
2. Sporting Jax — hosts multiple tournaments, existing app relationship
3. Jacksonville FC — Labor Day Shootout, U8–U19
4. Carolina Cup / Columbia SC organizers
5. Tucker Youth Soccer Association (Triumph Cup)

The Georgia Soccer and US Club Soccer directories can be scraped fully on
demand to expand this to hundreds of events nationally.

---

## 6. Build plan

**Already done (v1)**
- [x] Offer page live at `rrouleau-x.github.io/tournament-guide-studio/`
- [x] Pricing model anchored to verified comparables
- [x] Prospect list of 30 real events
- [x] Guide + PWA production pipeline (existing skills, proven in production)

**Next, if approved**
1. Brand decision — "Field Guide" is a placeholder; alternatives: Sideline
   Guide, Matchday, Tournament Guide Studio.
2. Stripe payment link + simple intake form (tournament packet upload).
3. Scrape the full Georgia + US Club Soccer directories into the prospect CSV.
4. Build one *new* sample guide from cold, for a real upcoming event, timed —
   to prove the 48-hour claim rather than assert it.
5. Send 5 warm emails. Measure replies before building anything else.

**Deliberately not building yet:** a client portal, self-serve signup,
multi-sport expansion, or any marketing site beyond the one-pager. Those come
after five paying clubs, not before.
