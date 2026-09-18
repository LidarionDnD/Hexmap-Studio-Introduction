---
layout: default
title: Keyboard Shortcuts & Quick Reference
nav_order: 7
has_children: false
permalink: /06_reference/
---

# Keyboard Shortcuts & Quick Reference

Keep this quick reference page handy for shortcuts, tool definitions, and settings while building and running your campaign.

---

## 1. Global Keyboard Shortcuts

| Shortcut | Action | Context |
|:---|:---|:---|
| **`Alt + H`** | Open / Toggle Hexmap Studio | Canvas (when viewing a hexmap scene) |

---

## 2. Mouse Controls & Gestures

| Action | Control | Result |
|:---|:---|:---|
| **Paint / Stamp Tile** | Left-Click | Places selected tile family at cursor |
| **Continuous Painting** | Left-Click & Drag | Paints multiple hexes across cursor trail |
| **Erase Tile / Prop** | Left-Click / Drag with Eraser | Removes elements on the active layer |
| **Sample Art (Eyedropper)** | Left-Click with Eyedropper | Samples tile family and resets to Brush |
| **Pan in Tile Creator** | Left-Click & Drag on Canvas | Repositions source image |
| **Zoom in Tile Creator** | Mouse Wheel Scroll | Zooms in/out relative to cursor |
| **Reload Image in Creator** | Right-Click Canvas | Opens "Delete Image" to reload artwork |
| **Delete Tile Family** | Right-Click Palette Card | Opens deletion dialog with permanent disk cleanup |
| **Delete Variant Tab** | Right-Click Variant Tab (`#2`..`#4`) | Removes variant from Creator family |
| **Open Scene Hub** | Left-Click on Painted Territory | Opens interactive regional codex |

---

## 3. Drawing Tools Summary

| Tool | Function |
|:---|:---|
| **Brush** | Paints tiles or props. Supports brush radius from 1 to 6 hexes. |
| **Fill Bucket** | Flood fills contiguous matching hexes with random variant support. |
| **Eraser** | Erases tiles on the active layer. Supports brush radius 1–6. |
| **Eyedropper** | Samples any tile or prop on the map and switches to Brush. |
| **Roads** | Connects adjacent hexes with styled dotted trail paths. |
| **Rivers** | Connects adjacent hexes with flowing rivers and translucent banks. |

---

## 4. Module Settings Overview

Configurable under **Configure Settings → Module Settings → Lidarion Hexmaps**:

| Setting Name | Scope | Default | Description |
|:---|:---:|:---:|:---|
| **Show Regions** | Client | `true` | Toggles whether translucent colored region overlays are visible on the map. |
| **Region Hover on Token/Notes Controls** | Client | `true` | Displays territory name tooltip when the mouse pauses over a hex while Token or Journal controls are active. |
| **Region Hover Delay** | Client | `0.5s` | Time the cursor must remain stationary over a hex before displaying the tooltip (0.1s to 5.0s). |
| **HUB Banner Title Alignment** | Client | `Centered` | Aligns the title in the Scene Hub banner: Centered or Left-aligned. |
| **Automatic Clouds on Hexmaps** | Client | `true` | Enables ambient drifting cloud shadows on hexmaps via FXMaster with dynamic zoom scaling. |
| **Group Token Movement Speed** | World | `1 space/s` | Sets the step-by-step hex animation speed for party tokens (0.1 to 10.0 spaces/second). |

---

## 5. Best Practices & Pro Tips

> ### 💡 Pro-Tip 1: The Core Hex Rule
> When creating custom terrain tiles, always ensure your artwork completely covers the **Green Core Hex** in the Creator. Any transparent areas in the green zone will appear as holes or gaps when placed next to neighboring tiles.
>
> ### 💡 Pro-Tip 2: Stacking Non-Destructive Layers
> Want to build a ruined castle atop a volcanic mountain? First paint the mountain on the **Terrain** layer, then switch to the **Objects** layer and place the castle on top. If you later decide to change the mountain into a snowy peak, your castle will remain untouched!
>
> ### 💡 Pro-Tip 3: Always Bake Before Game Night
> Before your players log in for the session, click **"Bake Scene"**. Baking produces a single, unified high-resolution background that runs at 60 FPS on any player laptop or tablet!

