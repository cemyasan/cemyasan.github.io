---
title: "Space Heroes: Hybrid-casual RPG"
excerpt: "Lead Developer for a mobile RPG. Built a custom Hexagon Level Editor and Region-Based Streaming system to handle open-world performance on low-end devices."
header:
  teaser: /assets/images/spaceheroes/space-heroes-icon.jpg
categories:
  - Portfolio
tags:
  - Unity
  - C#
  - Mobile
  - Hybrid-casual
---

## Project Overview
**Role:** Lead Developer & Architect
**Team Size:** 6 (Developers, Artists, Designers)
**Tech Stack:** Unity 2022, C#, Custom Editor Tools

*Space Heroes* is a casual team-building RPG featuring an open world, 20+ unique heroes, and complex enemy AI. As the Project Lead, I was responsible for the core architecture, specifically solving the challenge of rendering a large open world on mobile devices with strict memory constraints.

## Key Technical Challenges

### 1. Custom Hexagon Level Editor
The design team needed to iterate quickly on level layouts, but standard Unity scene placement was too slow and imprecise for our grid-based gameplay.
* **Solution:** I developed a custom **In-Editor Level Design Tool**.
* **Features:**
    * **Brush-based Painting:** Designers can "paint" biomes, props, and enemies directly onto the grid.
    * **Auto-Hierarchy:** The tool automatically sorts objects into the correct parent containers based on their region coordinates, keeping the scene hierarchy clean[cite: 47].
    * **Data Validation:** Prevented illegal object placement before runtime, reducing bugs.

### 2. Region-Based Streaming Architecture
Mobile memory limits made it impossible to keep the entire open world loaded at once.
* **Solution:** I implemented a **Region-Based Loading System**.
* **Implementation:** The world map is split into regions. The system tracks player position and dynamically loads/unloads regions (GameObjects and assets) in real-time.
* **Result:** Stabilized frame rates on low-end devices (iPhone 7 equivalent) by keeping active memory usage low, regardless of map size.

### 3. Dynamic NavMesh Baking
Since the world layout could change based on region streaming, standard static NavMesh baking was insufficient.
* **Solution:** Implemented a runtime NavMesh baking solution that updates navigation data dynamically as new chunks of the world are loaded.

## Media & Visuals
*(Placeholder for your Editor GIF)*
*Above: The Custom Level Editor in action, showing the brush-based biome painting system.*

## Outcome
The tooling allowed the design team to build levels 3x faster than manual placement. The optimization techniques ensured a smooth 60fps experience during the initial launch and subsequent 6 months of content updates.