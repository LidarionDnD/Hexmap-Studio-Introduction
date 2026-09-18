---
layout: default
title: The Custom Tile Creator Workshop
parent: Custom Tile & Object Creator
nav_order: 1
---

# The Custom Tile Creator Workshop

The **Custom Tile Creator** is an in-engine image workstation that removes all friction from preparing custom map art. You do not need Photoshop, GIMP, or external transparent PNG masks—the Creator handles scaling, positioning, masking, and export in a few clicks.

---

## 1. Launching the Creator

You can launch the Creator directly from the Studio palette:
* On the **Custom Terrain** layer: Click **"+ Add Custom Tiles"** (<i class="fa-solid fa-plus-circle"></i>).
* On the **Objects** layer: Click **"+ Add Custom Object"** (<i class="fa-solid fa-plus-circle"></i>).

The modal dynamically adapts its title, default accent colors (warm gold `#eab308` for objects), and storage directories based on whether you are crafting terrain or props.

---

## 2. The Interactive Canvas & Loading Images

The workshop features a generous **800×800 interactive canvas** with a dark checkerboard transparency background.

### Loading Artwork
* **Drag-and-Drop**: Simply drag any image file (`.png`, `.jpg`, `.jpeg`, or `.webp`) from the file explorer directly onto the canvas.
* **FilePicker**: Click the cloud upload button or the **"Load Image"** button in the sidebar to browse your Foundry VTT user data directories.

---

## 3. Understanding the Template Zones

Behind your image, they displays two color-coded template zones to help you position your art with mathematical precision:

1. **Green (Core Hex)**:
   * Represents the playable hexagonal cell on the canvas.
   * Rendered with a gentle 10% translucent green tint so you can align details while seeing the boundaries.
   * **Best Practice**: Ensure your artwork completely fills this green hexagon to prevent transparent gaps or holes between neighboring tiles on the map.
2. **Blue (Overhang Zone)**:
   * The allowed vertical overlap area extending above the core hex.
   * Perfect for high mountain peaks, towering pine trees, castle spires, or giant statues that naturally overlap the hex above them.
   * **"Mask blue overhang zone" Checkbox**: If your tile should be completely flat (e.g. flat grassland, sand dunes, or water), check this option. The Creator will automatically trim the blue overhang zone as well, producing a flush, flat hextile.
3. **Rest**:
   * Any portions of your image extending outside the green and blue zones are automatically clipped and made 100% transparent.

---

## 4. Pan, Zoom & Micro-Adjustments

Positioning your image is smooth and responsive:

* **Pan**: Click and drag anywhere on the canvas to move the image.
* **Mouse-Wheel Zoom**: Scroll up or down to zoom in or out relative to your mouse cursor.
* **Full-Width Zoom Slider**: A continuous slider (from **1%** up to **500%**) spans the bottom of the canvas.
* **Decimal Percentage Input**: Type an exact zoom level (e.g., `125.5` or `80%`) into the percentage box next to the slider and press **Enter** to jump immediately to that scale.
* **1-Pixel Keyboard Arrow Nudges**: Press the **Up**, **Down**, **Left**, or **Right** arrow keys on your keyboard to nudge the image by exactly 1 pixel for pixel-perfect alignment.
* **Reset Button**: Restores the image's original position and 100% scale.
* **Canvas Right-Click "Delete Image"**: Right-click the canvas at any time to remove the current image and reload a new one without losing your tab or category settings.

---

## 5. Multi-Variant Tabs (`Tile #1` to `Tile #4`)

A great fantasy map needs visual variety. Rather than creating and saving tiles one-by-one, the Creator features a **Multi-Variant Tab Bar** at the top of the canvas:

* **Adding Variants**: Click the **`+`** button to add tabs for `Tile #2`, `Tile #3`, and `Tile #4`.
* **Independent Transforms**: Each variant tab remembers its own uploaded image, pan coordinates, zoom level, and blue mask toggle.
* **Shared Family Metadata**: The Tile Name, Category, and Subcategory in the left sidebar apply to all variants in the family.
* **Removing Variants**: Right-click on any variant tab (`#2`, `#3`, or `#4`) and select **"Delete Variant"** to remove it.
* **One-Click Batch Save**: When you click **"Save Hextile"**, all configured variant tabs are exported simultaneously as a cohesive family!

---

## 6. Categories, Subcategories & Accent Colors

Organize your custom library into clean, beautiful collections:

* **Category Selection**: Pick an existing category from the dropdown or click **"Create new category..."**.
* **Custom Accent Color**: Every category has an accent color. In the Studio palette, this color dynamically themes the category header, border glow, and tile count badges using modern CSS color blending.
* **Subcategories**: Break large categories into manageable sub-groups (e.g., Category: *Volcanic Peaks* → Subcategories: *Active Lava*, *Basalt Fields*, *Obsidian Spires*).

---

## 7. Saving & Library Management

### Instant WebP Export
Clicking **"Save Hextile"** automatically:
1. Renders the transformed artwork through the binary alpha mask at high resolution.
2. Converts the image to a lightweight, gapless **200×200 WebP** asset.
3. Uploads the files directly into your world's storage folder (`worlds/{worldId}/hexmaps/_customtiles/` or `_customobjects/`).
4. Updates the catalog register (`register.json`), making your new tiles immediately available in the Studio palette without reloading Foundry!

### Safe Palette Management (Right-Click Context Menus)
In the Studio palette, you can right-click any custom element for instant management:
* **Right-Click Tile Card**:
  * **Edit Tile**: Loads the tile family back into the Creator for fine-tuning.
  * **Delete Tile**: Opens a safety confirmation dialog. Upon confirmation, the tile family is removed from your catalog and **permanently deleted from the hard drive**, leaving no orphaned files behind.
* **Right-Click Category or Subcategory**:
  * **Edit**: Rename the group or change its accent color.
  * **Delete**: Removes the category/subcategory and cleans up all associated files.
 
## 8. Import Hextiles
Do you already have a collection of hextiles? Copy them, along with the corresponding registry.json, into the `WORLDNAME/hexmaps/_customtiles/` folder, and they will appear after you reload Foundry VTT.

