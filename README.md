# India's Coal Dilemma — An Energy Security Simulator

A single-file, interactive tool for senior policy audiences. It shows why India
relies on coal and what moving off it costs, using sourced numbers.

## What it does

Drag capacity sliders to rebuild India's power fleet (coal, gas, nuclear, hydro,
solar, wind, storage) against a chosen peak demand, and watch a representative
**24-hour day** of supply get stacked against demand:

- **Cut coal and the evening peak fails first.** Solar output falls to zero at
  sunset, when demand peaks. Red shortfall bars mark unmet demand.
- **Demand is growing.** The demand slider follows CEA projections: 256 GW met in
  2026, 366 GW by 2031-32, 459 GW by 2035-36. Capacity must grow just to keep pace.
- **The cost of transition is shown.** A capital-cost panel prices every GW
  added beyond today's fleet at Indian benchmark costs (coal ₹8.34 cr/MW per CEA,
  solar ₹3.5 cr/MW, batteries ₹1.7 cr/MWh per Ministry of Power, plus a
  transmission adder), in ₹ lakh crore and USD, with context: % of the union
  budget, CEA's own ₹33.6 lakh crore plan figure, and the annual fossil-import bill.

Five presets frame the debate: *India today (2026)*, *CEA plan 2031-32*,
*CEA vision 2035-36*, the cautionary *"Just add solar"* (16 hrs/day of shortfall),
and *Coal phase-out 2036* (works — at ~₹95 lakh crore / ~$1.1 trillion).

## Validation

The model is calibrated to published figures. The
"India today" preset yields ~71% coal share, ~1,230 Mt CO₂/yr, ~₹4.3/kWh average
cost, ~1,790 BU/yr and a reliable 256 GW peak — all matching published 2025-26
figures. Its bottom-up cost of the CEA 2031-32 fleet (~₹29 lakh crore) lands
independently near CEA's own ₹33.6 lakh crore estimate, and its coal share of
generation for that fleet (~55%) matches the NEP's ~56% thermal projection.

Every externally sourced constant is cited in the in-page **"Assumptions & sources"** table
(CEA installed-capacity reports and the National Electricity Plan, PIB releases,
SECI auction results, Ministry of Power data, ICRA/CRISIL/Mercom/Ember analyses,
IEA and CEEW investment estimates).

## Numeric audit notes

The in-page totals distinguish **power capacity** (GW) from **storage energy**
(GWh). The modelled 2026 generation fleet sums to about 495 GW, while the cited
all-source installed grid total is about 514 GW because small categories outside
the simulator are not individually modelled. Similarly, the 2031-32 and 2035-36
presets keep CEA storage energy in GWh separate from generation capacity so the
capital-cost math does not accidentally add GWh to GW.

## How to run

Open `index.html` in any modern browser. No build, no install, no network, no
tracking. Everything (including the charts) is hand-rolled vanilla JS/canvas so it
can be emailed around or run on an air-gapped laptop.

## A note on the numbers

This is an hourly-dispatch **illustrative model, not a planning study**: one
representative day, fleet-average capacity factors, no inter-regional transfers or
demand response, storage dispatched as a peaker. Costs are overnight capital costs;
retired coal earns no credit (stranded assets and decommissioning are ignored, so
the true bill is higher). All assumptions live as named constants at the top of the
`<script>` block in `index.html` — tune them for your own briefing.
