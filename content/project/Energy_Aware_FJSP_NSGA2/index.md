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
    - icon: "file-pdf"
      icon_pack: "fas"
      name: "Documentation"
      url: "/uploads/energy_aware_fjsp_nsga2_documentation.pdf"

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
move that Pareto-dominates the current solution. The scheduler solves real
Brandimarte (1993) FJSP benchmark instances (`mk01`–`mk10`, parsed from the
standard Hurink `.fjs` format) rather than synthetic problem instances.
This project is a compact, independently implemented demonstration of the
approach described in Burmeister, Guericke, and Schryen (2024), *Flexible
Services and Manufacturing Journal* — see the
[GitHub README](https://github.com/Olorunnisola01/energy-aware-fjsp-nsga2#readme)
for the full citation list and an explicit account of what is simplified
relative to that paper (10 of the paper's 15 benchmark instances, no
exact-solver comparison, a simplified local-search operator).

#### Results

Running the algorithm for 800 generations on the `mk01` benchmark instance
(10 jobs, 6 machines, 55 operations) converges to a 15-point Pareto front
trading off a 42-minute minimum-makespan schedule (higher energy cost)
against an 88-minute schedule at the lowest energy cost found — a genuine,
non-trivial trade-off surfaced directly from real price data rather than
an assumed energy rate.

See the [GitHub repository](https://github.com/Olorunnisola01/energy-aware-fjsp-nsga2)
for the full implementation, convergence plots, and the resulting Gantt
chart, or the [full documentation PDF](/uploads/energy_aware_fjsp_nsga2_documentation.pdf)
for a complete write-up of the motivation, problem formulation,
methodology, data sources, results, and an explicit comparison against
Burmeister et al. (2024).
