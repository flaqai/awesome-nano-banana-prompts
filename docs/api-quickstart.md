# Gemini API Quick Start for Nano Banana Pro

Nano Banana Pro's model ID is `gemini-3-pro-image`. The current Gemini API documentation uses the Interactions API for image generation and editing.

## Prerequisites

```bash
pip install -U google-genai
export GEMINI_API_KEY="your-key"
```

Never commit an API key. Keep `.env` files ignored and use a secret manager in production.

## Python: text to image

```python
from google import genai
import base64

client = genai.Client()

prompt = """
Create a 16:9 editorial product image for a fictional ceramic tea set.
Warm side light, tactile glaze, restrained ivory and moss palette, no text or logos.
"""

interaction = client.interactions.create(
    model="gemini-3-pro-image",
    input=prompt,
    response_format={
        "type": "image",
        "mime_type": "image/png",
        "aspect_ratio": "16:9",
        "image_size": "2K",
    },
)

with open("tea-set.png", "wb") as output:
    output.write(base64.b64decode(interaction.output_image.data))
```

Use `1K`, `2K`, or `4K` when supported by the selected model and surface. Generate lower-resolution drafts first when cost and iteration speed matter.

## Python: continue an edit

```python
interaction_2 = client.interactions.create(
    model="gemini-3-pro-image",
    input=(
        "Keep the subject, crop, materials, and composition unchanged. "
        "Change only the background from ivory to deep forest green."
    ),
    previous_interaction_id=interaction.id,
    response_format={
        "type": "image",
        "mime_type": "image/png",
        "aspect_ratio": "16:9",
        "image_size": "2K",
    },
)
```

## Search grounding pattern

```python
interaction = client.interactions.create(
    model="gemini-3-pro-image",
    input=(
        "Use current, authoritative information to create a simple weather-preparedness "
        "infographic for the named city and date. Omit any value you cannot verify."
    ),
    tools=[{"type": "google_search"}],
    response_format={"type": "image", "aspect_ratio": "16:9", "image_size": "2K"},
)
```

Grounding improves access to current information; it does not replace editorial fact-checking. Review every claim and comply with Google's display requirements.

## Production checklist

- pin and test the SDK version used by your application;
- add retries and sensible timeouts;
- retain prompts, model ID, date, input rights, and output QA status;
- sanitize user-supplied filenames and content;
- do not log credentials or sensitive reference images;
- check current pricing, quotas, regional availability, and policy;
- preserve SynthID and required disclosures.

Official documentation: [image generation](https://ai.google.dev/gemini-api/docs/image-generation) and [Gemini 3 Pro Image model card](https://ai.google.dev/gemini-api/docs/models/gemini-3-pro-image).

