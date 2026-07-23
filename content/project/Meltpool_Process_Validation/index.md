---
title: Melt-Pool Process Maps and Literature Validation
summary: "Power-velocity process maps across four L-PBF alloys, and a quantitative validation of the Rosenthal calculator against published single-track measurements"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Additive manufacturing
- Process modelling

date: "2026-07-22T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Meltpool_Process_Validation/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "github"
      icon_pack: "fab"
      name: "Source code"
      url: "https://github.com/Olorunnisola01/rosenthal-meltpool"
    - icon: "file-pdf"
      icon_pack: "fas"
      name: "Documentation"
      url: "https://github.com/Olorunnisola01/rosenthal-meltpool/blob/main/docs/project2_documentation.pdf"

slides: ""
---
#### Project motivation

This project extends the [Rosenthal melt-pool calculator](/project/rosenthal_meltpool_calculator/) from a single-point tool into a swept process-mapping tool, and then asks the harder question: does it actually match reality? It sweeps the calculator across a full laser power x scan velocity grid for all four preset L-PBF alloys, and validates its predictions against a real published single-track dataset rather than only comparing parameters against each other.

#### Process maps

Sweeping power (50-400 W) and velocity (200-2000 mm/s) at fixed absorptivity produces width, depth, and aspect-ratio maps for each alloy. The two materials below, swept at identical ranges, land on entirely different absolute scales (316L peaks near 220 µm width; AlSi10Mg, roughly 5x more thermally conductive, peaks near 470 µm) — a direct confirmation that material choice, not just process parameters, sets melt-pool scale.

The aspect-ratio panel is flat at exactly 0.5 across the *entire* grid, for both materials — confirming a structural limitation identified in the base calculator (see its own project page) holds everywhere this model can be evaluated, not just at isolated points.

#### Literature validation

Predictions were checked against four published single-track cases for 316L stainless steel ([Zhang et al., 2024](https://doi.org/10.3390/mi15020170)), using the paper's own assumed absorptivity (0.5). The model underpredicts every case, by 7% to 74% depending on dimension. A calibration search — testing absorptivity values up to a deliberately unphysical 500% — shows this gap cannot be closed by absorptivity alone for three of the four cases: the predicted pool sizes (35-115 µm) are comparable to the paper's 100 µm laser spot diameter, which breaks the point-source model's core assumption that pool size must be much larger than source size.

Full methodology, tables, and figures are in the [documentation PDF](https://github.com/Olorunnisola01/rosenthal-meltpool/blob/main/docs/project2_documentation.pdf) and the [GitHub README](https://github.com/Olorunnisola01/rosenthal-meltpool#readme).
