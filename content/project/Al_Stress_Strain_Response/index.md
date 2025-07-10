---
title:  Aluminium Uniaxial Tensile loading of Single Crystal Aluminum
summary: "Materials, Mechanical Properties, Aluminum, Tensile Loading"

authors: 
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Materials
- Mechanical Properties
- Aluminium

date: "2024-06-15T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Al_Stress_Strain_Response"


# Optional external URL for project (replaces project detail page).
# external_link: "https://github.com/prakharrathi25/artificial-intelligence-for-trading"



# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "code"
      icon_pack: "fas"  # Font Awesome solid icons
      url: "https://drive.google.com/drive/folders/1V4nXMW8gSiCV-o15jgvauVXdbGSkKmi7?usp=sharing"
    - icon: "video"
      icon_pack: "fas"  # Font Awesome solid icons
      name: "Demo Videos"
      url: "https://drive.google.com/drive/folders/1pO_rMprO16Jvr-K8EtS3rB3CPFxbtVnt?usp=sharing"
#   - icon: "file-powerpoint"
#     icon_pack: "fas"  # Font Awesome solid icons
#     name: "Slides"
#     url: "https://slides.com/your-slides"
    - icon: "file-alt"
      icon_pack: "fas"  # Font Awesome solid icons
      name: "Results"
      url: "https://drive.google.com/file/d/1RG-2-ViSPyXf5Gj3wnGKwZPlxqZkZK7C/view?usp=sharing"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

This project focuses on simulating the uniaxial tensile deformation of single crystal aluminum using Molecular Dynamics (MD) with LAMMPS. The goal is to study the material's mechanical response—specifically its stress-strain behavior, elastic properties, and the onset of plastic deformation at the atomic scale.

A single crystal aluminum structure with a face-centered cubic (FCC) lattice is generated and subjected to gradual tensile loading along a specific crystallographic direction (e.g., [100]). The simulation employs the Embedded Atom Method (EAM) potential to model interatomic interactions realistically. Key steps include:

    Constructing and equilibrating the aluminum crystal

    Applying strain incrementally under controlled temperature and pressure

    Calculating stress from the virial expression

    Recording stress-strain data for post-processing

The simulation provides insights into the elastic modulus, yield stress, and dislocation activities that govern plasticity. Results are visualized using tools like OVITO and analyzed to compare with theoretical predictions and experimental data. This project is crucial for understanding the deformation mechanisms of metals at the nanoscale, aiding in materials design and mechanical performance prediction.