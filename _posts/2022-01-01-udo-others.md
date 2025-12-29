---
title: "Rapid Production Archive (2022-2023) - Hyper and Hybrid-casual Games"
excerpt: "A collection of hyper-casual and hybrid-casual titles where I served as the sole developer. Focus on rapid prototyping, mechanical variety, and data-driven iteration."
header:
  teaser: /assets/images/hyper-archive/teaser.jpg
categories:
  - Portfolio
tags:
  - Unity
  - C#
  - Hyper-casual
  - Hybrid-casual
  - Rapid Prototyping
  - Mobile
  - Optimization
---

> This page archives selected projects developed at **Udo Games** where I owned the full technical pipeline—from initial concept to store release. These projects typically operated on tight production cycles, requiring robust code architecture that could be discarded or scaled based on data.

---

# Udo Games (2022–2023)

During this period, I focused on **Hybrid-Casual** development, utilizing my full-stack background to own the entire technical pipeline—from ideation to release. We focused on higher complexity mechanics than standard hyper-casual games, incorporating idle economies, save systems, and puzzle logic.

---

## Moneymatic
**Role:** Sole Developer (with 1 Artist, 1 Designer)  
**Genre:** Automation Puzzle / Hyper-casual  
**Tech:** Grid Systems, Path Logic, Object Pooling

<video autoplay playsinline muted loop preload="metadata" width="100%">
  <source src="{{ '/assets/videos/archive/moneymatic-gameplay.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Moneymatic* is an automation-puzzle game centered on optimizing economic flow. The core objective is to transport coins from a source to a destination by strategically placing provided functional pieces, such as conveyor belts and modifiers.

### Key Technical Contributions
- **Grid & Path Logic:** Developed a deterministic grid system to handle the placement of directional pieces, ensuring coins followed complex, user-defined paths without logic breaks.
- **Automation Simulation:** Implemented a performant simulation loop that handled the movement, modification, and collection of hundreds of active coin entities simultaneously.
- **Puzzle Solvability:** Built validation tools to ensure that the randomly generated or designer-placed "provided pieces" always allowed for a valid solution path.

---

## Army Camp 3D
**Role:** Sole Developer (with 1 Artist, 1 Designer)  
**Genre:** Merge Defense / Hyper-casual Strategy  
**Tech:** Grid Logic, Wave Management, Object Pooling

<video autoplay playsinline muted loop preload="metadata" width="100%">
  <source src="{{ '/assets/videos/archive/armycamp-gameplay.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

*Army Camp 3D* is a merge-defense game where players construct a defensive line to withstand increasingly massive hordes of enemies. The gameplay focuses on resource management (buying units) and spatial puzzles (optimizing grid placement and merging units to upgrade tiers).

### Key Technical Contributions
- **Grid-Based Merge Architecture:** Developed a robust drag-and-drop grid system that handles valid placement logic and detects "merge" events when identical units are stacked, upgrading them to higher tiers in real-time.
- **Scalable Wave Spawner:** Engineered a wave management system capable of spawning and pathfinding hundreds of enemy units simultaneously, utilizing heavy object pooling to maintain 60 FPS on mobile devices.
- **Progression Systems:** Built the "Expand" mechanic, allowing players to dynamically unlock new grid rows and increase their unit cap using in-game currency, requiring dynamic updates to the play area and camera framing.

---

## Car Wreck Fest
**Role:** Sole Developer  
**Genre:** Hyper-casual Arcade / Physics  
**Tech:** Custom Vehicle Controller, Modular Physics Systems, Prefab Pipelines

<video autoplay playsinline muted loop preload="metadata" width="100%">
  <source src="{{ '/assets/videos/hyper-archive/vehiclewreck-gameplay.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

A physics-driven hyper-casual prototype focused on arcade vehicle control, modular car destruction, and character interactions, built end-to-end by a single developer for rapid gameplay validation.

### Key Technical Contributions
- **Custom Vehicle & Physics Architecture:** Designed and owned a modular vehicle framework covering input handling, camera follow, movement logic, and physics-driven car parts, enabling both real-time gameplay behavior and meta-layer vehicle upgrades without tightly coupling progression logic to physics.
- **Meta-Layer Vehicle Upgrade Systems:** Implemented data-driven meta progression layers for upgrading vehicle properties (e.g., performance, durability, component behavior), designed to safely modify runtime physics parameters while preserving gameplay stability and iteration speed.
- **Prefab-Driven Gameplay & Environment Systems:** Built reusable prefab pipelines for vehicles and stadium environments, decoupling content from logic to support rapid restructuring, safe iteration, and scalable expansion of upgradeable content.

<br>
<br>

# Soup Games (2019–2022)

A hyper-casual/mobile game studio where I and my artist partner developed various hyper-casual games and prototypes for publishers as a team of two.

These prototypes had an average of **2-week pipelines** for ideation, design, and development to end up in a test release. Publishers would test out these games for potential data to decide on scaling or killing the project.

*Some Honorable Mentions:*

### **Save The City**
**Genre:** Minigame Bundle / Police Simulation  
A comprehensive police-themed collection featuring diverse gameplay loops tied together by a station progression system.
* **Tech Highlights:** Built a modular "minigame framework" allowing the app to switch context seamlessly between 2D logic puzzles (suspect identification, parking jams), 3D action scenes (FPS training, chases), and idle management (station upgrades). Implemented randomized clue generation logic for the detective segments to ensure replayability.

### **Drift Legend RC**
**Genre:** Arcade Racing / Physics  
An RC car simulation played in a domestic environment. The core challenge was tuning the physics to feel like a lightweight toy car while maintaining satisfying, controllable drift mechanics.
* **Tech Highlights:** Implemented a custom arcade vehicle controller with exaggerated side-friction curves to allow for "snappy" drifting. Included dynamic camera smoothing to handle rapid direction changes without inducing motion sickness.

### **Jewelry 3D**
**Genre:** ASMR Simulation / Crafting  
A multi-stage crafting simulation where players fulfill customer orders by processing raw gems. The loop involves breaking raw rock, laser-cutting shapes, and polishing the final product.
* **Tech Highlights:** Developed a sequence of diverse interactions (tapping to break, drag-to-cut). Utilized mesh swapping and particle effects to simulate the "revealing" of the gem from the rough stone. Implemented line-renderer based logic for the laser cutting stage to detect shape tracing accuracy.

### **Sticky Smash Ball**
**Genre:** Runner / Katamari-style  
A momentum-based runner where the player controls a ball that "sticks" enemies to its surface. The ball grows in size and mass, allowing it to smash through numbered walls and obstacles.
* **Tech Highlights:** Created a dynamic parenting system that disables enemy AI and attaches them to the player sphere's surface upon collision. Managed physics mass calculations to ensure the ball felt heavier and more powerful as it collected more objects.

### **Physics Puzzles**
**Genre:** Physics / Logic Puzzles  
A suite of three prototypes exploring rope physics, dynamic mesh generation, and pathfinding logic.
* **Zipline Rescue:** A path-drawing puzzle where players generate a dynamic zipline mesh to guide crowds safely past obstacles like sawblades. I implemented physics joints to handle multiple characters sliding simultaneously on a user-generated curve.
* **Electric Flow:** A logic puzzle involving wrapping physical cables around pegs to connect power sources. The challenge was creating a stable "rope wrapping" simulation that could detect knots and valid connections without physics jitters.
* **Fruit Rope:** A physics puzzler requiring players to manipulate taut ropes to divert falling objects into target zones. Utilized Unity's physics engine with custom collision layers to handle the interaction between the "fluid" fruit particles and solid obstacles.