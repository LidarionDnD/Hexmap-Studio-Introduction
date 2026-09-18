---
layout: default
title: Exploration, Travel & Atmosphere
parent: Playable Hexmaps & Performance
nav_order: 1
---

# Exploration, Travel & Atmosphere

When your campaign session begins, Lidarion Hexmap Studio provides dedicated tabletop tools to make overland travel immersive and exciting.

---

## 1. Discrete Hex Fog of War

In traditional tabletop software, token vision reveals an awkward circular bubble that cuts through the middle of hexes. Lidarion fixes this with **Discrete Hex Exploration**:

* **How to Enable**:
  1. Open your Scene Configuration.
  2. Locate the **"Lidarion – Hexmap Exploration"** checkbox.
  3. Check the option and save changes.
* **How It Works at the Table**:
  * As tokens travel across the map, fog of war clears in **whole, discrete hexagonal tiles**.
  * A hex is either fully explored or concealed, preserving the mystery of adjacent wilderness tiles.
* **On-Screen Discovery Banners**:
  * When a party token crosses into a newly discovered territory or location, an animated cinematic title banner automatically appears on the players' screens:
    * `NEW AREA DISCOVERED: The Whispering Woods`
    * `NEW LOCATION DISCOVERED: The Sunken Citadel`

---

## 2. Group Token Travel Mechanics

Managing overland travel with a single party token keeps the game moving while providing clear travel pacing:

* **Configuring a Party Token**:
  1. Double-click the party/caravan token on the canvas to open its **Token Configuration**.
  2. Navigate to the token options and enable **"Group Token (Lidarion Hexmaps)"**.
* **Movement Speed Setting**:
  * In Foundry's Module Settings, configure **"Group Token Movement Speed"** (`groupTokenSpeed`).
  * Default: `1.0` space per second.
* **Animated Hex-by-Hex Traversal**:
  * When you drag or direct the party token across multiple hexes, it doesn't instantly teleport or slide diagonally across borders.
  * Instead, it smoothly animates step-by-step from hex center to hex center along the shortest path, giving players a tactile sense of distance and travel time.

---

## 3. Atmospheric Weather Clouds (FXMaster Integration)

To bring your overland map to life, Lidarion includes an integrated atmospheric cloud layer:

* **Setting**: **"Automatic Clouds on Hexmaps"** (`autoCloudWeather`) in client module settings (enabled by default).
* **Seamless Cloud Animation**: Drifting cloud shadows float across the terrain, adding depth and visual polish to mountains and valleys.
* **Dynamic Zoom-Responsive Density**:
  * **Zooming Out (Continental View)**: Clouds condense into denser atmospheric formations, enhancing the feeling of looking at a sprawling continent.
  * **Zooming In (Local View)**: Clouds automatically thin out and disperse, ensuring that individual trees, paths, and hex details remain crystal clear while playing.

