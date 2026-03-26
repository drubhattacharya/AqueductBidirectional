# Aqueduct — Technology-Enabled Community Health Platform

**The intelligence platform that identifies the specific SDOH programs delivering the highest simultaneous return across every regulatory, accreditation, and financial mandate.**

---

## What Aqueduct Does

Nonprofit hospitals receive an average **$11.1M/year in tax exemptions** (Nikpay et al. 2021, *JAMA Internal Medicine*). IRS Form 990 Schedule H requires community benefit documentation — but sets no minimum. State regulators, advocacy groups, and academic literature converge on **5% of total expenses** as the defensible floor.

Most health systems are leaving value on the table. Not because they don't do the work — but because their CHNA programs, quality improvement initiatives, care management investments, and community partnerships aren't connected into a unified, funded strategy that speaks to every stakeholder at once.

Aqueduct changes that. It connects what health systems **must** do (CHNA mandate, CMS SDOH, NCQA accreditation, JC standards) with what funders **need** to do (CRA examination, 5% payout obligation, ESG disclosure) and predicts the specific programs that satisfy every requirement simultaneously.

---

## File Architecture

### `aqueduct-index.html` — The Front Door
- Inspiring, brand-faithful landing with the three-tier value ladder
- Persona selection (Health System / Bank / Foundation) with routing
- Evidence statistics and value proposition copy
- Links to Platform and Intelligence Engine

### `aqueduct-platform.html` — The Main Application
Three distinct persona journeys:

**Hospital Journey (4 steps):**
1. Community Need — Census ACS, CDC PLACES, HRSA, CHNA auto-fetch + document upload
2. ROI Model — 5-layer cascade chart with enable/disable checkboxes
3. Funder Strategy — ranked funder match, strategy by type, gap analysis
4. Documents — 9-card thumbnail grid with Word/Excel preview modal

**Bank/CRA Journey (4 steps):**
1. CRA Profile — FFIEC exam search, current rating, performance gaps
2. Assessment Area Map — real data for the bank's geography
3. Program Finder — Claude finds health systems in the assessment area
4. CRA Package — exam-file documents, term sheet, CRA memo

**Foundation/Corporation Journey (4 steps):**
1. Funding Strategy — 5 vehicle cards (grant, PRI, ESG, direct, sponsorship), 5% payout tracker
2. Need Validation — pull real data for any health system being evaluated
3. Due Diligence — 10-item checklist, every claim mapped to primary source
4. Investment Documents — grant proposal, PRI brief, ESG memo, DAF letter

**Shared across all personas:**
- Document upload with Claude parsing (CHNA, Form 990, CRA exams, grant applications)
- Multi-year trend analysis when 2+ CHNAs uploaded
- NEMT initiative identifier
- Schedule H community benefit calculator
- Legal compliance section (AKS safe harbor, MA framework, CRA regs, foundation rules)
- 9-document generation suite with Word/Excel preview modals

### `aqueduct-intelligence.html` — The Scoring Engine *(most novel file)*

The first tool that scores SDOH programs across **8 compliance dimensions simultaneously**:

| Dimension | What It Measures |
|-----------|-----------------|
| Schedule H Parity | CB credit toward tax exemption gap (Part I Line 7e) |
| CRA Qualification | CD activity strength, LMI documentation, assessment area |
| NCQA / HEDIS | Specific HEDIS measures impacted, star rating lift, MA bonus revenue |
| CMS SDOH / Risk Adj | Z-code HCC uplift, ACO REACH TFU/ACR quality measures |
| JC Accreditation | NPSG standards, Community Care Certification 2024 |
| Financial ROI | 5-layer model: FFS, SDOH, CCM/TCM, VBC, HR/Workforce |
| Funder Accessibility | Concurrent funder types qualifying simultaneously |
| Evidence Strength | GRADE certainty, RCT data, clinical significance thresholds |

**Features:**
- Tax exemption parity calculator (expenses → CB gap → program fill recommendations)
- Profile-adjusted scoring (CHNA priorities, payer mix, HRSA designation, ACO participation)
- Compliance matrix (all 10 projects × all 8 dimensions)
- Portfolio builder (select projects, see combined CB credit, fundable ask, NCQA measures covered)
- AI strategic analysis (Claude generates board brief with specific citations)

### `aqueduct-compliance.json` — Compliance Framework Data
Machine-readable mapping of:
- Schedule H Part I vs. Part II (what counts toward CB total)
- CRA qualification pathways and enumeration gap risk
- NCQA/HEDIS measure mapping by project type
- Joint Commission standards addressed
- CMS SDOH programs (AHC, AHEAD Model, ACO REACH)
- AKS safe harbor conditions (42 CFR §1001.952(bb))
- Tax exemption parity model components

### `aqueduct-evidence.json` — Evidence Base
Structured evidence with effect sizes, certainty ratings, and clinical significance thresholds:
- Shekelle 2022 (HIGH certainty, OR 0.63)
- Chaiyachati RCT 2018 (HIGH certainty counterpoint)
- Balasubramanian 2025 (MODERATE, RRR 0.68)
- Berkowitz 2025 (MODERATE method, LOW magnitude)
- Berkowitz ACO 2022 (critical: NEMT alone not cost-saving)
- CMS 2025 billing rates (CMS-1807-F)

---

## Core Evidence Base

| Study | Finding | Certainty |
|-------|---------|-----------|
| Shekelle 2022 (BMC Public Health) | 37% reduction in missed appointment odds (OR 0.63, 95% CI 0.48–0.83) | **HIGH** |
| Chaiyachati RCT 2018 (JAMA IM) | Universal untargeted rideshare: NO reduction | **HIGH — counterpoint** |
| Balasubramanian 2025 (JAMA Network Open) | 30-day follow-up: 32% readmission reduction (RRR 0.68, 83 studies) | **MODERATE** |
| Berkowitz 2025 (J Primary Care) | Transport barrier removal: −0.09% HbA1c (n=86,977, TMLE) | LOW magnitude |
| Berkowitz ACO 2022 (Health Affairs) | NEMT alone not cost-saving; +9.2 outpatient visits, no admission/ED reduction | **Critical caveat** |
| NSI 2025 | Average RN turnover cost: $61,110 | HIGH |
| ASPE/HHS 2024 | Only 17.9% of eligible Medicare patients receive TCM | HIGH |

**Central thesis:** NEMT is a necessary *enabler* within multi-component care models (CCM, TCM, CHW), not a standalone intervention. The evidence for appointment adherence is robust (HIGH). Evidence for direct clinical outcomes is real but modest. Evidence for cost savings requires concurrent care management investment.

---

## Legal Framework

**AKS Safe Harbor** (42 CFR §1001.952(bb)): All 8 conditions must be met. Key points:
- Distance limits: ≤25 miles urban / ≤75 miles rural
- **No distance limit for discharge-to-home transport** (2020 amendment)
- Uber Health and Lyft Healthcare explicitly permitted
- No public advertising; established patients only

**Patient Engagement Safe Harbor** (42 CFR §1001.952(hh)): $500/patient/year cap for VBE participants

**MA Post-VBID (2026):** VBID Model terminated end of 2025. Transport as primarily health-related supplemental benefit (§422.102) or SSBCI for chronically ill (§422.102(f)). 24% of MA plans / 67% of SNPs offer transport in 2026.

**CRA 2023 Final Rule:** Healthcare transportation not explicitly listed on OCC Illustrative List — examiner discretion. Mitigate with: HRSA designation + CHNA citation + LMI income documentation chain.

**IRS Schedule H:** Transportation programs → Part I Line 7e (CHIS) with Z75.3 documentation and health outcome evidence. Without evidence, defaults to Part II — does NOT count toward community benefit total.

---

## Compliance Dimensions Explained

### NCQA / HEDIS
Moving CBP (Controlling High Blood Pressure) and CDC-HbA1c from 3★ to 4★ is worth an estimated **$1.8M–$3.2M in MA bonus revenue** for a 10,000-member plan. NCQA Health Equity Accreditation (launched 2023) requires SDOH data collection and stratified quality measurement — NEMT programs with Z75.3 documentation directly satisfy the referral pathway requirements.

### ACO REACH PY2026
5% quality withhold (up from 2%) — **$200K–$500K at stake for the median ACO**. TFU (Timely Follow-Up after acute exacerbation) is the most directly NEMT-sensitive measure. ACR (All-Condition Readmission) connects via Balasubramanian 2025. UAMCC (Unplanned Admissions for MCC) driven by chronic disease management gaps that NEMT enables to close.

### JC Community Care Certification (2024)
New Joint Commission certification specifically for organizations providing SDOH navigation and community-clinical linkages. NEMT programs with care coordination components directly qualify.

### Schedule H Parity
The parity model: hospital tax exemption (federal + property + bond savings) must be proportional to documented community benefit. The **parity gap** is what the scoring engine helps close — identifying which programs generate the most Part I CB credit per dollar invested while simultaneously satisfying other mandates.

---

## Technical Notes

- All files are self-contained single-file HTML (no build step, no dependencies, no backend)
- Real data from: Census Bureau ACS 5-Year Estimates API, CDC PLACES 2024, HRSA Data Warehouse (via Claude web search), FFIEC CRA Performance Evaluations (via Claude web search)
- Claude Sonnet API used for: CHNA/CRA document parsing, health system discovery, HRSA/CHR data search, AI strategic analysis, board brief generation
- XLSX export uses SheetJS (cdn.jsdelivr.net/npm/xlsx) — runs fully in browser
- No server required — all files can be served from static hosting or run locally

---

## Roadmap (Beyond MVP)

1. **EHR integration** — Pull actual HEDIS measure scores and no-show rates via FHIR API
2. **Grant database integration** — Connect to Foundation Directory Online / Candid for real-time funder search
3. **CHNA trend ML model** — Train on IRS 990 data (public) to predict which CHNA priorities are emerging nationally
4. **CRA assessment area overlap** — FFIEC geocoding API to confirm assessment area overlap before approaching bank funders
5. **NCQA measure projection** — Given NEMT program parameters, project specific HEDIS score improvement with confidence intervals
6. **Multi-hospital comparison** — Allow health systems to benchmark their CB parity gap against peer institutions

---

*Aqueduct v4.0 · Built on evidence. Bounded by evidence. The future of technology-enabled care.*
