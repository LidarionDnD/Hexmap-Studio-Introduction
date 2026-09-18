---
layout: default
title: Tools, Layers & Painting
parent: Hexmap Studio & Map Building
nav_order: 1
---

# Tools, Layers & Painting

Hexmap Studio is designed to make overland cartography as fast and intuitive as painting in digital art software, while preserving discrete hex grid accuracy.

---

## 1. Opening Hexmap Studio

To open the Studio on any active hexmap scene:
* Press the global hotkey: **`Alt + H`**
* Or click **"Edit in Hexmap Studio"** on any scene card in the Hexmaps sidebar directory.

### Studio Interface Overview
When Studio opens, a sleek floating dock appears on the left side of your screen:
* **Mode Switcher (Top Bar)**: Toggle between **Build Hexmap** (painting terrain and objects) and **Create Regions** (world-building and lore territories).
* **Live Hex Coordinates**: In the bottom status bar, `Hex: (i, j)` tracks the exact grid offset under your mouse pointer in real-time.
* **Viewport Culling Status**: Shows how many tiles are currently rendered in your active viewport versus how many are culled off-screen.

---

## 2. The Four Cartography Layers

At the top of the palette, you can switch between four distinct editing layers:

| Layer | Icon | Purpose |
|:---|:---|:---|
| **Terrain** | <i class="fa-solid fa-mountain-sun"></i> | Standard built-in biomes: Grassland, Forest, Mountains, Water, Desert, Tundra, Swamp, Jungle, Specials, and Dark Space. |
| **Custom Terrain** | <i class="fa-solid fa-shapes"></i> | Your own custom-created hextile categories, complete with user-defined accent colors and subcategories. |
| **Objects** | <i class="fa-solid fa-chess-rook"></i> | Structures, ruins, landmarks, and map props placed directly on top of terrain hextiles. |
| **Roads & Rivers** | <i class="fa-solid fa-route"></i> | Continuous vector connections running across hexes to form travel trails and flowing river networks. |

---

## 3. Universal Drawing Tools

The same intuitive toolset is available across **Terrain**, **Custom Terrain**, and **Objects**:

### <i class="fa-solid fa-paintbrush"></i> Brush Tool
* **Click to Place**: Single-click any hex to stamp the selected tile family.
* **Drag to Paint**: Click and drag your mouse across the map to rapidly paint continuous landmasses.
* **Brush Size Scaling (1 to 6 Hexes)**: Use the slider beneath the tools to scale your brush radius from a single hex up to a massive 6-hex cluster (covering up to 91 hexes in a single click!).
* **Hover Highlight Preview**: As you move your mouse over the canvas, a glowing golden polygon overlay outlines the exact radius of hexes that will be affected.

### <i class="fa-solid fa-fill-drip"></i> Bucket / Flood Fill
* **Intelligent Flood Fill**: Click on any hex to flood-fill all connected identical hexes with your currently selected tile family.
* **Variant Awareness**: If **Random Variant** is turned on, the fill algorithm automatically rolls varied art assets for every filled hex, producing a natural, variegated landscape without repetitive patterns.

### <i class="fa-solid fa-eraser"></i> Eraser Tool
* **Layer-Specific Erasing**: Click or drag across hexes to remove tiles on the active layer.
* **Brush Size Support**: The Eraser respects your Brush Size slider (1–6 hexes) with a red preview outline, allowing you to clear large areas quickly.

### <i class="fa-solid fa-eye-dropper"></i> Eyedropper Tool
* **Instant Asset Sampling**: Click on any placed tile or object on your map to immediately select its family in the palette.
* **Automatic Tool Reset**: After sampling a tile, the Eyedropper automatically switches back to the **Brush Tool** so you can immediately continue painting.

---

## 4. The 1-Terrain + 1-Object Stacking Rule

Lidarion Hexmap Studio enforces a clean, non-destructive **stacking engine** for every grid cell on your map:

> ### The Rule of Stacking
> For every hex coordinate `(i, j)` on your scene:
> 1. There can be at most **ONE** terrain hextile (on the Terrain/Custom Terrain layer, rendered at base sort ~100,000).
> 2. Placed on top of that cell, there can be at most **ONE** object hextile (on the Objects layer, rendered at base sort ~10,000,000).

### Non-Destructive Workflow Benefits
* **Painting Terrain Preserves Objects**: When you paint or flood-fill new terrain underneath an existing castle or tower object, the object stays perfectly in place.
* **Painting Objects Preserves Terrain**: Placing a city, ruin, or tree object never deletes the grassland or desert tile underneath it.
* **Isolated Erasing**: Using the Eraser on the **Objects** layer only deletes object props, leaving the terrain intact. Using the Eraser on the **Terrain** layer only clears the terrain tile, leaving the object intact.

---

## 5. Palette Features & Organization

### 2-Level Collapsible Accordions
* **Level 1 (Category)**: Displays the category name, custom accent color bar, and total tile count. Click to expand or collapse.
* **Level 2 (Subcategory)**: Organizes tile families into neat groups (e.g. *Grassland > Hills*, *Mountains > Peaks*).
* **Collapse/Expand All**: Use the angle toggle button in the header (<i class="fa-solid fa-angles-up"></i> / <i class="fa-solid fa-angles-down"></i>) to quickly collapse or expand all groups.

### Live Search Filter
Type into the search bar at the top of the palette to instantly filter tile families across all categories. Click the (<i class="fa-solid fa-xmark"></i>) button to instantly clear the search.

### Random Variant Shuffling vs. Specific Selection
* **Random Variant (Toggle ON)**: As you paint with the Brush or Fill Bucket, the engine randomly picks from all available art variations in that family. This produces realistic terrain without visual repetition.
* **Random Variant (Toggle OFF)**: Reveals a horizontal **Variant Selector** strip (`1`, `2`, `3`...) allowing you to hand-pick the exact graphic asset for specific landmarks.

---

## 6. Canvas Navigation & Global Controls

* **Pan Map without Painting**: Hold the **`Spacebar`** and drag with your mouse to pan around the scene freely.
* **Undo & Redo**
* **Infinity Mode Toggle**:
  * In the options of the Studio, toggle **Infinity Mode** ON or OFF.
  * When **ON**, painting near the outer edges of the map automatically and seamlessly expands the scene boundaries outward, letting you grow your world organically.
