---
title: Path Planning Algorithms for Robot Obstacle Avoidance
summary: "A*, Probabilistic Roadmap (PRM), and RRT motion planning, implemented and simulated in CoppeliaSim"

authors:
- "Adeleke Olorunnisola Oyeyemi"

tags:
- Robotics
- Motion Planning
- Algorithms

date: "2026-08-01T00:00:00Z"

# Internal link to another page within the Hugo site
internal_link: "project/Path_Planning_Algorithms/"

# Links to additional resources (like code, demo videos, etc.)
links:
    - icon: "github"
      icon_pack: "fab"
      name: "Source code"
      url: "https://github.com/Olorunnisola01/Path_planning"

slides: ""
---
#### Project overview

An implementation of three fundamental robot motion-planning algorithms
for obstacle avoidance, developed as part of the *Modern Robotics, Course
4: Robot Motion Planning and Control* curriculum and simulated in
CoppeliaSim:

- **A\*** — heuristic graph search combining Dijkstra's guaranteed
  shortest-path property with a distance-to-goal heuristic to search
  efficiently toward the goal rather than expanding uniformly in all
  directions.
- **Probabilistic Roadmap (PRM)** — builds a roadmap by randomly sampling
  collision-free configurations and connecting nearby samples, well suited
  to high-dimensional configuration spaces with many obstacles.
- **Rapidly-exploring Random Tree (RRT)** — incrementally grows a tree from
  the start configuration by repeatedly extending toward randomly sampled
  points, quickly covering large regions of the space to find a feasible
  (not necessarily shortest) path.

#### Implementation

Each algorithm is implemented in Python and evaluated in a shared obstacle
environment in CoppeliaSim, with the resulting roadmap/tree, computed path,
and obstacle layout logged to CSV (`nodes.csv`, `edges.csv`,
`obstacles.csv`, `path.csv`) for each run:

- `Astar_algorithm/` — A* search implementation and results.
- `PRM/` — Probabilistic Roadmap implementation and results.
- `RRT_algorithm/` — RRT implementation, pseudocode, and results.

See the [GitHub repository](https://github.com/Olorunnisola01/Path_planning)
for the full source code, per-algorithm results, and simulation
screenshots.

#### Educational value

Working through all three algorithms side by side highlights their
different trade-offs directly: A\*'s optimality guarantee versus its cost
in dense graphs, PRM's strength in high-dimensional spaces via random
sampling, and RRT's speed at covering large regions when a feasible (rather
than optimal) path is enough — core building blocks for autonomous
navigation systems in robotics.
