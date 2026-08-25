# 🔋 Data-Driven Battery Management System for Li-ion Batteries

A machine-learning-based Battery Management System (BMS) for **State of Charge (SOC) estimation, State of Health (SOH) prediction, battery degradation analysis, and safety monitoring** using NASA Li-ion battery cycling data.

---

## 📌 Project Overview

Battery Management Systems are essential for monitoring battery performance, safety, and degradation. This project develops a **data-driven BMS** using real-world Li-ion battery cycling data from the NASA battery dataset.

The system combines:

- 🔋 SOC estimation using Coulomb counting
- ❤️ SOH calculation and prediction
- 📉 Battery capacity degradation analysis
- 🌡️ Temperature monitoring
- ⚡ Voltage safety monitoring
- 🤖 ML/DL model benchmarking
- 🧪 Cross-battery validation using an unseen battery

The models are trained using **B0005 and B0006** and evaluated on the unseen **B0018** battery to assess cross-battery generalization.

---

## 🎯 Objectives

- Develop a data-driven framework for Li-ion battery health monitoring.
- Estimate **State of Charge (SOC)** using current-time measurements.
- Calculate and predict **State of Health (SOH)** from battery capacity degradation.
- Monitor battery voltage and temperature for safety conditions.
- Compare multiple machine-learning and neural-network regression models.
- Evaluate model generalization on an **unseen battery**.

---

## 🗂️ Dataset

The project uses the **NASA Li-ion Battery Dataset**.

### Batteries Used

| Battery | Purpose |
|---|---|
| B0005 | Training |
| B0006 | Training |
| B0018 | Unseen testing |

### Data Types

**Charge data**
- Voltage
- Current
- Temperature
- Time
- Cycle

**Discharge data**
- Voltage
- Current
- Temperature
- Load measurements
- Time
- Capacity
- Cycle

---

## ⚙️ Methodology

```text
              NASA Li-ion Battery Data
                        │
                        ↓
              Data Preprocessing
                        │
              ┌─────────┴─────────┐
              ↓                   ↓
        Charge Profiles      Discharge Profiles
              │                   │
              ↓                   ↓
      Coulomb Counting       Feature Engineering
              │                   │
              ↓                   ↓
             SOC              SOH Calculation
                                  │
                                  ↓
                    ┌─────────────┴─────────────┐
                    ↓             ↓             ↓
               ML Models     Neural Network   Evaluation
                    │             │             │
                    └─────────────┴─────────────┘
                                  ↓
                        Unseen B0018 Testing
                                  │
                                  ↓
                     BMS Monitoring & Analysis
