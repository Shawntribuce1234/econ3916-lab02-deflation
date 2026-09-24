 Deflating Economic Data — Nominal vs. Real

  Objective

  Separate inflation from real economic growth by deflating nominal wage and consumer price data to a constant 2020 dollar baseline, revealing the fifty-year divergence between headline earnings growth and actual
  purchasing power.

  Methodology

  - Data sources: Federal Reserve Economic Data (FRED) — Consumer Price Index (CPIAUCSL), Average Hourly Earnings (AHETPI, 1964–2026), and The Economist's Big Mac Index (2000–2026)
  - Deflation framework: Built and applied a reusable deflate_series() function to convert nominal values to constant 2020 dollars using the formula: Real = (Nominal / CPI) × Base CPI
  - Time alignment: Used pandas .asof() to align semi-annual Big Mac prices with monthly CPI observations
  - Interactive exploration: Constructed a base-year slider widget to demonstrate that growth rates are invariant to base-year choice, while dollar levels scale proportionally

  Key Findings

  Average Hourly Earnings (1964–2026):
  - Nominal growth: $2.50 → $32.53 (1,201% increase)
  - Real growth (2020 $): $20.92 → $25.20 (only 20% increase)
  - Interpretation: Most headline wage growth was absorbed by inflation; real purchasing power barely budged
  
  US Big Mac Price (2000–2026):
  - Nominal change: +178%
  - Real change: +43%
  - CPI change: +95%
  - Verification: (1 + 178%) = (1 + 43%) × (1 + 95%) ✓
  
  The Vibecession: Workers received raises that looked substantial in dollar terms, but inflation eroded those gains faster than wages grew, leaving real purchasing power nearly flat for decades. In 2023, even as
  headline inflation cooled, consumers still felt worse off because the damage to real wages had already been done during the 2021–2022 spike.# econ3916-lab02-deflation
