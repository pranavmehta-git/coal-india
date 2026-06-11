# India's Coal Dilemma — An Energy Security Simulator

A single-file, interactive demo for senior policy stakeholders to *feel* why India
leans so heavily on coal — and what it actually takes to move away from it without
the lights going out.

## What it does

Drag capacity sliders to rebuild India's power fleet (coal, gas, nuclear, hydro,
solar, wind, batteries) and watch a representative **24-hour day** of supply get
stacked against demand. The core insight is made visceral:

- **Cut coal, and the evening peak breaks first.** Solar collapses to zero at
  sunset — exactly when India's demand is highest. Red "shortfall" bars appear:
  these are blackouts.
- **Firm capacity and storage are the price of going clean.** Add nuclear, hydro,
  or batteries to carry the grid through sunset and the lights come back on — but
  watch the cost climb.
- Live KPIs track **coal share, hours of unmet demand, CO₂ emissions, average
  cost**, plus a daily generation-mix bar.

Four presets frame the debate: *India today*, *2030 NDC pathway*, *Coal
phase-down*, and the cautionary *"just add solar"*.

## How to run

Open `index.html` in any modern browser. That's it — no build, no install, no
network, no tracking. Everything (including the charts) is hand-rolled vanilla
JS/canvas so it can be emailed around or run on an air-gapped laptop.

## A note on the numbers

This is an **illustrative conversation tool, not a dispatch model**. Figures are
order-of-magnitude (peak demand ~245 GW, ~0.95 tCO₂/MWh for coal, indicative
₹/kWh costs, 4-hour batteries). Every assumption lives at the top of the `<script>`
block in `index.html` — open it and tune the constants for your own briefing.
