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
