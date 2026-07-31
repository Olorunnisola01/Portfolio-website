---
title: The Brinell Hardness Test — A Foundational Indentation Method in Strength of Materials Engineering
summary: "Physically-grounded derivation and worked analysis of the Brinell hardness test, from Hertzian contact through Tabor's fully-plastic relation to a corrected governing equation"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Materials science
- Mechanical testing
- Strength of materials

date: "2023-08-01T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Brinell_Hardness_Test/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "file-pdf"
      icon_pack: "fas"
      name: "Full Report (PDF)"
      url: "/uploads/brinell_hardness_test_report.pdf"

slides: ""
---
#### Report motivation

Hardness testing is the most frequently performed mechanical test in industry,
run far more often than tensile testing precisely because it is fast,
non-destructive, and needs no machined coupon. The Brinell test is the oldest
indentation hardness method still in continuous industrial use, introduced by
Johan August Brinell in 1900. This report, prepared for MEE 813 — Applied
Manufacturing Engineering Methods at the Federal University of Technology,
Akure, develops the test from first principles rather than treating it as a
procedure to be followed.

#### What the report covers

The analysis moves from Hertzian elastic contact through Tabor's fully-plastic
indentation relation (H ≈ 3σ_y), showing that the Brinell hardness number is,
to a good approximation, three times the material's flow stress — the reason
the test can substitute for a tensile test when pulling a specimen to failure
is impractical. Meyer's law and the indentation size effect are then used to
explain why the standard specifies load, ball diameter, and dwell time
alongside every reported hardness number.

A significant correction is derived along the way: many introductory
treatments define the Brinell hardness number using the flat *projected*
indentation area, when the standard actually requires the curved
*spherical-cap* surface area. The two differ by 10–15% over the standard's
permitted diameter range — far larger than the test's stated repeatability —
so the report derives the correct governing equation from first geometric
principles and works a complete numerical example (187 HBW 10/3000/15,
estimated UTS ≈ 645 MPa) using it.

#### Structure

The report covers apparatus and indenter selection, the standardized ASTM
E10 / ISO 6506-1 procedure, sources of measurement error (surface
preparation, indentation spacing, dwell time, indenter condition, elastic
recovery), advantages and limitations relative to Vickers and Rockwell
testing, and representative industrial applications in aerospace, automotive,
and foundry work.

See the [full PDF report](/uploads/brinell_hardness_test_report.pdf) for the
complete derivation, all figures, and the full reference list.
