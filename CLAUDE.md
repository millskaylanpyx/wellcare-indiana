# Wellcare Indiana CAHPS & Preventive Care Dashboard

## What this is
A single-page HTML dashboard for the Pyx Health account team managing the Wellcare Indiana SOW #13 partnership. Deployed via GitHub Pages at **millskaylanpyx.github.io/wellcare-indiana**.

Everything is one file: `index.html` — HTML + CSS + JS, all inline. No build step, no backend.

---

## File structure
```
index.html    — the entire dashboard (HTML + CSS + JS inline)
CLAUDE.md     — this file
```

---

## Program Context
- **Program Name:** Wellcare IN CAHPS & Preventive Care Program (2026)
- **Program Type:** Member Activation Program — Motivate (FarmboxRx produce boxes + Pyx engagement)
- **SOW:** #13, dated February 1, 2026
- **Project Plan ID:** 20267001
- **Line of Business:** Medicare
- **State:** Indiana (single market)
- **Program Start:** March 13, 2026
- **Program End:** December 31, 2026 (auto-renews annually through 2028)
- **NOT TO EXCEED:** $1,288,328

---

## Wellcare's 3 Goals
1. Increase member engagement (high-touch, intentional)
2. Address CAHPS performance (SDOH screening, PHQ-4, benefit reinforcement)
3. Drive completion of preventive care milestones (AWV, flu vaccine, preventive screenings)

---

## Milestone Box Structure (up to 5 boxes per member)
| Box | Trigger |
|-----|---------|
| Box 1 | Push Box — go-live April 13, initial cohort of 4,141 members |
| Box 2 | Program Opt-In + Care Barrier Assessment |
| Box 3 | Annual Wellness Visit (AWV) attestation |
| Box 4 | Preventive Screening attestation (COL, BCS, dental, A1c) |
| Box 5 | Annual Flu Vaccine attestation |

---

## Member Population
- **7,000 eligible members** (annual scope)
- **~2,100 target activation** (30% opt-in rate)
- Indiana only, Medicare

---

## Key Contacts
| Role | Name | Email |
|------|------|-------|
| Pyx — Director, Strategic Accounts | Kaylan Mills | kaylan.mills@pyxhealth.com |
| Pyx — Chief Revenue Officer | Alexis Colton | alexis.colton@pyxhealth.com |
| Wellcare — VP, Quality Improvement | Hagy Wegener | hagy.wegener@wellcare.com |

---

## How to update the dashboard

### Monthly update checklist
All data lives in the `const D = { ... }` object near the bottom of `index.html`.

Fields to update each month (pull from Pyx Tableau):
- `D.metrics.pushBoxesShipped`
- `D.metrics.membersOptedIn`
- `D.metrics.optInRate`
- `D.metrics.careBarrierAssessments`
- `D.metrics.awvAttestations`
- `D.metrics.preventiveAttestations`
- `D.metrics.fluVaccineAttestations`
- `D.metrics.sdohNeedPct`
- `D.metrics.avgSocialNeeds`
- `D.metrics.phq4Avg`
- `D.metrics.ucla3Avg`
- `D.screenings[*].actual` — screening completion counts
- `D.revenue.revenueToDate`
- `D.program.reportMonth` and `D.program.dataAsOf`
- `D.program.programMonth` — e.g. "3 of 9"
- `D.milestones[*].actual` — box completion counts
- `D.milestones[*].status` — "pending" → "active" → "done"
- `D.flags[]` — update account health narrative
- `D.narrative[]` — update client-facing story

### Milestone status values
- `"pending"` — not yet reached
- `"active"` — in progress / currently trackable
- `"done"` — completed

### SLA status values
- `"pending"` — data not yet available
- `"active"` — currently accumulating
- `"exceed"` — at or above target
- `"behind"` — below target

---

## Deploying changes
Push to `main` — GitHub Pages auto-deploys in ~60 seconds.

```bash
git add index.html
git commit -m "Update [Month] metrics"
git push
```

---

## Brand
Pyx Health brand:
- Green: `#49a601` | Slate: `#2e4456` | Teal: `#29a4a2`
- Headlines: Roboto Slab | Body: Montserrat
- Tone: action-oriented, data-driven, warm

---

## Related project
The Molina DSNP Stars Partnership dashboard (same architecture) lives at:
- GitHub: `rswan-code/molina-stars-partnership`
- URL: `rswan-code.github.io/molina-stars-partnership`

---

## Owner
Kaylan Mills — kaylan.mills@pyxhealth.com
