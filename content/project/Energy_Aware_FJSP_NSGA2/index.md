---
title: Energy-Aware Flexible Job-Shop Scheduling via a Memetic NSGA-II
summary: "Bi-objective (makespan, energy cost) scheduling under real electricity prices, using NSGA-II with local-search refinement"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Optimization
- Operations Research
- Metaheuristics
- Scheduling
- Smart manufacturing

date: "2026-08-01T00:00:00Z"

# Internal link to another page within the Hugo site
internal_link: "project/Energy_Aware_FJSP_NSGA2/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "github"
      icon_pack: "fab"
      name: "Source code"
      url: "https://github.com/Olorunnisola01/energy-aware-fjsp-nsga2"

slides: ""
---
#### Project motivation

Manufacturing energy cost is no longer flat: as power grids incorporate
more intermittent renewable generation, electricity markets increasingly
price consumption in real time, and manufacturers who can shift flexible
production toward cheap-price windows reduce cost without new capital
investment. This project schedules a Flexible Job-Shop Scheduling Problem
(FJSP) instance to jointly minimise **makespan** and **energy cost**,
computing energy cost from a real day-ahead electricity price series
(Belgium, February 2022, ENTSO-E Transparency Platform) integrated over
each operation's exact processing window, rather than a flat per-machine
energy rate.

#### Method

The scheduler is a **memetic NSGA-II**: the multi-objective genetic
algorithm NSGA-II (Deb et al., 2002), augmented with a greedy local-search
refinement applied to every offspring each generation — alternating
between machine re-assignment and operation-sequencing moves, keeping any
move that Pareto-dominates the current solution. This project is a
compact, independently implemented demonstration of the approach described
in Burmeister, Guericke, and Schryen (2024), *Flexible Services and
Manufacturing Journal* — see the
[GitHub README](https://github.com/Olorunnisola01/energy-aware-fjsp-nsga2#readme)
for the full citation list and an explicit account of what is simplified
relative to that paper (random instances rather than the Brandimarte
benchmark suite, no exact-solver comparison, a simplified local-search
operator).

#### Results

Running the algorithm for 800 generations on a 15-job/4-machine instance
converges to an 18-point Pareto front trading off a 200-minute
minimum-makespan schedule (higher energy cost) against a 239-minute
schedule at the lowest energy cost found — a genuine, non-trivial
trade-off surfaced directly from real price data rather than an assumed
energy rate.

See the [GitHub repository](https://github.com/Olorunnisola01/energy-aware-fjsp-nsga2)
for the full implementation, convergence plots, and the resulting Gantt
chart.
