---
title: "Space Heroes — Project Lead"
excerpt: "Project Dev Lead for a content-heavy mobile RPG. Built core gameplay + meta systems, a designer-facing hex-grid level editor, and production-safe persistence for a year of release + live updates."
header:
  teaser: /assets/images/space-heroes/teaser.jpg
categories:
  - Portfolio
tags:
  - Unity
  - C#
  - Mobile
  - Hybrid-casual
  - RPG
  - Editor Tools
  - Live Ops
---

> **Tech:** Unity, C#, Unity UI, ScriptableObjects, NavMesh, Editor Tooling, Custom Persistence, Analytics, Client-side Auth/Leaderboards/Cloud Save


## Project Overview

<img src="{{ '/assets/images/space-heroes/store-page.jpg' | relative_url }}" alt="Store page screenshot" width="100%">

**Studio:** Udo Games<br>
**Team Size:** 7 (Developers, Artists, Designers)<br>
**Role:** Project Development Lead<br>
**Timeline:** 6 months to first release + ~6 months of content updates<br>
**Store Pages:** 
<a href="https://tinyurl.com/spaceheroesand" target="_blank">Google Play</a> ·
<a href="https://tinyurl.com/spaceheroesios" target="_blank">App Store</a><br>
**Gameplay Videos:** <a href="https://tinyurl.com/spaceheroesvideos" target="_blank">Watch</a>

Space Heroes is a mobile, casual team-building RPG with an open-world structure, repeatable combat modes, hero progression, and a town/meta layer. The project’s technical complexity comes from scaling **large content volumes** (heroes, enemies, zones, quests) while maintaining **stable saves**, reliable navigation across streamed world regions, and efficient iteration during post-launch update cycles.


## My Role
- Owned the project end-to-end as **Project Development Lead** for ~1 year, responsible for technical direction and day-to-day execution.
- Designed and implemented the majority of **core gameplay + meta systems** (characters, combat, enemies, town/buildings/menus, quests, dungeons, challenges).
- **Managed and mentored other developers** on the project:
  - Defined technical direction and system boundaries.
  - Reviewed implementations for correctness, maintainability, and production safety.
  - Coordinated task ownership to reduce overlap and unblock parallel work.
- Built **designer-facing tooling** (hexagon-base world editor + dungeon editor workflow) to scale level production and reduce manual setup.
- Took responsibility for **production safety**: save/load, persistent state restoration, version compatibility, and regression risk during content updates.
- Acted as **Project Manager** during later update cycles—owning prioritization, release readiness, and scope trade-offs alongside implementation.


## World & Level Editor (Hexagon Base)
A major part of the project was enabling content production at scale through a custom **hex-grid world editor**.

- Implemented a hexagon-based level editor for designers.
- Designed the world to be **region-based**:
  - The map is split into regions by size.
  - The editor manages which objects belong to which region.
- Built runtime systems to support **dynamic region load/unload** based on character position.
- Implemented a complementary **dungeon editor workflow** for structured encounter content.

<video autoplay playsinline muted loop preload="metadata" width="100%">
  <source src="{{ '/assets/videos/space-heroes/level-editor.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

<img src="{{ '/assets/images/space-heroes/dungeon-editor.jpg' | relative_url }}" alt="Meta menus and progression" width="100%">

## Runtime Streaming & Navigation Safety
To keep an open-world structure performant on mobile, the world was built to stream content in and out safely.

- Implemented region-based loading boundaries to avoid loading the entire world at once.
- Supported navigation across streamed regions with runtime-oriented systems.
- Invested heavily in stability fixes around world streaming edge cases (e.g., missing area references, unloaded objects behavior, and safe defaults).

<video autoplay playsinline muted loop preload="metadata" width="100%">
  <source src="{{ '/assets/videos/space-heroes/navmesh.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


## Combat, Characters & Enemy Architecture
The gameplay layer was built to support many unique heroes and enemies without rewriting core logic.

- Character movement + interaction system foundations, iterated early and continuously.
- Combat system supporting unique hero and enemy behaviors (attacks, inflictors, damageables, effects).
- Enemy management + spawning systems designed to scale across:
  - Open world encounters
  - Dungeons
  - Challenge modes

<video autoplay playsinline muted loop preload="metadata" width="100%">
  <source src="{{ '/assets/videos/space-heroes/combat.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


## Recruitment, Management & Progression (Meta Layer)
The meta layer was built around stable data and UI-driven flows—because post-launch iteration happens here first.

- Implemented the recruitment and character management loop (selection, upgrades, training, rarity/progression data).
- Built town/building/menu architecture to support:
  - Multiple upgrade surfaces
  - Unlock gating
  - Safe iteration on UI-heavy systems during live updates

<video autoplay playsinline muted loop preload="metadata" width="50%">
  <source src="{{ '/assets/videos/space-heroes/menus.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


## Quests, Dungeons & Repeatable Modes
To support long-term play and updates, the project includes multiple repeatable content loops.

- Quest framework + quest UI and state management.
- Daily / weekly quest systems and related menu flows.
- Dungeon mode with dedicated scene/data controllers and robust “don’t lose progress/resources” edge-case handling.
- Challenge modes (e.g., arena-style flows) designed to reuse combat + progression systems.

<video autoplay playsinline muted loop preload="metadata" width="50%">
  <source src="{{ '/assets/videos/space-heroes/quests-dungeons.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>


## Persistence & Version Compatibility
Because this project shipped and then ran through content updates, persistence correctness was treated as a first-class system.

- Built and maintained a custom persistent data layer across core systems (characters, menus, quests, dungeons).
- Ensured player progression remained valid across updates by treating IDs and data consistency as a production risk area.
- Shipped targeted fixes for compatibility issues when older saved data needed to remain stable through content and system changes.


## Client-Side Online Services
The project includes online-facing features; my scope was the **Unity client integration and safety**.

- Implemented and maintained client-side flows for:
  - Authentication entry points and account linking patterns
  - Online leaderboards + season/reward UI surfaces
  - Cloud save integration and recovery flows
- Focused on production-readiness: fail-safe UI, retries/timeouts, and graceful degradation when services are unavailable.


---
