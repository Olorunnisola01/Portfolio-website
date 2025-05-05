---
title: A case study on raw material management in a manufacturing industry using advanced nonlinear optimization technique(NLOT)
summary: "Optimizing raw materials using Heuristics and Exact method"

authors: 
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Optimization
- Smart manufacturing

date: "2024-06-15T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Raw_material_GA/"


# Optional external URL for project (replaces project detail page).
# external_link: "https://github.com/prakharrathi25/artificial-intelligence-for-trading"



# Links to additional resources (like code, demo videos, etc.)
links:
#   - icon: "code"
#     icon_pack: "fas"  # Font Awesome solid icons
#     name: "Code"
#     url: "https://github.com/prakharrathi25/artificial-intelligence-for-trading"
#   - icon: "video"
#     icon_pack: "fas"  # Font Awesome solid icons
#     name: "Demo Videos"
#     url: "https://youtube.com/your-demo-videos"
#   - icon: "file-powerpoint"
#     icon_pack: "fas"  # Font Awesome solid icons
#     name: "Slides"
#     url: "https://slides.com/your-slides"
  - icon: "file-alt"
    icon_pack: "fas"  # Font Awesome solid icons
    name: "Report"
    url: "https://drive.google.com/file/d/1XYgr8jkvWQt_Uu5RYNKcbxVaoO8xAa9f/view?usp=drive_link"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
This study focuses on Raw Material Inventory Optimization for Benmist Water Company in Akure, Nigeria. The goal is to minimize total costs related to raw material holding and ordering, considering demand, holding costs, and ordering costs over a specified time period. Decision variables include order quantity, with parameters like demand, holding cost, ordering cost, initial inventory, storage capacity, and time period.

To solve this optimization problem two algorithms are applied: Genetic Algorithm (GA) and Sequential Quadratic Programming with Linear Programming and Equality Constraints (SLPSQP). GA, inspired by evolution principles, iteratively refines solutions to find optimal order quantities while SLPSQP uses a mathematical programming approach, considering constraints.

Separate optimization runs with both algorithms are conducted, comparing their performance in terms of total cost minimization, convergence speed, computational efficiency, and solution quality. Results show that GA excels in exploring diverse solutions, while SLPSQP demonstrates precision with fewer iterations. The comparison provides insights into exploration-exploitation trade-offs.

This research contributes to inventory management by showcasing the applicability and performance of GA and SLPSQP in addressing real-world raw material optimization challenges for a water bottling company. The insights guide practitioners in selecting the most suitable algorithm based on specific optimization objectives and constraints.