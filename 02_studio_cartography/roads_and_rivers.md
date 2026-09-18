---
layout: default
title: Roads & Rivers Network
parent: Hexmap Studio & Map Building
nav_order: 2
---

# Roads & Rivers Network

Creating roads, trade routes, trails, and waterways is a breeze with Lidarion's integrated vector path engine. Paths seamlessly snap to hex centers and edges, creating natural travel networks that integrate with your terrain.

---

## 1. Entering Roads & Rivers Mode

To start drawing travel routes and waterways:
1. Select the **Roads & Rivers** layer (<i class="fa-solid fa-route"></i>) at the top of the Studio palette.
2. The tools palette switches into Path Mode, presenting options for **Roads** (<i class="fa-solid fa-road"></i>) and **Rivers** (<i class="fa-solid fa-water"></i>).

---

## 2. Drawing Roads

Lidarion renders roads with a specialized, stylized **dotted travel trail** aesthetic that complements fantasy cartography:

* **How to Draw**:
  * Select **Roads**.
  * Click on your starting hex and **drag** your mouse across adjacent hexes.
  * As your cursor moves across hexes, clean dotted path segments automatically connect between adjacent hex centers.
* **Line Width Presets**:
  * Choose from 5 stepped thickness levels (Level 1 to Level 5, ranging from fine footpaths to broad imperial highways).
* **Color Palette & Presets**:
  * Select from built-in road color presets (like parchment bone `#FAF6EE`, dirt brown, or stone grey), or click the color picker to define any custom color.

---

## 3. Drawing Rivers

Rivers in Lidarion feature an advanced dual-layer vector shader that creates a natural flowing waterway with soft shoreline banks:

* **Dual-Layer Rendering**:
  * **Core River Stream**: A solid, vibrant blue waterway following the path center.
  * **Soft Shoreline Bank**: An automatic 3px translucent outer water transition that blends gently into the adjacent terrain hextiles.
* **How to Draw**:
  * Select **Rivers**.
  * Click on the mountain or lake source hex and drag downstream toward the coast.
  * Winding river bends snap cleanly to the hexagonal geometry.
* **River Width Presets**:
  * Adjust between stepped widths (from narrow mountain streams to wide navigable rivers).

---

## 4. Editing & Erasing Path Segments

* **Erasing Connections with Drag**:
  * Select the **Eraser** tool (<i class="fa-solid fa-eraser"></i>).
  * Click and drag across the path segment you wish to remove. Only the traversed connection is deleted.
* **Single-Click Hex Intersection Clearing**:
  * Clicking directly on a single hex with the Eraser tool removes all incoming and outgoing connections meeting at that hex.
* **Layer Isolation**:
  * Erasing roads or rivers will **never** damage or erase the terrain or object tiles underneath!

