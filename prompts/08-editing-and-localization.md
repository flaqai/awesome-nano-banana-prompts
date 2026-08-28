# Editing, Localization, and Compositing Prompts

## 1. Precise object replacement

**Best for:** interiors and product cleanup · **Format:** match input · **Difficulty:** Intermediate

```text
Image 1: edit target. Image 2: replacement-object reference.
Replace only {{target_object}} in Image 1 with the object from Image 2. Preserve the base camera, crop, room geometry,
all other objects, people, surface textures, and light direction. Match scale, perspective, occlusion, depth of field,
contact shadow, reflection, and color bounce.

Do not move, recolor, remove, sharpen, or restyle anything else. Do not duplicate the replacement. Compare the entire
frame with Image 1 and confirm that pixels outside the necessary blend area are conceptually unchanged.
```

## 2. Localized menu without layout drift

**Best for:** international campaigns · **Format:** match input · **Difficulty:** Advanced

```text
Image 1: approved source menu. Create a {{target_locale}} edition. Replace only text in the approved mapping:
{{source_to_target_copy}}. Preserve brand name, item order, prices, currency, numbers, dietary icons, logo placement,
grid, illustrations, colors, hierarchy, margins, and paper texture. Use natural locale-appropriate line breaks and
adjust font size minimally only to prevent overflow.

Do not invent dishes, translations, prices, claims, or extra labels. Compare every protected string and price against
Image 1, then proofread every target-language character.
```

## 3. Day-to-night relighting

**Best for:** architecture, travel, and campaign variations · **Format:** match input · **Difficulty:** Advanced

```text
Image 1: daytime base image. Transform only time of day and physically dependent illumination to {{night_condition}}.
Preserve camera, geometry, people, faces, pose, clothing, signage, object count, weather, and composition. Replace sun
light with motivated moon, street, window, and practical light. Recalculate shadows, reflections, sky exposure, and
color temperature coherently.

Do not add neon signs, stars, fog, rain, vehicles, or lit windows unless physically implied or requested. Keep all
existing text unchanged and legible.
```

## 4. Clean background extraction

**Best for:** catalogs and design systems · **Format:** match input · **Difficulty:** Intermediate

```text
Image 1: extraction target. Isolate {{subject}} onto a genuinely transparent background. Preserve exact shape, product
label, colors, material highlights, semi-transparent areas, hair/fur fibers, and fine edges. Remove all background,
floor, props, cast shadow, and reflected environment unless {{shadow_requirement}}.

No white matte, checkerboard pattern, halo, clipped edge, extra outline, color spill, retouching, relighting, or label
redesign. Return a clean alpha channel and verify difficult edges at high zoom.
```

## 5. Multi-reference campaign composite

**Best for:** complex ads and group scenes · **Format:** 16:9 · **Difficulty:** Advanced

```text
Image 1: base location and camera. Images 2–{{n}}: people/product identity references. Image {{style_index}}: lighting
reference only. Create one cohesive 16:9 campaign scene where {{placement_and_action}}. Preserve each identity or
product independently; do not merge features. Match scale, perspective, eye line, focus, color temperature, grain,
contact shadow, reflection, and environmental bounce.

Keep base architecture and framing unchanged. Do not duplicate subjects, exchange clothing or labels, add props,
or transfer objects from the lighting reference. Count every subject and compare each one with its source.
```

