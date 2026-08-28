# Fashion, Beauty, and Lookbook Prompts

## 1. Consistent fashion lookbook contact sheet

**Best for:** collection presentation · **Format:** 3:2 · **Difficulty:** Advanced

```text
Images 1–{{look_count}}: approved garments. Image {{model_index}}: consenting model identity reference.
Create a clean 3:2 lookbook contact sheet with exactly {{look_count}} full-body looks. Preserve the model's
identity, body proportions, skin tone, hair, and apparent age. Preserve each garment's cut, length, closure,
print placement, fabric drape, and color. Use one neutral studio, camera height, lens behavior, and lighting.

Do not exchange garments, alter body shape, add accessories, duplicate looks, crop feet, or invent labels.
Number looks exactly {{approved_numbers}} and compare every outfit with its reference.
```

## 2. Beauty texture macro campaign

**Best for:** skincare and cosmetics art direction · **Format:** 4:5 · **Difficulty:** Intermediate

```text
Create a photorealistic 4:5 beauty macro featuring {{subject_description}} and {{product_or_texture}}.
Focus on real skin texture, pores, fine hair, natural lip and eye detail, and physically plausible product
sheen. Camera: close macro with a narrow but intentional focus plane. Light: {{soft_or_directional_setup}}.
Palette: {{palette}}. Leave {{copy_safe_area}} clear for later layout.

No skin smoothing, face reshaping, exaggerated wetness, floating droplets, impossible lashes, third-party
logos, medical claims, text, or identity imitation. Keep retouching editorial and human.
```

## 3. Identity-preserving virtual try-on

**Best for:** wardrobe previews · **Format:** match person reference · **Difficulty:** Advanced

```text
Image 1: consenting person and base pose. Images 2–{{n}}: garment references.
Replace only the clothing in Image 1 with the supplied garments. Preserve face, body shape, skin tone,
hair, expression, hands, pose, camera, background, and lighting. Reconstruct believable fabric tension,
folds, seams, closures, overlap, and contact shadows for the existing pose. Keep garment color and pattern exact.

Do not change weight, age, body proportions, hairstyle, makeup, or accessories. Do not combine garment
details or expose areas not shown in the original. Verify identity and construction against all inputs.
```

## 4. Colorway and fabric line sheet

**Best for:** merchandising and design review · **Format:** 16:9 · **Difficulty:** Advanced

```text
Create a front-facing 16:9 line sheet for {{garment_or_accessory}} with exactly {{variant_count}} approved
colorways. Show one consistent product view per variant, aligned to the same baseline and scale. Add a fabric
macro swatch and render only the approved variant name and code: {{variant_data}}. Background: neutral white;
lighting: even catalog light; layout: clean grid with generous margins.

Do not invent colors, prices, sizes, fibers, care symbols, sustainability claims, or decorative copy.
Verify each name, code, swatch, and product color mapping.
```

## 5. Multi-person runway editorial

**Best for:** campaign concepts with several identities · **Format:** 16:9 · **Difficulty:** Advanced

```text
Images 1–{{person_count}}: consenting identity and outfit references. Create a cinematic 16:9 runway editorial
in {{original_environment}}. Preserve each person's independent identity, age, skin tone, hair, body proportions,
and exact outfit construction. Place subjects at varied depths with natural gait and sight lines. Match scale,
perspective, motion blur, color temperature, contact shadows, and grain across the entire scene.

Do not merge faces, exchange clothing, duplicate people, add accessories, change body shape, or imitate a named
fashion campaign. Count every person and verify each against the corresponding input.
```

