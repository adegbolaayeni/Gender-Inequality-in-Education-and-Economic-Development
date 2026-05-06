# Gender-Inequality-in-Education-and-Economic-Development
> **Economics Research | Econometrics | Education Policy | Human Capital | Nigeria**
 
---
 
## 🔍 Overview
 
This repository contains the full B.Sc.(Ed.) Economics research project submitted in partial fulfilment of the requirements for the award of **Bachelor of Science Education in Economics** at Ekiti State University (EKSU), Ado-Ekiti, in affiliation with Emmanuel Alayande University of Education, Oyo.
 
The study provides a **43-year empirical analysis (1981–2024)** of how gender inequality in education impacts economic development in Nigeria, using an **Autoregressive Distributed Lag (ARDL)** econometric framework.
 
---
 
## 📋 Abstract
 
This research examines the macroeconomic consequences of educational gender disparities in Nigeria using time-series econometrics. Key findings reveal a significant short-run negative effect of gender parity improvements on GDP per capita — interpreted as a transitional human capital investment cost — alongside confirmed long-run cointegration that signals lasting positive returns to gender-equitable education.
 
**Period Covered:** 1981–2024 (43 years)  
**Estimation Method:** ARDL with Bounds Test for Cointegration  
**Data Sources:** CBN Statistical Bulletin, World Development Indicators (WDI), NBS
 
**Key Findings:**
- ARDL Bounds Test confirms a **statistically significant long-run cointegrating relationship** (F = 4.502, exceeds upper bounds at all significance levels)
- Current GPI has a **large, significant negative short-run effect** on GDP per capita (β = −43.22, p = 0.005) — interpreted as transitional investment cost, not evidence against gender equality
- Current **female unemployment significantly reduces GDP per capita** (β = −4.69, p = 0.021)
- Model explains **53.5% of variance** in GDP per capita (R² = 0.535)
- **Government education expenditure is economically insignificant** — signals resource misallocation
---
 
## 🧮 Econometric Methodology
 
### Variables
 
| Variable | Code | Definition | Source |
|---|---|---|---|
| GDP Per Capita Growth | `PC` | Annual % growth of GDP per capita | WDI |
| Gender Parity Index | `GPI` | Gross enrollment ratio (primary + secondary) | WDI / UIS |
| Labour Force Participation | `LFP` | Female-to-male LFP ratio | WDI |
| Female Literacy Rate | `FLR` | % female adult literacy | NBS / WDI |
| Male Literacy Rate | `MLR` | % male adult literacy | NBS / WDI |
| Govt. Expenditure on Education | `GEE` | % of GDP | CBN / WDI |
| Female Unemployment | `UEMF` | % female unemployment rate | NBS / WDI |
 
### Model Equation
 
```
PCt = β₀ + β₁GPIt + β₂LFPt + β₃FLRt + β₄MLRt + β₅GEEt + β₆UEMFt + ε
```
 
### Estimation Pipeline
 
```
1. ADF Unit Root Tests  →  Mixed I(0)/I(1) results
         ↓
2. Select ARDL (flexible; handles mixed integration orders)
         ↓
3. ARDL Bounds Test  →  Confirm long-run cointegration
         ↓
4. ARDL Short-Run Estimation  →  Coefficient interpretation
         ↓
5. Diagnostic Tests  →  Heteroskedasticity + Serial Correlation
         ↓
6. Discussion & Policy Recommendations
```
 
---
 
## 📊 Key Results
 
### Unit Root Test (ADF)
 
| Variable | Level (prob.) | 1st Diff. (prob.) | Order |
|---|---|---|---|
| PC (GDP per capita) | **0.0203*** | — | I(0) |
| GPI | 0.0680 | **0.0000*** | I(1) |
| LFP | 0.0002 | 0.0000 | I(1) |
| FLR | **0.0051*** | — | I(0) |
| MLR | 0.8615 | **0.0001*** | I(1) |
| GEE | 0.8874 | **0.0026*** | I(1) |
| UEMF | **0.049*** | — | I(0) |
 
> Mixed I(0)/I(1) → ARDL selected over Johansen cointegration
 
### ARDL Bounds Test
 
| F-Statistic | 5% Lower I(0) | 5% Upper I(1) | Decision |
|---|---|---|---|
| **4.502** | 2.45 | 3.61 | ✅ **Reject H₀ — Cointegration Confirmed** |
 
### ARDL Estimation Summary
 
| Variable | Coefficient | p-value | Interpretation |
|---|---|---|---|
| PC(-1) | +0.3997 | 0.0043** | Strong GDP persistence |
| **GPI (current)** | **−43.22** | **0.0051*** | Short-run transitional cost of enrollment parity |
| GPI(-1) | +24.47 | 0.0737† | Partial reversal — early returns emerge |
| LFP | +57.48 | 0.3941 | Positive direction, quality of employment matters |
| FLR | +0.11 | 0.6813 | Positive, not yet statistically significant |
| MLR | −0.32 | 0.4657 | Negative, insignificant |
| GEE | −0.15 | 0.8417 | ⚠️ Spending not generating returns |
| **UEMF (current)** | **−4.69** | **0.0209*** | Immediate cost of female exclusion |
| UEMF(-1) | +9.60 | 0.0053** | Cyclical adjustment |
| UEMF(-2) | −11.14 | 0.0117* | Volatility in female employment |
| UEMF(-3) | +7.22 | 0.0059** | Recovery phase |
 
| Model Statistic | Value |
|---|---|
| R-squared | 0.535 |
| Adjusted R-squared | 0.358 |
| F-statistic (overall) | 3.029 (p = 0.008) |
| Durbin-Watson | 2.027 |
| Heteroskedasticity (BPG) | p = 0.213 ✅ |
| Serial Correlation (BG) | p = 0.853 ✅ |
 
---
 
## 🌱 The Short-Run Cost / Long-Run Gain Framework
 
The negative short-run GPI coefficient is the **central finding** and its correct interpretation is critical:
 
```
Year 0:  Girls enter school
         → Diverted from informal household production
         → GDP per capita declines temporarily          ← What this study measures
 
Years 3–10+: Educated women enter labour market
         → Higher wages, productivity, innovation
         → GDP per capita rises                         ← What the Bounds Test confirms
```
 
> **"Think of it like planting a fruit tree. In year one, you spend money on the seedling
> and get no harvest. But in year three, the tree starts bearing fruit year after year."**
 
---
 
## ⚠️ Key Policy Concerns
 
| Issue | Evidence |
|---|---|
| 🏫 Low education spending returns | GEE coefficient: negative & insignificant |
| 👩‍💼 Female labour market exclusion | UEMF: significant negative effect on GDP |
| 📚 Education-employment mismatch | High GPI + persistent female unemployment |
| 🏘️ Regional disparities | Northern Nigeria disproportionately affected |
| 💰 Funding inefficiency | Public spending without accountability mechanisms |
 
---
 
## ✅ Policy Recommendations
 
1. **Enforce Gender Education Policies** — Rigorous implementation of UBE and National Gender Policy in rural and northern regions
2. **Expand Financial Support** — Scholarships, conditional cash transfers, and school feeding for low-income girls
3. **Invest in Infrastructure** — Gender-segregated facilities, safe transport, anti-harassment policies
4. **Reform Curricula** — Gender-neutral STEM content and teacher training to eliminate stereotype reinforcement
5. **Address Labour Market Barriers** — Equal opportunity enforcement, entrepreneurship grants, childcare support
6. **Awareness Campaigns** — Community-level communication of economic returns to educating girls
7. **Reform Education Spending** — Tie budgets to measurable gender-disaggregated outcomes with public reporting
8. **Strengthen Data Systems** — Track enrollment, completion, and employment by gender for evidence-based policy
---
 
## 📁 Repository Structure
 
```
📦 gender-inequality-education-economic-development-nigeria
├── 📄 README.md                          ← This file
├── 📄 journal_article.docx               ← Full peer-reviewed journal article
├── 📄 full_project_report.docx           ← Original B.Sc.(Ed.) project report
├── 📊 data/
│   └── panel_data_1981_2024.xlsx         ← Raw dataset (PC, GPI, LFP, FLR, MLR, GEE, UEMF)
└── 📈 outputs/
    ├── unit_root_tests.txt               ← ADF test results (EViews output)
    ├── ardl_bounds_test.txt              ← Bounds test output
    └── ardl_estimates.txt               ← Short-run ARDL estimates
```
 
---
 
## 🧭 Theoretical Foundations
 
| Theory | Key Scholars | Application |
|---|---|---|
| Human Capital Theory | Schultz (1961), Becker (1993) | Education raises productivity and wages |
| Endogenous Growth Theory | Romer (1990), Lucas (1988) | Human capital drives long-run innovation & growth |
| Feminist Economics | Folbre (1994), Sen (1999) | Gender biases embedded in economic institutions |
| Institutional Theory | Acemoglu & Robinson (2012) | Formal and informal institutions sustain gender gaps |
| Gender Equity Theory | Various | Fairness in resource distribution achieves equal outcomes |
 
---
 
## 🌍 Related Empirical Studies
 
| Study | Country/Region | Method | Finding |
|---|---|---|---|
| Klasen & Lamanna (2009) | 139 countries | Panel | Gender gaps reduce growth significantly |
| Onogwu (2021) | 29 Sub-Saharan Africa | Panel regression | GII negatively impacts GDP per capita |
| Adeleke et al. (2024) | Nigeria (1991–2022) | ARDL | Negative long-run, positive short-run |
| Lawanson & Umar (2019) | Nigeria (1980–2018) | ARDL | Gender inequality harms inclusive growth |
| Wang et al. (2023) | 17 Sub-Saharan Africa | IV-GMM | Gender parity boosts economic growth |
| Nnoje (2024) | Nigeria (2009–2023) | Granger Causality | Bi-directional causality established |
 
---
 
## 📚 Citation
 
```
Ayeni, A. E. (2025). Impact of gender inequality in education on economic development
in Nigeria [B.Sc.(Ed.) Project, Ekiti State University / Emmanuel Alayande University
of Education]. Department of Economics Education.
```
 
**BibTeX:**
```bibtex
@thesis{ayeni2025gender,
  author    = {Ayeni, Adegbola Elijah},
  title     = {Impact of Gender Inequality in Education on Economic Development in Nigeria},
  school    = {Ekiti State University / Emmanuel Alayande University of Education},
  year      = {2025},
  type      = {B.Sc.(Ed.) Project},
  address   = {Ado-Ekiti, Nigeria}
}
```
 
---
 
## 🔖 Keywords
 
`Gender Inequality` · `Education Economics` · `Economic Development` · `ARDL Model` · `Cointegration` · `Human Capital` · `Nigeria` · `GDP Per Capita` · `Labour Force Participation` · `Female Literacy` · `Time Series Econometrics` · `Inclusive Growth`
 
---
 
*© 2025 Ayeni, Adegbola Elijah — Ekiti State University / Emmanuel Alayande University of Education*  
*Supervised by Dr. T.O. Ajiteru · Coordinator: Dr. Ajibade I.O.*
