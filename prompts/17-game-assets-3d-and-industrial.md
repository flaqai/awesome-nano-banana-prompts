# Game Assets, 3D, and Industrial Concept Prompts

## 1. Animation-ready 2D sprite sheet

**Best for:** game prototyping · **Format:** grid · **Difficulty:** Advanced

```text
Image 1: approved original character anchor. Create a transparent-background sprite sheet using a fixed
{{cell_width}}×{{cell_height}} cell grid. Include exactly {{animation_list_and_frame_counts}}. Preserve character
proportions, palette, costume, equipment, outline weight, pixel density, ground line, and facing direction.
Keep each frame centered with consistent margins and no overlap.

No existing game IP, mixed scales, anti-aliased pixels when pixel art is requested, duplicated frames, cropped
equipment, text, shadows outside cells, or background. Verify frame count and animation continuity.
```

## 2. Isometric modular environment kit

**Best for:** level-building concepts · **Format:** 16:9 sheet · **Difficulty:** Advanced

```text
Create an isometric modular kit for {{environment_theme}} on a clean neutral sheet. Include exactly {{tile_list}},
with one shared grid unit, identical camera angle, matching edge heights, repeatable materials, and consistent light.
Show a small assembled example using only the supplied modules. Palette: {{palette}}; rendering: {{style}}.

No mismatched perspective, unique edges that cannot connect, hidden backs, changing scale, baked text, logo,
or extra module. Verify that every path, wall, corner, stair, and doorway joins correctly.
```

## 3. Inventory item family

**Best for:** RPG and strategy UI · **Format:** 1:1 atlas · **Difficulty:** Intermediate

```text
Create a square inventory atlas with exactly {{item_count}} original items: {{item_list}}. Each item sits in an
equal transparent cell, uses the same three-quarter camera, scale logic, outline behavior, light direction, and
render finish. Rarity is communicated only through {{approved_rarity_system}}, not item size.

No existing franchise shapes, duplicated item, inconsistent padding, labels, numbers, background scene, or glow
that obscures silhouettes. Count items and verify each remains recognizable at 64 pixels.
```

## 4. Industrial machine cutaway

**Best for:** concept communication · **Format:** 3:2 · **Difficulty:** Advanced

```text
Images 1–2: verified exterior and internal references for {{machine}}. Create a 3:2 technical cutaway showing
only {{approved_subsystems}}. Preserve exterior geometry, access panels, safety guards, scale, and subsystem position.
Use clear color coding and leader lines with labels {{approved_labels}}. Rendering: precise industrial 3D with
neutral studio light and restrained section surfaces.

Do not invent engineering details, remove guards in the operational view, imply certification, show unsafe operation,
or add specifications not provided. Verify subsystem mapping and label endpoints.
```

## 5. Gameplay HUD over an original scene

**Best for:** game UI exploration · **Format:** 16:9 · **Difficulty:** Advanced

```text
Create a 16:9 gameplay mockup for an original {{genre}} game set in {{world}}. Overlay a practical HUD containing
{{required_HUD_elements}} while keeping the action readable. Establish clear hierarchy, safe margins, consistent icon
language, controller-friendly scale, and accessible state colors. Use only this sample data: {{approved_data}}.

No existing game interface, fake platform logo, random quest text, unreadable microtype, excessive vignette, or HUD
element without a gameplay purpose. Verify every value and keep critical action unobstructed.
```

