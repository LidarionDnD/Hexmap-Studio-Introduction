---
layout: default
title: Playable Hexmaps & Performance
nav_order: 6
has_children: true
permalink: /05_gameplay_mechanics/
---

# Chapter 5: Playable Hexmaps & Performance

Running an overland hex crawl requires both engaging table mechanics and rock-solid software performance. This chapter explains how Lidarion handles discrete hex fog of war, group travel animations, weather effects, and high-performance scene baking for massive worlds.

---

## In this Chapter

* **[Exploration, Travel & Atmosphere](exploration_and_travel.html)**
  * Discrete Hex Fog of War exploration (revealing whole hex tiles instead of circular sight bubbles).
  * Setting up party tokens as "Group Tokens" with animated space-by-space travel.
  * Configuring travel speed (`groupTokenSpeed`).
  * Dynamic weather clouds powered by FXMaster with automated zoom scaling.
* **[Baking Composite Maps & Performance](baking_performance.html)**
  * Understanding live tile documents vs. flattened background composites.
  * The Baking workflow: Generating high-resolution WebP images for 60 FPS performance.
  * Tested stability: Running maps with over **250,000 hex tiles**.
  * Unbaking back to edit mode anytime.
  * Viewport Culling during active editing.

