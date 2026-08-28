# Contributing

Thanks for helping build a useful, rights-safe Nano Banana Pro prompt library.

## What a strong contribution includes

- a real production use case;
- an original prompt written by you for this repository;
- placeholders using `{{double_braces}}` where customization matters;
- explicit reference-image roles;
- exact text and localization rules when the asset contains copy;
- locked constraints and a short QA step;
- a title, intended output, suggested aspect ratio, and difficulty level.

## Originality and rights

Do not submit:

- copied or lightly paraphrased prompts from another collection, social post, course, or creator;
- an image copied from another gallery or generated from an input you cannot redistribute;
- removed author credits or intentionally obscured provenance;
- prompts whose main purpose is cloning a living artist's signature style;
- deceptive identity edits, non-consensual likeness use, or unverified high-stakes claims.

If you build on a permissively licensed source, follow that license and provide attribution in the contribution. When in doubt, submit a clean-room original recipe instead.

## Recipe format

````markdown
## Recipe title

**Best for:** ...  
**Format:** ...  
**Inputs:** ...  
**Difficulty:** Beginner / Intermediate / Advanced

```text
FUNCTION
...

LAYOUT
...

ASSETS
...

QUALITY LOCKS
...
```

**Why it works:** one concise paragraph.  
**Adapt it:** two or three safe variables to change.
````

## Example-image metadata

If you include an image, add a sidecar YAML file with the model ID, prompt file, recipe name, generation date, aspect ratio, rights status for inputs, and post-processing. Never label output from another model as Nano Banana Pro.

## Review checklist

- [ ] Prompt is original and reproducible.
- [ ] Placeholders and reference roles are clear.
- [ ] Exact copy and protected strings are separated.
- [ ] Constraints prevent likely drift.
- [ ] Claims about model capability match current official documentation.
- [ ] Example-image rights and provenance are documented.
- [ ] Markdown links and headings work.
- [ ] No credentials, personal data, or private assets are included.
