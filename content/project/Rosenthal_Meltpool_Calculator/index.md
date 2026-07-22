---
title: Rosenthal Melt-Pool Calculator for Laser Powder Bed Fusion
summary: "Interactive analytical prediction of single-track melt-pool geometry from laser power, scan speed, and material properties"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Additive manufacturing
- Process modelling

date: "2026-07-21T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Rosenthal_Meltpool_Calculator/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "github"
      icon_pack: "fab"
      name: "Source code"
      url: "https://github.com/Olorunnisola01/rosenthal-meltpool"
    - icon: "file-pdf"
      icon_pack: "fas"
      name: "Documentation"
      url: "https://github.com/Olorunnisola01/rosenthal-meltpool/blob/main/docs/project1_documentation.pdf"

slides: ""
---
#### Project motivation

Predicting single-track melt-pool geometry is the first, cheapest screening step
before committing to full process-parameter optimization in laser powder bed
fusion (L-PBF). This tool implements the Rosenthal (1946) moving point-heat-source
analytical solution to predict melt-pool width, depth, and length directly from
laser power, scan velocity, absorptivity, and preheat temperature, for four common
L-PBF alloys (Ti-6Al-4V, 316L, AlSi10Mg, Inconel 718).

The calculator below runs the exact same Python implementation available on
[GitHub](https://github.com/Olorunnisola01/rosenthal-meltpool) — a plain,
documented module with no GUI dependencies, wrapped here in an interactive
Streamlit front end.

<iframe
  src="https://rosenthal-meltpool.streamlit.app/?embed=true"
  height="900"
  style="width:100%; border:none;"
  title="Rosenthal Melt-Pool Calculator"
></iframe>

#### Validation against published data

Predictions were checked against a real single-track dataset
([Zhang et al., 2024](https://doi.org/10.3390/mi15020170), 316L stainless
steel). The model systematically underpredicts pool size at the paper's own
assumed absorptivity, and a calibration search shows this cannot be fixed by
absorptivity alone for most cases — the root cause is that predicted pool
sizes here are comparable to the real laser spot diameter, which breaks the
point-source model's core assumption.

#### Model limitations

This is a conduction-mode analytical model: it does not capture keyhole-mode
vaporization, recoil pressure, Marangoni convection, or temperature-dependent
material properties. A more fundamental limitation, confirmed while building
this tool rather than assumed in advance: the predicted depth-to-width ratio
is *always exactly 0.5*, for any material or parameters — a mathematical
identity of the point-source formula, not an approximation. The predicted
cross-section is therefore always a perfect semicircle, which real melt pools
(measured aspect ratios 0.49–1.58 in the validation data above) are not.

Treat this tool's output as a first-pass estimate for comparing process
parameters against each other, not a substitute for a validated thermal-fluid
simulation. See the [documentation PDF](https://github.com/Olorunnisola01/rosenthal-meltpool/blob/main/docs/project1_documentation.pdf)
or the [GitHub README](https://github.com/Olorunnisola01/rosenthal-meltpool#readme)
for the full analysis.
