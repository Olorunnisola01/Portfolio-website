---
title: "Meta-Heuristic Optimization of PID Controllers for a 5-DOF Robotic Manipulator"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- Adeleke Olorunnisola Oyeyemi
- Olurotimi Dahunsi

# Author notes (optional)
author_notes:
- "First Author"
- "Second Author"

# Schedule page publish date (NOT publication's date).
# publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: In *Computational Engineering and Physical Modeling*, vol. 8, no. 3, pp. 1-19
publication_short: In *CEPM*

date: "2025-07-01T00:00:00Z"

abstract: Accurate motion control is a critical requirement for robotic manipulators in advanced industrial and research applications. Proportional-Integral-Derivative (PID) controllers remain the preferred choice due to their simplicity and reliability, although their performance is highly dependent on effective gain tuning. Conventional tuning techniques are often inefficient and fail to deliver consistent results across complex robotic systems. This study investigates the application of metaheuristic optimization methods, specifically Genetic Algorithm (GA) and Ant Colony Optimization (ACO), for tuning PID controllers in a five-degree-of-freedom robotic manipulator. The manipulator was modeled in SolidWorks, simulated in Simscape, and integrated with MATLAB-based control. A sinusoidal trajectory was employed as the reference input, and performance was evaluated using Integral Time Absolute Error (ITAE) and overshoot metrics across all joints. The results show that both GA and ACO outperform manual tuning. GA reduced the average overshoot by approximately 51% and ACO by 61% compared with manual tuning, while the GA and ACO algorithms achieved fitness (ITAE) improvements of 0.36% and 0.04%, respectively. GA demonstrated faster convergence (within 10 generations), whereas ACO achieved more stable fitness reduction and superior trajectory tracking, indicating enhanced robustness. These findings suggest that while GA offers computational efficiency, ACO provides improved stability and accuracy, making it a more effective strategy for PID tuning in this system.

# Summary. An optional shortened abstract.
summary: "Genetic Algorithm and Ant Colony Optimization tuning of PID controllers for a 5-DOF robotic manipulator, modeled in SolidWorks/Simscape/MATLAB, cutting average overshoot by 51-61% relative to manual tuning."

tags:
- Robotics
- Control systems
- Optimization

# Display this page in the Featured widget?
featured: false


links:
    - icon: "file-alt"
      icon_pack: "fas"
      name: "Paper"
      url: "https://www.jcepm.com/article_235487_190b044c5cf63542fa06a9e7fcecdbf9.pdf"
    - icon: "link"
      icon_pack: "fas"
      name: "DOI"
      url: "https://doi.org/10.22115/cepm.2025.544303.1383"

# Custom links (uncomment lines below)


# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- Manipulator_PID_Optimization


# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
