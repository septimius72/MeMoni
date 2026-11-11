# MeMoni 🏛️

> **Plan your money, see your future, check in monthly.**  
> A private, client-side personal finance architect and FIRE simulator with zero bank logins.

[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)
[![Zero-Dependency](https://img.shields.io/badge/Stack-Vanilla%20JS%20%7C%20Tailwind-3e1a47.svg)](#architecture)
[![Privacy First](https://img.shields.io/badge/Privacy-100%25%20Local%20Storage-d4af37.svg)](#privacy-first-architecture)

---

## Overview

**MeMoni** is an upscale, privacy-first web application designed for intentional cash-flow allocation, real-time balance tracking, and long-term financial independence forecasting. 

Unlike conventional budgeting apps that mandate third-party bank credential syncing (e.g., Plaid, MX), MeMoni returns full control and privacy to the user. All financial computation and storage occur directly inside the client browser.

---

## ✨ Key Features

### 1. Zero-Based Cash Flow Allocation
- **Every Dollar Given a Job**: Dynamic budget engine measuring Inflow vs. Total Outflow in real-time.
- **Dynamic 4-Bucket Hierarchy**: 
  - 🏠 **Needs** (Housing, Groceries, Utilities, Healthcare)
  - 🍸 **Wants** (Dining, Travel, Subscriptions, Lifestyle)
  - 📈 **Savings & Investments** (Roth IRA, Brokerage, Emergency Buffer)
  - 💳 **Debt Elimination** (Student Loans, Auto Notes, Credit Facilities)
- Add, edit, or delete custom line items within any bucket on the fly.

### 2. Connected Cash-Flow Engine
- **Direct Account Mapping**: Link monthly **Savings** line items directly to Asset accounts to watch balances accumulate.
- **Principal Reduction**: Link monthly **Debt** line items directly to Liabilities to automatically track amortization and balance dissolution.

### 3. Continuous Multi-Month Rollover
- Navigate across months and years with auto-inheriting templates.
- Avoid repetitive month-to-month data entry—future months automatically populate with your active baseline.

### 4. 12-Month Annual Overview (Chart.js)
- **Stacked Cash Allocation Flow**: Visualizes allocation splits across the entire calendar year.
- **Rolling Net Worth Progression**: Area chart charting annualized trajectory based on current savings and paydown velocities.

### 5. Future Projections & FIRE Engine
- Interactive compound interest simulator with adjustable:
  - Starting Capital
  - Monthly Contribution
  - Expected Annual Return Rate (CAGR)
  - Time Horizon (5 to 40 Years)
  - Target FIRE / Independence Goal
  - Inflation Discounting Toggle (2.5% annualized)
- **Automatic Milestone Badges**: Calculates the exact calendar year when crossing critical thresholds ($100k, $250k, $500k, $1M, $2M, and Custom FIRE target).

### 6. Full Data Portability & Privacy
- **Instant JSON Export**: One-click manual backup saved directly to disk (`MeMoni-backup-[YYYY-MM-DD].json`).
- **One-Click Restore**: Load previous backups onto any device or browser with zero account registration.
- **Auto-Persistence**: Real-time synchronization to browser `localStorage`.

---

## 🎨 Design System & Aesthetic

MeMoni is styled with a bespoke **Dark Luxury** palette:

| Color Role | Hex Code | Purpose |
| :--- | :--- | :--- |
| **Obsidian Plum** | `#0B050D` / `#1F0D23` | Deep background layering & ambient glow |
| **Forest Green** | `#0E2B13` / `#235E1D` | Primary wealth accents & actionable elements |
| **Champagne Gold** | `#E6C568` / `#D4AF37` | Typography highlights, badges & brand insignia |
| **Soft Mint** | `#EDF9EB` / `#BFEAC8` | High-contrast readable typography & metrics |

Typography is typeset in **Outfit** (display headings) and **Plus Jakarta Sans** (interface and financial data).

---

## 🚀 Quick Start

### Option A: Open Directly in Any Browser
Because MeMoni is built as a self-contained single-page application, no build tools, Node runtime, or package managers are required.

1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/MeMoni.git
   ```
2. Navigate to the project directory:
   ```bash
   cd MeMoni
   ```
3. Open `index.html` in your preferred modern web browser (Chrome, Safari, Firefox, Edge).

### Option B: Host via GitHub Pages
1. Push this repository to GitHub.
2. Navigate to **Settings** > **Pages**.
3. Under **Build and deployment**, select `main` (or `master`) branch as the source and `/root` as the folder.
4. Click **Save**. Your MeMoni instance will be live on your custom `github.io` domain.

---

## 🛠️ Tech Stack & Dependencies

- **Markup & Layout**: Semantic HTML5 & [Tailwind CSS CDN](https://tailwindcss.com/)
- **Visualizations**: [Chart.js CDN (v4.4+)](https://www.chartjs.org/)
- **Typography**: [Google Fonts](https://fonts.google.com/) (`Outfit` & `Plus Jakarta Sans`)
- **Persistence**: Web Storage API (`localStorage`) & Web File/Blob APIs

---

## 🔒 Privacy-First Architecture

```text
[ Browser Window ]
       │
       ├── State Engine (Vanilla JS)
       │        │
       │        ├──> LocalStorage (Auto-saved locally)
       │        └──> JSON Export (Client-side download)
       │
       └── ZERO Network Requests (No tracking, no telemetry, no third-party APIs)
```

No financial credentials, numbers, or account balances ever leave your device.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
