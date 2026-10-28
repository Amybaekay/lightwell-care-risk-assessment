# Lightwell Care Group: Healthcare Risk Assessment

A GRC portfolio project: an end-to-end risk assessment for a fictional GP practice, covering a 31-risk register, 5x5 inherent and residual risk matrices, a costed treatment plan, key risk indicators (KRIs) and a risk owner report for a Risk Committee.

> **All organisations, people, figures and incidents in this project are fictional and simulated for portfolio purposes.** Regulatory and framework references (UK GDPR, CQC, DSPT, ISO 27001 and so on) are real. Costs are indicative estimates.

## Scenario

| | |
|---|---|
| **Organisation** | Lightwell Medical Centre (fictional), part of Lightwell Care Group |
| **Setting** | Single-site urban GP practice, Merseyside, England; high deprivation index |
| **Size** | 18,640 registered patients; 74 staff (58.6 WTE); £6.4m annual income |
| **Services** | General practice, minor surgery, vaccinations, diagnostics, in-house pharmacy support, urgent same-day clinic |
| **Systems** | Supplier-hosted EPR, on-site server room, NHSmail, online consultation tool, AI scribe pilot (paused) |
| **Regulatory context** | CQC, UK GDPR / DPA 2018, DSPT (2 evidence items outstanding), DCB0129 / DCB0160 |
| **Role played** | GRC Analyst reporting to the Risk Committee (reporting date: 16 October 2026) |

## What's in this repo

| File | What it contains |
|---|---|
| [`lightwell-methodology.docx`](lightwell-methodology.docx) | Methodology and executive summary: scope, scoring approach, key findings, decisions required, ISO 27001 control mapping, cloud supplier assessment approach, limitations. **Start here.** |
| [`lightwell-risk-assessment.xlsx`](lightwell-risk-assessment.xlsx) | The working risk assessment workbook (sheets listed below). |

### Workbook sheets

| Sheet | Purpose |
|---|---|
| Organizational Profile | Scenario, assumptions, appetite statement and a guide to the workbook |
| Criteria | Likelihood and impact scales, rating bands, review frequencies, appetite threshold and reporting date. Scoring inputs live here, so changing them recalculates the whole workbook |
| Risk Register | 31 risks, each with cause/event/consequence, owner, inherent and residual scoring, existing controls, control effectiveness, appetite status, treatment option, regulatory reference and review dates |
| Risk Matrix | Inherent and residual 5x5 heat maps (counts), residual risk IDs by cell and a rating summary showing the effect of controls |
| Treatment | 26 treatment actions with owners, dates, estimated cost, % complete, target residual score, RAG status and success measures |
| KRI Data | 22 simulated key risk indicators (12 months to 30 Sep 2026) used to support likelihood scoring |
| Risk Owners | Directory of risk owners and reporting lines |
| Risk Owners report | Headline metrics, per-owner summary with analyst commentary and decisions requested, and a summary by risk category |

## Methodology

- **Scoring:** 5x5 likelihood x impact, with each risk scored twice. *Inherent* assumes no controls operate; *residual* takes account of the controls in place today (rated Strong, Adequate or Weak).
- **Rating bands:** Low (1-4), Medium (5-9), High (10-15), Critical (16-25), each with a review frequency and escalation route.
- **Impact** is judged against the worst credible dimension: patient safety, data protection, financial, operational, or regulatory and reputational.
- **Risk appetite:** low for patient safety, safeguarding and regulatory risk. A single threshold is applied: any residual score above 9 is outside appetite and must have a funded treatment action.
- **Treatment options:** Mitigate, Transfer, Avoid, Accept.
- **Frameworks:** ISO 31000 (risk management process) and ISO/IEC 27005 (information security risk), with outputs that support ISO 27001 clauses 6.1.2 and 6.1.3.

## Headline results

| Metric | Value |
|---|---|
| Risks on register | 31 |
| Critical + High before controls (inherent) | 27 (7 Critical) |
| Critical + High after controls (residual) | 9 (0 Critical) |
| Average score, inherent → residual | 13.5 → 8.5 |
| Risks outside appetite | 9, all with a treatment action |
| Treatment actions | 26 (1 overdue) |
| Indicative first-year treatment cost | £323,600 |
| KRIs breaching threshold | 21 of 22 |

### The nine risks outside appetite

| ID | Risk | Residual | Owner | Main treatment |
|---|---|---|---|---|
| R01 | Ransomware attack on clinical systems | 12 | Head of IT & Digital | Immutable backups and restore tests, phishing training, cyber insurance |
| R02 | Staff credential compromise via phishing | 12 | Head of IT & Digital | MFA on all systems, quarterly phishing simulations |
| R03 | Unsupported legacy imaging workstations | 12 | Head of IT & Digital | Replace or isolate on a segregated VLAN |
| R12 | Delayed review of test results | 10 | Clinical Director | Results-tracking dashboard and weekly audit sign-off |
| R16 | Failure to recognise a deteriorating patient or sepsis | 10 | Head of Nursing | NEWS2-based triage tool and simulation training |
| R18 | Missed or late safeguarding referral | 10 | Safeguarding Lead | Case audit and Level 3 refresher training |
| R19 | Clinical vacancies and burnout | 12 | HR Manager | Recruit 2 GPs and 1 ANP, retention programme |
| R27 | Fire safety non-compliance | 10 | Estates & Facilities Manager | Fire door remediation and reinstated drills |
| R31 | Poor access: long waits and high DNA rate | 12 | Practice Manager | Online triage, DNA reminders, capacity review |

**Two kinds of exposure.** Cyber and workforce risks are driven by likelihood and weak controls. Clinical safety, safeguarding and fire risks are driven by impact: likelihood is low, but the potential harm is severe, so they cannot simply be accepted.

### Decisions requested from the Risk Committee

1. Approve £38,000 to replace or isolate unsupported imaging workstations (R03).
2. Approve the c. £92,000 recruitment and retention programme (R19).
3. Release contractor capacity to close the overdue fire door remediation and reinstate quarterly drills (R27).
4. Confirm renewal of cyber and business-interruption insurance (R01).
5. Appoint a Clinical Safety Officer by 27 November and keep the AI scribe paused until the DPIA, processing agreement and safety case are signed off (R07, R23).

## Framework alignment

The methodology document maps cyber and information security risks to ISO 27001:2022 Annex A controls. A sample:

| Risk | Annex A controls |
|---|---|
| R01 Ransomware | A.8.13 Information backup; A.8.7 Protection against malware; A.5.30 ICT readiness for business continuity |
| R02 Credential compromise | A.8.5 Secure authentication; A.6.3 Awareness and training |
| R03 Legacy systems | A.8.8 Technical vulnerabilities; A.8.22 Segregation of networks |
| R04 Inappropriate record access | A.5.15 Access control; A.8.15 Logging; A.8.16 Monitoring activities |

The document also outlines how to assess the hosted EPR supplier using a cloud security lens: shared responsibility, assurance evidence (ISO 27001, SOC 2, DSPT, DTAC), the NCSC Cloud Security Principles, resilience (RTO/RPO) and data governance.

## Skills demonstrated

- Risk identification, scoring and prioritisation against a defined appetite
- Control effectiveness assessment and inherent vs residual analysis
- Risk treatment planning with owners, budgets, target scores and success measures
- KRI design and evidence-based scoring
- Governance reporting: owner-level reporting and decisions framed for a committee
- Mapping risks to ISO 27001, ISO 31000, ISO 27005, NCSC, UK GDPR, CQC and DSPT requirements
- Spreadsheet modelling with formula-driven scoring and rating bands

## Limitations and next steps

- All data is simulated. Scores are analyst judgements that would normally be validated with risk owners in workshops.
- The single appetite threshold of 9 is a simplification. The Criteria sheet includes a draft category-level appetite table (for example, stricter for clinical safety than for finance) as a basis for recalibrating.
- Next steps: re-score each risk when its action completes, test controls rather than rely on owner statements, replace simulated KRIs with live data, and reassess annually or after major change.

## Author

Amarachi N. | Cloud Security Engineer building a governance, risk and compliance portfolio.
