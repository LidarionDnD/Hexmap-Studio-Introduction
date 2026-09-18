---
layout: default
title: Baking Composite Maps & Performance
parent: Playable Hexmaps & Performance
nav_order: 2
---

# Baking Composite Maps & Performance

One of the greatest technical challenges in virtual tabletop mapping is rendering massive worlds. Lidarion solves this through an architectural breakthrough: **High-Performance Scene Baking**.

---

## 1. The Challenge of Live Tile Documents

When you design a map in Hexmap Studio, every terrain tile, road segment, and placed tree or ruin is a live, editable Foundry document. 

* On a modest 50×50 hexmap, there can easily be **5,000 to 10,000 individual tiles**.
* While Hexmap Studio handles this effortlessly during editing using **Viewport Culling**, having players render thousands of separate sprite objects during a live session can drain GPU memory and battery on player laptops.

---

## 2. The Baking Solution ("Bake Scene")

**Baking** compiles your entire hexmap into a single, ultra-high-resolution, seamless WebP background image.

### How to Bake a Map
1. In the top-right corner of Hexmap Studio, click the **"Bake"** button (<i class="fa-solid fa-cake-candles"></i>).
2. A progress modal appears showing real-time chunk rendering and an accurate countdown timer.
3. The engine renders all terrain hextiles, vector roads, flowing rivers, and object props into an optimized WebP image.
4. Lidarion automatically generates a dedicated **Baked Scene** in your standard Foundry **Scenes directory** (`fa-map`), fully configured with the exact same grid dimensions, regions, and journal links!

---

## 3. Verified 250,000+ Hex Tile Stability

Baking delivers unprecedented performance scalability:
* **Battle-Tested**: Lidarion's baking pipeline has been verified with maps containing **over 250,000 hex tiles**.
* **Rock-Solid 60 FPS**: Because the entire map is treated by Foundry as a single static background texture, your players experience instantaneous load times, zero stutter, and flawless 60 FPS panning even on modest hardware.

---

## 4. Non-Destructive Workflow: Unbaking & Editing

You are never locked into a baked map:

* **Return to Edit Mode Anytime**:
  * Your original working map remains safe in the **Hexmaps Directory**.
  * Click **"Unbake Scene"** or **"View & Edit"** to re-open Hexmap Studio.
* **Make Changes & Re-Bake**:
  * Add new mountain ranges, erase roads, or place new cities.
  * Click **"Bake"** again: Lidarion will cleanly update the existing playable scene without breaking player token positions, walls, or notes!

---

## 5. Viewport Culling During Active Editing

Even before baking, Hexmap Studio maintains high authoring performance through **Automatic Viewport Culling**:

* **How It Works**: The engine calculates which hexes are currently visible inside your screen boundaries, plus a safety buffer of **+5 hexes** in all directions.
* **Lag-Free Painting**: Only visible tiles are rendered into the GPU scene graph. Off-screen tiles are temporarily culled, keeping framerates high even when zooming and panning across vast continents.
* **HUD Status**: The bottom status bar displays live metrics (e.g. `240 in view / 4,800 culled`).

