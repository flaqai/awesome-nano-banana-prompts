# Architecture, Interiors, and Real Estate Prompts

## 1. Floor plan to photoreal interior

**Best for:** early spatial visualization · **Format:** 16:9 · **Difficulty:** Advanced

```text
Image 1: approved floor plan with dimensions. Image 2: material palette reference only.
Create a photorealistic eye-level interior view from {{camera_position}} looking toward {{direction}}.
Preserve the room footprint, ceiling height, wall openings, door swings, window locations, circulation,
and built-in elements from Image 1. Apply only the materials named in {{approved_material_schedule}}.
Lighting: physically plausible {{time_of_day}} daylight plus the specified practical fixtures.

Do not enlarge the room, move walls, add windows, hide doors, invent furniture, or copy objects from
Image 2. Keep verticals straight, scale credible, and every material consistent across reflections.
```

## 2. Controlled interior renovation

**Best for:** before-and-after concepts · **Format:** match input · **Difficulty:** Advanced

```text
Image 1: existing room photo. Renovate only {{approved_scope}} using {{materials_and_colors}}.
Preserve camera position, room geometry, windows, doors, ceiling, floor area, permanent structure,
and every object listed in {{protected_elements}}. Replace {{elements_to_replace}} and remove only
{{approved_removals}}. Match perspective, daylight direction, contact shadows, and color bounce.

Do not change the view outside, make the room larger, raise the ceiling, add structural openings,
or conceal defects that remain in scope. Return a truthful design visualization, not a listing photo.
```

## 3. Retail spatial concept

**Best for:** pop-ups and small shops · **Format:** 3:2 · **Difficulty:** Intermediate

```text
Create a 3:2 spatial concept for a {{store_type}} occupying {{approximate_area}}. Customer journey:
{{entry_to_checkout_sequence}}. Include entrance threshold, hero display, browsing zone, accessible
circulation, checkout, storage access, and one memorable brand installation based on {{concept}}.
Materials: {{materials}}; lighting: layered ambient, accent, and task lighting; viewpoint: wide eye-level.

No impossible aisle widths, blocked exits, floating shelves, fake customer logos, unreadable signage,
or excessive decorative stock. Keep fixture construction and product scale plausible.
```

## 4. Architectural axonometric explainer

**Best for:** design presentations · **Format:** 4:5 · **Difficulty:** Advanced

```text
Image 1: verified architectural model or drawings. Create a clean 4:5 exploded axonometric explaining
{{building_system}}. Separate exactly {{layer_count}} layers along one vertical axis and label only:
{{approved_labels}}. Use consistent projection, restrained material colors, thin leader lines, a scale
figure, and a compact legend. Show relationships without implying construction details not provided.

Do not invent structure, services, dimensions, codes, or assembly order. Verify layer count, alignment,
and every label endpoint against Image 1.
```

## 5. Facade material and lighting study

**Best for:** architecture and hospitality concepts · **Format:** 16:9 · **Difficulty:** Advanced

```text
Image 1: approved facade geometry. Create a 16:9 dusk material-and-lighting study. Preserve massing,
openings, signage zones, roofline, neighboring context, camera, and landscape. Apply {{facade_materials}}
with realistic joints, weathering, roughness, and reflections. Illuminate only the specified fixtures:
{{fixture_plan}}. Maintain dark-sky-conscious, physically motivated light distribution.

Do not add floors, windows, signs, vehicles, crowds, dramatic fog, or impossible uplighting. Keep all
existing legal and accessibility elements visible.
```

