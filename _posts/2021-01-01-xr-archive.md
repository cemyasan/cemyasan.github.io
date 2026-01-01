---
title: "XR Development (2016-2023)"
excerpt: "A showcase of 7+ years in XR development, ranging from award-winning commercial releases on Steam to B2B hardware integrations and medical therapeutics on standalone headsets."
header:
  teaser: /assets/images/xr-archive/teaser.jpg
categories:
  - Portfolio
tags:
  - VR
  - Unity
  - Oculus/Meta Quest
  - SteamVR
  - HTC Vive Trackers
  - Kinect
  - Optimization
---

> This page archives my extensive work in Extended Reality (XR). With over 7 years of experience in this specific domain, I have shipped commercial products on Steam/Oculus, developed "Serious Games" for medical therapy, and engineered complex B2B installations using custom hardware peripherals like Vive Trackers and Microsoft Kinect.

---

# Commercial Release

## Header Goal VR: Being Axel Rix
**Role:** Sole Developer  
**Genre:** Physics Arcade / Sports  
**Tech:** SteamVR, Oculus SDK, Physics Architecture  
**Platform:** HTC Vive, Oculus Rift, Meta Quest (Steam & Oculus Store)<br>
**Web-site:** <a href="https://www.headergoalvr.co/" target="_blank">headergoalvr.co</a>

*Header Goal VR* is an action-packed, physics-based VR sports game featuring **simulation-like interaction dynamics**. Players step into the shoes of **Axel Rix**, a young soccer player, progressing through story-based levels to master their heading skills. The gameplay goes beyond simple arcade mechanics; it requires strategic planning—hitting targets in specific orders to maximize combos—while interacting with fully dynamic lighting and destroyable environments.

<video autoplay playsinline muted loop preload="metadata" width="75%">
  <source src="{{ '/assets/videos/xr-archive/header-goal-gameplay.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Key Technical Contributions
- **Physics-Based Interaction:** Engineered a "natural and realistic" heading mechanic that calculates precise reflection vectors based on headset velocity and impact angles, creating a simulation-grade feel.
- **Dynamic Environment Systems:** Implemented **fully dynamic lighting** and a destruction system for **breakable objects**, enhancing immersion without sacrificing performance on 2016-era hardware.
- **Cross-Platform Architecture:** Built a hardware-agnostic player rig supporting HTC Vive, Oculus Rift, and recently **Meta Quest**, allowing for a single codebase to deploy across PCVR and standalone platforms.
- **Game Loop Engineering:** Designed a robust level progression system featuring combo mechanisms, Steam and Oculus Store achievements and leaderboards, and localized UI support for multiple languages.
- **Performance Optimization:** Optimized physics calculations and rendering pipelines to maintain a strict 90 FPS on 2016-era VR hardware, preventing motion sickness during high-speed gameplay interactions.

---

# Digital Therapeutics

At **DancingMind Therapeutics**, I led the development of VR content designed to assist in the rehabilitation of patients with dementia and stroke. Beyond the flagship titles, I developed a broad library of **cognitive simulations and memory retention games**, transitioning my focus from PC-based powerhouses to highly optimized mobile VR (Pico/Quest) environments.

## DancingMind Apps
**Role:** Sole Developer
**Genre:** Serious Games / Health  
**Tech:** Photon PUN, Custom Build Pipelines, Mobile Optimization  
**Platform:** Meta Quest, Pico Neo 2 / G2 (Standalone)

A comprehensive suite of gamified therapy and life-skill training experiences. Beyond physical therapy tools like *Hummingbird* (neck exercises) and social multiplayer games like *Dart VR*, I developed a vast library of **cognitive and memory training modules** (e.g., object sorting) and **"Life Integration" simulations**. These realistic scenarios allowed patients to practice daily tasks in a safe environment, including **subway navigation, pedestrian traffic safety, kitchen cooking, marketplace shopping, hospital visits, and guided meditation**. These projects required strict adherence to accessibility standards and robust tooling to manage multiple hardware targets from a single codebase.

<img src="{{ '/assets/images/xr-archive/dancing-mind-comp.jpg' | relative_url }}" width="100%">

### Key Technical Contributions
- **Automated Multi-SDK Build Platform:** Engineered a custom build automation tool that dynamically switches build targets (Pico vs. Quest) within the same project. The system automatically strips unused SDKs from the build to minimize bloat and supports generating "Non-VR" builds with simulated mobile/mouse controls for rapid debugging without a headset.
- **Universal Interaction Framework:** Developed modular VR interaction systems designed to work agnostically across all supported SDKs. I implemented a simulation layer that maps standard mouse/keyboard inputs to VR controllers, allowing complex VR mechanics to be tested and refined on standard displays.
- **Real-Time Multiplayer (Photon PUN):** Built the multiplayer architecture for a dart game using **Photon PUN**, synchronizing projectile physics, scoring, and VR avatar movements in real-time to allow up to 3 patients to interact in a shared virtual space. Also used these modules a couple of other projects later on. This was integrated with a **custom avatar creation** system.
- **Mobile Optimization & Accessibility:** Achieved stable framerates on standalone Android chipsets through aggressive asset optimization, while implementing "comfort mode" movement systems tailored for users with limited mobility.

---

# Hardware Integration & B2B

During my time at **Codemodeon** and **Flamingo Game Studio**, I specialized in experimental hardware integrations. These projects often required bypassing standard input systems to utilize HTC Vive Trackers, Kinects, and Green Screen technologies for custom B2B installations.

## Experimental Installations & Custom Hardware
**Tech:** HTC Vive, Oculus Rift, Vive Trackers, Kinect  
**Scope:** B2B Marketing, Event Installations

* **Archery VR:** A realistic archery simulation designed for public events. This was achieved by **mounting an HTC Vive Tracker onto a physical recurve bow**, allowing users to aim and shoot using the actual weight and ergonomics of real archery equipment, bridging the gap between physical skill and virtual aim.
<a href="https://www.youtube.com/watch?v=FfF6dxLlh74" target="_blank">Youtube Video</a>
* **Cyber Security VR Card Game:** A turn-based strategy game developed for a mobile service brand. I engineered a **local multiplayer system** where two players (Hacker vs. Defender) faced off in VR using a card battle mechanic to deploy "attacks" (viruses) or "defenses" (firewalls).
<a href="https://www.youtube.com/watch?v=hi_Rg6iGs2o" target="_blank">Youtube Video</a>
* **Mixed Reality Stage Demo:** Developed a live-feed application using green screen technology to composite real-time video of a player into the VR environment. **I achieved this by mounting an HTC Vive Tracker directly onto the physical camera**, enabling the virtual camera to synchronize perfectly with the real-world operator's movements.
<a href="https://www.youtube.com/watch?v=l_5DODciNWE" target="_blank">Youtube Video</a>
* **Vertigo VR:** An acrophobia experience where users walk on a physical plank. I implemented Vive Trackers on the user's feet to render virtual shoes that matched real-world movements 1:1, significantly increasing immersion.
<a href="https://www.youtube.com/watch?v=kN5z3gn5cUU" target="_blank">Youtube Video</a>
* **Turkcell Kopilot:** A high-fidelity driving simulator where I synchronized the VR environment with a **Logitech steering wheel** and a **motion seat platform**, simulating physical forces like acceleration and crashes.
<a href="https://www.youtube.com/watch?v=FJ4JCnIlZOo" target="_blank">Youtube Video</a>
* **Streetball VR:** A penalty kick simulator. I utilized tracker data to calculate the velocity and trajectory of a user's real kick to launch a virtual ball.
* **Penalty Master (Kinect):** A penalty kick simulator using Microsoft Kinect. I developed the body tracking interpretation layer to specifically track the user's feet, allowing players to simulate kicking a virtual ball by swinging their leg in the real world.

<img src="{{ '/assets/images/xr-archive/vr-1.jpg' | relative_url }}" width="100%">
<img src="{{ '/assets/images/xr-archive/vr-2.jpg' | relative_url }}" width="100%">