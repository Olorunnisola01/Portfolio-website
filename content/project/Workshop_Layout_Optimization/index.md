---
title: Optimizing Machine Workshop Layout for Efficiency and Productivity
summary: "Facility layout design grounded in Systematic Layout Planning and the material-handling objective function, applied to the FUTA Central Workshop"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Manufacturing systems
- Facility planning
- Lean manufacturing

date: "2023-10-01T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Workshop_Layout_Optimization/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "file-pdf"
      icon_pack: "fas"
      name: "Full Report (PDF)"
      url: "/uploads/workshop_layout_report.pdf"

slides: ""
---
#### Report motivation

Machine workshop layout is often treated as a matter of taste, arranging
equipment wherever seems reasonable. This report, prepared for MEE 812 —
Design and Manufacturing of Machine Tools at the Federal University of
Technology, Akure, argues instead that layout is a design problem with a
well-developed quantitative literature, and applies that literature to a
real case study: the FUTA Central Workshop.

#### What the report covers

The report builds from lean manufacturing and 5S principles through to
Muther's Systematic Layout Planning methodology, the from-to chart, and the
material-handling objective function

Z = ΣΣ f₍ᵢⱼ₎ c₍ᵢⱼ₎ d₍ᵢⱼ₎,

the formal target that heuristic layout algorithms such as CRAFT and ALDEP
minimize by iteratively exchanging department locations. The five standard
layout archetypes — fixed, process/functional, line, cell, and combinational
— are each developed with their governing trade-offs and best-fit
industrial applications.

#### Case study and an honest limitation

The FUTA Central Workshop's nine equipment categories are laid out as a
zoned functional layout along a central supervision aisle: a storage and
hand-fitting zone near the entrance, general machining grouped by type, a
partitioned CNC cell kept separate from swarf and vibration, and the
workshop's noisiest, highest-vibration equipment placed as far from the CNC
cell as the floor plan allows. An earlier draft of this case study described
the layout as a line–process hybrid; that framing didn't hold up once
checked against what a line layout actually requires (a fixed sequence of
different operations, not multiple redundant machines of the same type), so
the report corrects it explicitly rather than leaving the mislabel in place.
The report is equally direct about what this layout is *not*: it is a
qualitative, closeness-rating-based design, not one validated against a
measured from-to chart or run through a CRAFT/ALDEP exchange procedure. That
distinction, and what it would take to close the gap, is discussed directly
rather than glossed over.

See the [full PDF report](/uploads/workshop_layout_report.pdf) for the
complete derivation, all figures, and the full reference list.
