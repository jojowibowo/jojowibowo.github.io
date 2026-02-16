---
marp: true
theme: lioncity-finai
paginate: true
footer: "Jojo Wibowo | RevoU DEEPP | Gold & Bitcoin Regime Analysis"
---

<!-- _class: title-slide -->

# Gold and Bitcoin as Inflation Hedges
## A Regime-Dependent Analysis for Singaporean Retail Investors

**Jojo Wibowo**  
RevoU – Data End-to-End Portfolio Project (DEEPP)

---

## Problem Statement & Objectives

**Problem**
- Retail investors face conflicting narratives about inflation hedges
- Static dashboards fail under regime shifts
- Bitcoin is often misclassified as “digital gold”

**Objective**
- Build an **interpretable, regime-based decision-support framework**

**Key Goals**
1. Normalize macro, inflation, and sentiment stress
2. Distinguish **macro-driven vs sentiment-driven regimes**
3. Use ML for **explanation, not prediction**
4. Deliver a **mobile-friendly dashboard**

---

## Methodology Overview

**Data Sources**
- **Assets:** Gold (SGD), Bitcoin (USD)
- **Macro:** Singapore CPI, SORA, USD/SGD, Fed Funds, DXY
- **Sentiment:** Crypto Fear & Greed Index

**Period**
- Weekly data, **2017–2025** (n ≈ 410)

**Approach**
- Log returns, Winsorization (1% / 99%)
- Lag features (1–4 weeks)
- Models: Random Forest, Logistic Regression, SARIMAX / VAR
- Time-series validation (no trading simulation)

---

## Key Findings — EDA & Correlations

**Gold**
- Near-zero correlation with Singapore inflation (r ≈ 0.02)
- Sensitive to FX and global macro stress  
**Insight:** Defensive, diversifying asset — *not* a CPI tracker

**Bitcoin**
- Strong correlation with sentiment (r ≈ 0.47)
- Weak / negative link to inflation  
**Insight:** Sentiment-conditional risk asset

**Visuals**
- Correlation heatmap
- Regime overlays (e.g., 2022 tightening cycle)

---

## Machine Learning Insights

**Feature Importance (Random Forest)**
- **Bitcoin:** Sentiment ≈ 47% of total importance
- **Gold:** FX + macro ≈ 54%

**Directional Classification**
- ~**62% accuracy** for Bitcoin direction  
- Baseline ≈ 52.5%

**Takeaway**
> ML confirms **regime dependence**  
> Sentiment drives Bitcoin; macro drives Gold

---

## Regime-Based Framework

**Shift in Question**
> From *“Is it a hedge?”*  
> to *“When is it a hedge?”*

**Regime Types**
1. **Macro Stress:** Inflation + tightening → Gold relevant
2. **Sentiment Positive:** Risk-on liquidity → Bitcoin tactical
3. **Crisis / Panic:** Capital preservation → Defensive stance

**KPIs**
- Gold Hedge Relevance (0–100)
- Bitcoin Tactical Score (0–100)
- Regime Confidence Score

---

## Dashboard Solution (The Product)

**Design**
- Mobile-first, single-screen layout

**Features**
- Traffic-light regime indicators
- Normalized scores (0–100)
- Plain-language “Why this matters” explanations

**Value Proposition**
- Bridges advanced analytics with **retail usability**
- Eliminates static “one-size-fits-all” hedge narratives

*(Insert dashboard mockup image here for live / Reveal version)*

---

## Recommendations & 2026 Scenarios

**For Retail Investors**
- **Gold:** Macro stabilizer during FX stress & uncertainty
- **Bitcoin:** Tactical exposure only in favorable sentiment regimes
- **Risk Management:** Avoid Bitcoin during extreme fear + tightening

**2026 Scenarios**
- **Stagflation:** High Gold relevance, low Bitcoin
- **Soft Landing:** Bitcoin tactical opportunity improves

---

## Conclusion & Future Work

**Conclusions**
- Gold ≠ direct inflation hedge  
- Bitcoin ≠ digital gold  
- **Regime-based logic > static allocation**

**Future Work**
- NLP-based sentiment (news & social media)
- Inflation nowcasting
- Portfolio-level integration
- Bitcoin on-chain indicators

**Final Message**
> Interpretation beats prediction  
> Context beats slogans
