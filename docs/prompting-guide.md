# Nano Banana Pro Prompting Guide

This guide turns an image idea into a production brief that Nano Banana Pro can reason about, render, edit, and localize. It is written for `gemini-3-pro-image`, where complex instructions, text-heavy layouts, grounded visuals, reference-image composition, and iterative editing are more important than raw generation speed.

## 1. Think in contracts, not adjectives

An effective prompt is a small production contract. It tells the model:

1. what the asset must accomplish;
2. what content must appear;
3. how the content should be composed;
4. what supplied references mean;
5. what must remain unchanged;
6. how the result will be checked.

“Make it premium and cinematic” is a mood. “Create a 4:5 product launch poster, one bottle at 60% frame height, headline in the upper safe area, warm rim light, no invented claims” is a production instruction.

## 2. The FLAQ prompt stack

Use only the blocks your task needs.

```text
F — FUNCTION
Asset, audience, channel, communication goal.

L — LAYOUT
Canvas, hierarchy, camera, placement, safe zones, reading order.

A — ASSETS
Subjects, exact copy, product facts, reference-image roles, brand rules.

Q — QUALITY LOCKS
Invariants, prohibited changes, fact checks, character-by-character review.
```

### Function

Name the deliverable and decision it supports:

```text
Create a 16:9 hero image for a landing page aimed at independent coffee shops.
The single message is: inventory forecasting can feel calm and understandable.
```

### Layout

Describe the canvas as a designer or cinematographer:

```text
Wide eye-level view; subject occupies the right 55%; clean negative space on the left;
keep all important details inside a 10% safe margin; soft morning side light; 4K output.
```

### Assets

Separate visual content from literal copy:

```text
Image 1: product identity and geometry reference.
Image 2: label artwork reference—place on the product without redesigning it.
Image 3: lighting reference only—do not copy its objects or composition.

TEXT — RENDER VERBATIM
"Forecast less. Serve more."
```

### Quality locks

State what cannot drift:

```text
Preserve the bottle silhouette, cap shape, label proportions, brand colors, and exact copy.
Do not invent badges, ingredients, prices, certification marks, barcodes, or fine print.
Before finalizing, compare the product against Image 1 and verify all text character by character.
```

## 3. Prompt order for common jobs

### Text-to-image

```text
goal → subject/action → environment → composition → style/light → exact text → constraints → QA
```

### Image editing

```text
input role → requested change → locked elements → blend rules → prohibited drift → QA comparison
```

### Multi-image compositing

```text
input index and role → base scene → placement → scale/perspective → shared lighting → identity locks
```

### Localization

```text
source image → target locale → translatable fields → protected fields → layout locks → numeric QA
```

### Grounded infographic

```text
question → audience → source/grounding instruction → visual structure → exact labels → uncertainty rule
```

## 4. Exact text that survives production

Text rendering is strongest when copy is treated as immutable data.

```text
TEXT — RENDER VERBATIM
Line 1: "WEEKEND MARKET"
Line 2: "SAT 09:00–14:00"
Line 3: "RIVER STREET · HALL B"

Use exactly three lines. Do not add a slogan, URL, price, logo, punctuation, or repeated words.
Verify capitalization, the en dash, middle dot, and every digit before finalizing.
```

Practical rules:

- finalize copy before image generation;
- keep body copy short enough for the canvas;
- separate headline, supporting line, price, and disclaimer;
- provide exact punctuation and case;
- protect names, URLs, SKUs, dates, and currency values;
- require “no other text” when stray copy would be costly;
- for long paragraphs, ask the model to draft and approve the text before asking it to typeset the image.

## 5. Reference-image roles

Never write “use these images” without roles.

| Role | Instruction pattern |
|---|---|
| Identity | Preserve face, age, skin tone, hair, body proportions, and distinguishing features. |
| Product | Preserve silhouette, material, seams, ports, label geometry, and color. |
| Base scene | Keep camera position, architecture, horizon, and object layout unchanged. |
| Pose | Transfer the body pose only; do not copy identity, clothing, or background. |
| Style | Use palette, texture, mark-making, and finish only; do not copy subject matter. |
| Lighting | Match direction, softness, contrast, and color temperature only. |
| Logo/artwork | Place supplied artwork accurately; do not redraw or reinterpret it. |
| Material | Apply the referenced surface behavior while preserving object geometry. |

Example:

```text
Image 1: approved character identity anchor.
Image 2: pose reference only.
Image 3: watercolor texture reference only.
Image 4: background location reference.

Use the identity from Image 1 in the pose from Image 2, inside the location from Image 4,
with the restrained paper grain and edge softness of Image 3. Do not transfer the person,
clothing, objects, or composition from Images 2–3.
```

## 6. Editing without drift

Editing prompts need three layers:

```text
CHANGE
Replace only the two dining chairs with curved walnut chairs.

LOCK
Keep the room geometry, camera, table, floor, windows, wall art, sunlight, and crop unchanged.

BLEND
Match contact shadows, lens perspective, wood grain scale, and ambient color bounce.
```

Repeat the lock block in every follow-up. Do not assume a conversational model remembers which details are sacred after several edits.

## 7. Character and brand consistency

Create an anchor before creating a series.

### Character anchor

Generate a neutral sheet containing front, three-quarter, profile, full-body, expression, outfit construction, color swatches, and a short written trait list. Approve it, then use that one image as the identity reference throughout the sequence.

### Product anchor

Use clean views of the real product. Declare which references control front label, side profile, finish, closure, and dimensions. If a generated frame changes the product geometry, correct it before using that frame as a new reference.

### Brand anchor

Keep a compact brand block:

```text
Brand personality: quietly optimistic, precise, human.
Palette: warm ivory #F5F0E6, ink #1F2328, citrus #F5C542.
Typography: geometric sans-serif headlines, humanist sans-serif body.
Image behavior: real materials, soft directional light, uncluttered sets.
Never use: neon gradients, chrome text, floating UI chips, generic AI sparkles.
```

## 8. Search-grounded visuals

Grounding can help with current weather, geography, known objects, public facts, and educational diagrams, but it does not remove the need for review.

```text
If Google Search grounding is available, verify the five data points against authoritative
sources current to {{date}}. Use only facts that can be verified. If a value is uncertain or
conflicting, omit it rather than estimating. Return a short source list in the accompanying
text response; do not place URLs inside the image unless requested.
```

Use primary sources for science, medicine, law, finance, public policy, and product specifications. Never publish an image merely because its labels look plausible.

## 9. Composition controls

Useful controls include:

- aspect ratio: `1:1`, `4:5`, `3:2`, `16:9`, `9:16`, `21:9` where supported;
- shot size: macro, close-up, medium, full-body, wide, aerial;
- viewpoint: eye level, low angle, top-down, isometric, orthographic;
- lens behavior: wide environmental view, normal perspective, compressed telephoto look;
- focus: deep focus, shallow depth, focus falloff, foreground occlusion;
- light: direction, size, hardness, color, motivation, time of day;
- layout: grid, center axis, asymmetry, reading order, negative space, safe zone;
- physical logic: contact shadows, reflections, material roughness, scale cues.

Avoid piling incompatible camera terms into one prompt. Choose the few that control the result.

## 10. Format recipes

| Channel | Suggested canvas | Layout notes |
|---|---|---|
| E-commerce hero | 1:1 or 4:5 | Product large, clean silhouette, mobile-safe labels |
| Instagram feed | 4:5 | Headline in central safe area, bold first-read shape |
| Story/Reel cover | 9:16 | Keep face and copy away from top/bottom UI zones |
| YouTube thumbnail | 16:9 | One subject, one idea, very short copy, high contrast |
| Website hero | 16:9 or 21:9 | Declare where HTML copy will sit; often generate no text |
| Presentation slide | 16:9 | Large labels, strong hierarchy, limited body copy |
| Print poster | 2:3 or 3:4 | Specify bleed/safe margin conceptually; export-check separately |
| Marketplace listing | 1:1 | Accurate geometry and color; avoid unverified claims |

## 11. Multi-turn refinement

Use observable defect language:

```text
Keep everything else unchanged. Make only these corrections:
1. Replace the headline with "SMALL STEPS, REAL CHANGE" exactly.
2. Move the headline upward by approximately one headline height.
3. Reduce the orange saturation slightly so skin tone remains natural.
Do not change the subject, crop, pose, clothing, background objects, or lighting direction.
```

Good iterations change one category at a time:

1. composition;
2. identity or product accuracy;
3. lighting and materials;
4. text;
5. localization;
6. final crop and resolution.

## 12. Negative constraints that work

Prefer concrete exclusions:

```text
one bottle only; five fingers on each visible hand; no label redesign; no extra copy;
no duplicated jewelry; no floating objects; no halo around cutout edges; no modern objects;
no unreadable microtext; no watermark added by the composition.
```

Avoid enormous generic negative-prompt lists. They dilute the important constraints.

## 13. Final QA checklist

### Content

- correct subject, count, action, setting, and audience;
- exact text, numbers, punctuation, language, and reading order;
- no invented claims, ingredients, certifications, or prices;
- factual labels checked against authoritative sources.

### Visual

- identity and product geometry match references;
- hands, eyes, reflections, shadows, and object contact look coherent;
- type is legible at intended display size;
- important content sits within platform safe zones;
- crop, aspect ratio, and resolution match the deliverable.

### Rights and provenance

- permission exists for people, products, logos, and source images;
- no copied community prompt or unlicensed example image;
- no deceptive identity use;
- SynthID and required disclosures are preserved;
- the output is not described as an official benchmark unless it truly is one.

## 14. Failure recovery

| Symptom | Better follow-up |
|---|---|
| Text misspelled | Supply only the exact copy block, reduce text volume, lock everything else. |
| Layout drifts during translation | Translate text only; lock grid, prices, art, hierarchy, and line-count limits. |
| Face changes | Return to the approved identity anchor; remove conflicting references; restate locks. |
| Product shape changes | Use cleaner product views; assign geometry and label roles explicitly. |
| Composite looks pasted | Request matched perspective, color temperature, grain, contact shadow, and bounce light. |
| Infographic invents facts | Supply verified facts as data; enable grounding; require omission when uncertain. |
| Design becomes cluttered | Restate the single message; cap element count; remove decorative copy. |
| Edit changes too much | Use CHANGE / LOCK / BLEND blocks and repeat them every turn. |

## 15. Copy-ready prompt builder

```text
You are producing a final visual asset, not brainstorming.

FUNCTION
Deliverable: {{asset}}
Audience: {{audience}}
Channel: {{channel}}
Single message: {{message}}

LAYOUT
Canvas: {{aspect_ratio}}, {{resolution}}
Composition: {{framing_and_hierarchy}}
Camera: {{viewpoint_and_lens_behavior}}
Lighting: {{direction_quality_temperature}}
Palette/materials: {{visual_system}}

ASSETS
Subject/action/environment: {{content}}
Image 1: {{role}}
Image 2: {{role}}

TEXT — RENDER VERBATIM
{{exact_copy}}
Do not add, translate, paraphrase, repeat, or decorate any other text.

QUALITY LOCKS
Preserve: {{invariants}}
Change only: {{scope}}
Exclude: {{specific_failures}}
Before finalizing, verify: {{text_identity_geometry_facts_safe_zone}}
```

Next: browse the [prompt library](../prompts/) or adapt the [multilingual localization patterns](multilingual-prompting.md).

