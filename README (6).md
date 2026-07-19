# NidhiManager

**AI-Powered Cash Flow Prediction & Risk Flagging Platform for Rural Micro Enterprises**

Built for the **NABARD Hackathon @ Global Fintech Fest 2026**

---

## Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Our Solution](#our-solution)
- [Key Features](#key-features)
- [Sector-Specific Risk Models](#sector-specific-risk-models)
- [System Architecture](#system-architecture)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Data & Privacy](#data--privacy)
- [Roadmap](#roadmap)
- [Value to NABARD](#value-to-nabard)
- [Team](#team)
- [License](#license)

---

## Overview

Millions of rural micro enterprises in India — Self-Help Groups (SHGs), Farmer Producer Organizations (FPOs), and individual entrepreneurs — lack formal credit histories, limiting their access to structured financial services. At the same time, the rapid adoption of digital payments (UPI), combined with market and climate data, has created a rich but underutilised data ecosystem reflecting real-time rural economic activity.

**NidhiManager** bridges this gap. It fuses financial records, UPI transaction proxies, market intelligence, and climate/seasonal data into a single predictive engine that forecasts cash flow 3–6 months ahead and flags financial risk early — giving both micro enterprises and field officers the ability to act *before* a liquidity crisis, not after.

---

## Problem Statement

> **AI-Driven Cash Flow Prediction & Risk Flagging System for Rural Micro Enterprises**
> — NABARD Hackathon @ GFF 2026

The current approach to monitoring the financial health of microenterprises is largely manual. There is no integrated, data-driven system that combines financial data with digital transaction signals, market intelligence, and external factors to predict future cash flows — so early warning signs of financial stress are often missed, leading to delayed interventions, liquidity issues, and increased credit risk.

---

## Our Solution

NidhiManager combines four data streams into one AI-driven forecasting and risk-flagging engine:

| Data Stream | Description |
|---|---|
| **Financial Records** | Savings, loans, repayments, balances |
| **UPI Transaction Proxies** | Digital payment trends and usage patterns |
| **Market Intelligence** | Commodity/crop prices, demand trends |
| **Climate & Seasonal Data** | Weather shocks, monsoon patterns, seasonal income cycles |

The output is delivered through **two role-based interfaces on one platform**:

- **Enterprise App View** — for SHGs, FPOs, and individual entrepreneurs
- **Field Officer Dashboard** — for bank/NABARD field staff monitoring a portfolio of enterprises

---

## Key Features

### For the Micro Enterprise
- Simple data entry for income, expenses, savings, and loans
- 3–6 month cash-flow forecast in plain language
- Early-warning risk alerts (e.g., seasonal dip, repayment stress)
- Actionable, corrective suggestions
- Offline-first — works in low-network conditions, syncs when connectivity returns

### For the Field Officer
- Risk-ranked list of all enterprises in their portfolio
- Detailed, drill-down enterprise profiles
- Cash-flow forecast view per enterprise
- Risk panel with clear visual early-warning signals
- Enables proactive intervention instead of reactive damage control

---

## Sector-Specific Risk Models

Rural livelihoods don't share a single risk profile, so NidhiManager weights each sector's model for the factors that actually drive its cash flow:

| Sector | Key Risk Drivers |
|---|---|
| Dairy | Milk price, monsoon, fodder cost |
| Poultry | Feed cost, demand seasonality |
| Food Processing | Raw material price, demand cycles |
| Handicrafts | Festival demand, tourism inflow |
| Rural Retail | Local market disruption, liquidity |

---

## System Architecture

```
[Data Inputs]
 ├─ Financial records (savings, loans, repayments) — mock dataset
 ├─ UPI transaction pattern proxies — simulated
 ├─ Market intelligence (commodity/crop prices, demand trends)
 └─ Climate & seasonal data (weather, monsoon patterns)
        │
        ▼
[Spring Boot API Layer — Data Ingestion & Normalization]
        │
        ▼
[Sector-Specific Feature Engineering]
  (dairy / poultry / food processing / handicrafts / rural retail)
        │
        ▼
[AI/ML Core]
 ├─ Cash-Flow Forecast Model (3–6 month horizon)
 └─ Risk Classification Model (early warning scoring)
        │
        ├──────────────────────┬───────────────────────┐
        ▼                                              ▼
[Enterprise App View]                       [Field Officer Dashboard]
 (Flutter / React Native)                    (Flutter / React Native)
        │                                              │
        └──────────────────────┬───────────────────────┘
                                ▼
                 [JWT + OAuth Access Control Layer]
                                │
                                ▼
                  [PostgreSQL — persistent storage]
                                │
                                ▼
                [Offline-first Local Cache + Sync]
       (on-device storage, periodic low-bandwidth sync to
                  Render / Railway / AWS backend)
```

---

## Tech Stack

| Layer | Technology | Why |
|---|---|---|
| **Frontend** | Flutter (or React Native) | Single cross-platform codebase for enterprise & field-officer apps; offline-first support |
| **Backend** | Spring Boot (Java) | Mature, strongly-typed REST API layer; integrates well with banking/NBFC systems |
| **Database** | PostgreSQL | Relational storage for financial records, profiles, and forecast history |
| **AI/ML Layer** | Time-series forecasting (Prophet/LSTM) + gradient-boosted classifier (XGBoost/LightGBM) | Cash-flow prediction + risk classification |
| **Authentication** | JWT + OAuth | Secure, stateless, role-based access for enterprises vs. field officers |
| **Hosting** | Render / Railway / AWS (free tier) | Cost-efficient deployment for prototype and pilot stage |

---

## Project Structure

```
nidhimanager/
├── mobile-app/              # Flutter / React Native frontend
│   ├── enterprise/          # Enterprise-facing screens
│   └── field-officer/       # Field officer dashboard screens
├── backend/                 # Spring Boot application
│   ├── src/main/java/       # Controllers, services, repositories
│   └── src/main/resources/  # application.yml, config
├── ml-models/                # Forecasting & risk classification models
│   ├── cashflow-forecast/
│   └── risk-classifier/
├── data/                     # Mock/simulated datasets
├── docs/                     # Architecture diagrams, submission materials
└── README.md
```

> **Note:** This structure reflects the planned layout for the prototype phase. Folders will be populated as development progresses through the hackathon timeline.

---

## Getting Started

> This section will be completed as the prototype is built out during the Prototype Development Period (25 July – 15 Aug 2026).

### Prerequisites
- Flutter SDK or Node.js (for React Native)
- Java 17+ and Maven/Gradle
- PostgreSQL 14+

### Setup (planned)
```bash
# Clone the repository
git clone https://github.com/<your-org>/nidhimanager.git
cd nidhimanager

# Backend
cd backend
./mvnw spring-boot:run

# Frontend
cd ../mobile-app
flutter pub get
flutter run
```

---

## Data & Privacy

- The prototype uses **mock/simulated datasets** for financial records and UPI transaction proxies — no real user financial data is accessed or stored.
- UPI/transaction signals are used as **aggregated behavioural patterns**, not raw, personally identifiable account data.
- Designed to work **offline / in low-network conditions**, syncing only when connectivity allows.

---

## Roadmap

- [x] Idea submission & architecture design
- [ ] Prototype: Enterprise app (Flutter/React Native)
- [ ] Prototype: Field officer dashboard
- [ ] Cash-flow forecasting model (v1)
- [ ] Risk classification model (v1)
- [ ] Sector-specific model weighting (dairy, poultry, food processing, handicrafts, retail)
- [ ] Multilingual support (Hindi + regional languages)
- [ ] Pilot deployment with a partner bank/RRB/MFI

---

## Value to NABARD

1. **Enhanced Credit Flow** — reliable forecasts and risk profiles strengthen bank credit appraisal for underserved rural enterprises.
2. **Credit-Led Rural Development** — enterprises build a verifiable repayment track record, shifting from grant dependency to formal credit.
3. **Digital Public Good** — a common infrastructure layer for enterprise profiling, cash-flow assessment, and risk monitoring.
4. **Better Beneficiary Outcomes** — actionable, plain-language insights placed directly in the hands of rural entrepreneurs and field officers.

---

## Team

| Name | Role | Organization |
|---|---|---|
| _Your Name_ | _Role_ | _Organization_ |
| _Teammate_ | _Role_ | _Organization_ |
| _Teammate_ | _Role_ | _Organization_ |

---

## License

This project is submitted as part of the NABARD Hackathon @ Global Fintech Fest 2026. License to be finalized post-hackathon.

---

<p align="center">
  <i>NidhiManager — predictive, proactive, and built for the field.</i>
</p>
