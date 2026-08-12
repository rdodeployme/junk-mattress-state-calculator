# JUNK — Mattress Recycling State Setup Calculator

An interactive model for working out what it would cost to stand up a mattress collection
and recycling operation in a new state, and whether that state would actually make money.

**Live:** https://bigdigitalaus.github.io/junk-mattress-state-calculator/

Single self-contained HTML file. No build step, no dependencies, no server — open
`index.html` in any browser and it runs.

---

## What it models

Inputs are grouped by cost block so each part of the operation can be costed on its own:

| Block | Covers |
|---|---|
| **Volume** | Mattresses per month, working days, daily throughput |
| **Winning the work** | Contract/B2B share, cost per lead, lead→job conversion, mattresses per job, BD cost |
| **Vehicles & fleet** | Load capacity, hours per round, finance, rego and insurance, fuel, servicing, tolls |
| **People** | On-costs, productive hours, drivers, offsiders, dismantlers, supervisors, admin |
| **Warehouse & facility** | Rent (per month or per m²/yr), outgoings, utilities |
| **Plant & overhead** | Consumables, plant maintenance, insurance and compliance, admin and software |
| **Disposal & recovery** | Residual landfill disposal, outbound freight, steel and other material revenue |
| **Pricing & revenue** | Consumer price, contract price, stewardship or grant income |
| **Setup capital** | Bond, fit-out, vehicles, plant, licensing, launch, working capital buffer |

## What it outputs

- Monthly profit, cost per mattress, revenue per mattress, margin and margin %
- **Break-even volume**, found by re-running the whole model at every volume — so it
  respects step costs (the point where you have to add a truck or another dismantler)
  rather than assuming a straight line
- **Setup payback** in months
- A **team roster** showing every person on the payroll and how their month splits between
  the road, the yard, and paid-but-idle time
- A **Compare tab** for saving several states side by side, with the best figure on each
  line highlighted, plus export/import of saved scenarios as JSON

## Two levers worth knowing about

**Double-hatting.** Truck crew rarely spend a full month on the road. With it on, their
spare hours go to the dismantling line before any dedicated dismantler is hired.

**Rostered vs casual.** A rostered dismantler is paid for a full month whether the work is
there or not. On the default settings, switching dismantlers to casual takes monthly profit
from roughly $5.9k to $11.2k — a payroll decision, not a pricing one.

## Important

**The default figures are placeholders, not JUNK's verified numbers.** They exist so the
model runs out of the box. Anything marked in amber inside the tool needs confirming before
a decision is made on it. In particular, these differ materially between states:

- Landfill levy / residual disposal cost per mattress
- Industrial rent and outgoings for the precinct you'd actually take
- EPA and planning approval requirements (the timeline is the risk more than the cost)
- Local offtake for foam, timber and textiles — no local processor means that revenue is zero
- Achievable contract/B2B volume

The model shows a steady-state month. It does not show the ramp — the six to twelve months
of under-utilised fixed cost getting there. That's what the working capital buffer is for.

## Saved scenarios

Scenarios saved on the Compare tab live in the page only and are lost on refresh. Use
**Export saved states** to download them as JSON and **Import** to bring them back.

## Licence

Internal JUNK tool. All rights reserved.
