---
title: A Three-Objective Optimisation Framework for Circular Product Ecodesign
summary: "NSGA-III optimisation of Planet/Prosperity/People trade-offs for a real, cited product, built end to end on open data"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Optimization
- Circular Economy
- Life Cycle Assessment
- Metaheuristics
- Multi-objective Optimization
- Sustainability

date: "2026-08-06T00:00:00Z"

# Internal link to another page within the Hugo site
internal_link: "project/CircuOpt/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "github"
      icon_pack: "fab"
      name: "Source code"
      url: "https://github.com/Olorunnisola01/circuopt"
    - icon: "file-pdf"
      icon_pack: "fas"
      name: "Full report"
      url: "/uploads/circuopt_report.pdf"

slides: ""
---
#### Project motivation

Circular ecodesign stalls at the concept stage because designers cannot show
that circularity pays: deep circularity (design for disassembly,
remanufacturing, high-purity recycling) demands capital up front against
benefits distributed across a decade, split between actors, and exposed to
commodity and regulatory volatility. Existing eco-efficiency tools optimise
one variable at a time, hold the rest fixed, and evaluate only against
today's factors. This project builds a framework that answers the question
quantitatively, for a real product, under uncertainty.

The case product is the **GARO LS4** ground-mounted AC electric-vehicle
charging station. Its bill of materials, mass and technical lifetime are
taken from a published manufacturer LCA rather than invented, and every
result in the report is cross-checked against that independent, published
figure.

#### Method

Fourteen design variables — recycled content per material, joining method,
design lifetime, remanufacture cycles, end-of-life route, and standby power
class — are optimised simultaneously against three objectives: cradle-to-grave
carbon per service-year (**Planet**), annualised life-cycle cost
(**Prosperity**), and a composite repairability/modularity/circular-labour/
supply-risk index (**People**). A self-contained NSGA-III (NumPy only, no
external optimisation library) performs the search, benchmarked against
NSGA-II and random search with a Mann–Whitney U test and effect size, not
just a headline hypervolume number.

The inventory is Idemat 2026 (Delft University of Technology), a
process-level life-cycle database carrying global warming, cumulative energy
demand, and the EU's own Environmental Footprint 3.1 method — not a
single-indicator carbon-reporting factor. Commodity prices come from USGS
Mineral Commodity Summaries and World Bank commodity data. No licensed
database is used and no factor is invented.

Every methodological choice that could decide the answer is tested, not
assumed: impact category, end-of-life allocation convention (cut-off,
substitution, and the EU PEF's own Circular Footprint Formula), grid
geography across six European markets, social weighting, commodity price
source, and the weakest inventory proxy — each with a quantified sensitivity
result, not a caveat in a footnote.

#### Results

The optimiser recovers a several-hundred-design Pareto archive in which
*every* non-dominated design beats a linear take-make-waste baseline on
carbon **and** cost simultaneously — the central, industry-disputed claim,
now demonstrated rather than asserted. A Monte Carlo ensemble of hundreds of
plausible futures (grid decarbonisation, carbon pricing, commodity
volatility, an ESPR-style recycled-content mandate) then separates designs
that are merely optimal today from designs that stay good answers under
uncertainty.

The most striking finding is not about the product at all: purely
methodological choices — which grid region, which inventory backend —
routinely move the result more than the entire Pareto-optimal design space
does. That is reported as a finding in its own right, because a framework
that hid it to make its own headline number look cleaner would not be one
worth citing.

See the [GitHub repository](https://github.com/Olorunnisola01/circuopt) for
the full implementation, 127-test regression suite, and reproducible
experiment protocol, or the [full report PDF](/uploads/circuopt_report.pdf)
for the complete write-up: formulation, method, results, every sensitivity
analysis, and a stated account of what the model still cannot tell you.
