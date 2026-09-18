---
layout: default
title: Scene Management & Directory
parent: Getting Started
nav_order: 1
---

# Scene Management & The Hexmap Directory

Lidarion Hexmap Studio introduces a dedicated workspace for your campaign world maps, keeping your overland hexmaps completely organized and separated from tactical battlemaps and dungeon scenes.

---

## 1. The Hexmaps Sidebar Tab

In Foundry VTT's right sidebar, Lidarion adds a dedicated **Hexmaps** tab with a hexagon icon (<i class="fa-solid fa-hexagon-nodes"></i>).

* **Independent Directory**: Your working hexmaps are managed here instead of cluttering the standard Scenes directory.
* **Search & Filter**: Use the search input at the top of the directory to instantly filter maps by name.
* **Favorites System**: Click the star icon on any hexmap card to mark it as a favorite for quick access.
* **Quick Action Header**:
  * **New Hexmap (+)**: Launches the creation dialog for a new hexmap scene.
  * **Open Studio**: Directly launches the full-screen Hexmap Studio on the currently viewed map.

---

## 2. Creating a New Hexmap Scene

Clicking the **"New Hexmap"** button opens the creation dialog with the following configurable options:

| Setting | Recommended Default | Description |
|:---|:---|:---|
| **Scene Name** | `Hexmap Region` | The descriptive name of your campaign region, continent, or kingdom. |
| **Columns (Width)** | `30` | The horizontal width of the map measured in hex columns. |
| **Rows (Height)** | `20` | The vertical height of the map measured in hex rows. |

### Automatic Grid Alignment
Lidarion automatically configures the scene's grid type to **Hexagonal Column – Even** (`GridType: 4`). This ensures that hextiles, paths, tokens, and hover highlights align with mathematical precision.

### Large Map Advisory
If you configure a map exceeding **7,500 hex tiles**, a warning notice will appear:
> While Hexmap Studio supports massive maps, editing maps with tens of thousands of individual live tile documents can cause browser performance impacts during authoring. However, once you **Bake** the scene (see [Chapter 5](../05_gameplay_mechanics/baking_performance.html)), performance remains silky smooth at 60 FPS even with **over 250,000 hex tiles**!

---

## 3. Hexmap Cards & Context Actions

Each hexmap in the directory is represented by an informative card:

* **Tile Counter**: Displays the exact number of placed terrain tiles and object props.
* **Hover Controls & Right-Click Menu**:
  * **View & Edit (Left-Click)**: Switches your canvas to this map and opens Hexmap Studio.
  * **Activate**: Activates the scene for your connected players.
  * **Configure**: Opens Foundry's standard Scene Configuration sheet.
  * **Duplicate**: Creates an exact clone of the hexmap, including all tiles, paths, regions, and lore.
  * **Delete**: Permanently removes the hexmap scene after a confirmation prompt.

---

## 4. Studio Scenes vs. Baked Scenes

Understanding the dual-scene architecture is key to getting the best performance in Lidarion:

1. **Hexmap Studio Scene (Authoring Mode)**:
   * Accessible in the **Hexmaps Sidebar**.
   * Contains individual, live, editable tiles, vector paths, regions, and objects.
   * Features dynamic **Viewport Culling** so you can paint massive worlds without lag.
2. **Baked Scene (Campaign Gameplay Mode)**:
   * Generated automatically when you click **"Bake Scene"**.
   * Merges all visual tiles, roads, rivers, and props into a single ultra-high-resolution WebP background.
   * Appear in Foundry's standard **Scenes Sidebar** ready for your players.
   * You can return to the Studio scene to make edits and re-bake at any time!

