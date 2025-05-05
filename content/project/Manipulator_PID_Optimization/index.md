---
title: Meta-Heuristic Optimization Algorithms Based PID Controller Design For A 5-DOF Robotic Manipulator
summary: "Smart Control for Precision in Robotic Manipulators"

authors: 
- "Adeleke Olorunnisola Oyeyemi, Olurotimi Dahunsi"

tags:
- Optimization
- Control systems
- Robotics
date: "2024-06-15T00:00:00Z"

# # Internal link to another page within the Hugo site
internal_link: "project/Manipulator_PID_Optimization/"


# Optional external URL for project (replaces project detail page).
# external_link: "https://github.com/prakharrathi25/artificial-intelligence-for-trading"



# Links to additional resources (like code, demo videos, etc.)
links:
#   - icon: "code"
#     icon_pack: "fas"  # Font Awesome solid icons
#     name: "Code"
#     url: "https://github.com/prakharrathi25/artificial-intelligence-for-trading"
    - icon: "video"
      icon_pack: "fas"  # Font Awesome solid icons
      name: "Demo Video"
      url: "https://drive.google.com/file/d/1E5r5m59TFC4LmfLXf8Gh0l05ZjntU4Tj/view?usp=sharing"
    - icon: "file-powerpoint"
      icon_pack: "fas"  # Font Awesome solid icons
      name: "Slide"
      url: "https://docs.google.com/presentation/d/1mNNV45HiQF2pO4W0JiaSBDtBOCeQccra/edit?usp=sharing&ouid=109917310000887207564&rtpof=true&sd=true"
    - icon: "file-alt"
      icon_pack: "fas"  # Font Awesome solid icons
      name: "Report"
      url: "https://drive.google.com/file/d/1mpWC0FfftLG1vrRwk7cRNyktjSL1tZR9/view?usp=sharing"

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
### Abstract
This research presents a comprehensive approach to the design and implementation of a Proportional Integral Derivative (PID) controller for a 5-degree-of-freedom (DOF) robotic manipulator, utilizing meta-heuristic optimization algorithms. The robotic arm, initially designed using SolidWorks, was translated into a Simscape model for simulation purposes. Two distinct optimization algorithms, the Genetic Algorithm (GA) and Ant Colony Optimization

(ACO), were employed to fine-tune the PID controller gains, aiming to enhance the system’s dynamic performance and stability. The optimized PID gains obtained from simulations were then applied to a physical prototype of the robotic manipulator, which was 3D printed based on the SolidWorks design. The coding and real-time implementation of the PID controllers were conducted using MATLAB.


### Problem statement
The optimization of the PID controller using Genetic Algorithms and Ant Colony Optimization aims to address the laborious nature of manual PID tuning method.

These evolutionary and swarm intelligence-based algorithms offer the potential to efficiently explore the vast parameter space, leading to improved controller performance, robustness, and adaptability. The primary challenge lies in achieving optimal

PID controller parameters for the 5 DOF robotic arm to ensure precise, responsive, and stable control. While current studies often utilize individual nature-inspired optimization algorithms for tuning PID controllers, there is a gap in the literature regarding a comprehensive comparison of the trade-offs and effectiveness of these algorithms specifically applied to a 5-DOF robotic manipulator. This study aims to fill this gap by providing a detailed comparative analysis, ultimately contributing to the development of more efficient and robust control strategies for robotic systems.

### Cost of implementation of both algorithms to PID control
![Convergence Plot for the algorithms](Convergence_plot.jpg)

Upon comparison, it was observed that the Genetic Algorithm (GA) exhibited faster convergence and ran more efficiently than the Ant Colony Optimization (ACO) algorithm.

### More details of the project and results (graphs) are documented in the report