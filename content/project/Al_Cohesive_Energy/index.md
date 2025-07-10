---
title:  Aluminum cohesive energy study
summary: "Visual Odometry, Navigation, Localizing"

authors: 
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Materials
- Aluminum

date: "2024-06-15T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Al_Cohesive_Energy"


# Optional external URL for project (replaces project detail page).
# external_link: "https://github.com/prakharrathi25/artificial-intelligence-for-trading"



# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "code"
      icon_pack: "fas"  # Font Awesome solid icons
      url: "https://drive.google.com/drive/folders/1SGRvBx8J3-Smqv--bJg_boJMTZu36Kcc?usp=sharing"
#    - icon: "video"
#      icon_pack: "fas"  # Font Awesome solid icons
#      name: "Demo Videos"
#      url: "https://drive.google.com/file/d/1zL0PU_8tsCgWUMCGJDBJctH0ZzCXCyD-/view?usp=sharing"
#   - icon: "file-powerpoint"
#     icon_pack: "fas"  # Font Awesome solid icons
#     name: "Slides"
#     url: "https://slides.com/your-slides"
    - icon: "file-alt"
      icon_pack: "fas"  # Font Awesome solid icons
      name: "Results"
      url: "https://drive.google.com/drive/folders/1NPdUKb6E9W6L28HNPqg0xUNS-dsWOeIB?usp=sharing"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

This project investigates the cohesive energy of aluminum, a fundamental material property that reflects the energy required to disassemble a solid into isolated atoms. Cohesive energy provides insight into the stability, bonding strength, and mechanical behavior of metals at the atomic level.

Using Molecular Dynamics (MD) simulations with the LAMMPS software, the study models a bulk FCC (face-centered cubic) aluminum crystal and calculates its cohesive energy based on the Embedded Atom Method (EAM) potential. The simulation involves:

    Initializing a periodic aluminum lattice

    Relaxing the atomic system to its equilibrium state

    Computing the total potential energy per atom

The resulting cohesive energy is then compared to experimental and theoretical reference values to validate the simulation accuracy. This project is essential for understanding interatomic interactions in metals, and serves as a foundation for more advanced simulations, such as mechanical deformation, dislocation dynamics, or alloy studies involving aluminum.