# Multilingual Prompting and In-Image Localization

Nano Banana Pro can generate legible text in multiple languages and translate text inside an existing design. Production localization still requires locale-aware copy, protected data, layout control, and human review.

## Locale contract

```text
TARGET LOCALE: {{language-region}}
AUDIENCE: {{country_or_community}}
TONE: {{formal_conversational_luxury_playful}}
TRANSLATE: {{headlines_body_labels}}
DO NOT TRANSLATE: {{brand_names_SKUs_URLs_legal_marks}}
PRESERVE EXACTLY: {{prices_dates_units_numbers}}
LAYOUT: preserve grid, hierarchy, artwork, margins, and reading order; allow native line breaks.
QA: compare every protected field with the source and proofread the target copy character by character.
```

## Master localization prompt

```text
Image 1: approved source design.

Create a {{target_locale}} edition of Image 1. Change only the text declared as translatable.
Preserve the composition, images, logo placement, colors, typography hierarchy, spacing, prices,
numeric data, product codes, and legal marks. Use natural copy for {{target_audience}}, not a
word-for-word translation. Keep the same information priority; adjust line breaks and font size
minimally to prevent overflow. Do not add claims or explanatory text. Before finalizing, compare
every protected value with Image 1 and verify the target-language text character by character.

TRANSLATABLE COPY
{{source_to_target_mapping}}

PROTECTED STRINGS
{{brand_SKU_URL_price_date_legal_strings}}
```

## Eight copy blocks for one campaign

Use these as syntax examples. Adapt tone and vocabulary with a native reviewer.

### English — `en-US`

```text
Headline: "MAKE ROOM FOR BETTER MORNINGS"
Supporting line: "Thoughtful tools for an easier daily rhythm."
CTA: "EXPLORE THE COLLECTION"
```

### Simplified Chinese — `zh-CN`

```text
标题："给清晨，多一点从容"
副标题："贴近日常的好设计，让每一天更轻松。"
行动文字："探索系列"
```

### Traditional Chinese — `zh-TW`

```text
標題："讓早晨，多一點從容"
副標題："貼近日常的好設計，讓每一天更輕鬆。"
行動文字："探索系列"
```

### Japanese — `ja-JP`

```text
見出し："朝に、心地よい余白を。"
補足："毎日のリズムを整える、使い手思いの道具。"
CTA："コレクションを見る"
```

### Korean — `ko-KR`

```text
헤드라인: "더 나은 아침을 위한 여유"
보조 문구: "일상의 리듬을 가볍게 만드는 세심한 도구."
CTA: "컬렉션 보기"
```

### Spanish — `es-MX`

```text
Titular: "HAZ ESPACIO PARA MEJORES MAÑANAS"
Texto de apoyo: "Objetos bien pensados para un ritmo diario más ligero."
CTA: "CONOCE LA COLECCIÓN"
```

### French — `fr-FR`

```text
Titre : "PLACE À DES MATINS PLUS DOUX"
Sous-titre : "Des objets bien pensés pour alléger le rythme du quotidien."
CTA : "DÉCOUVRIR LA COLLECTION"
```

### German — `de-DE`

```text
Headline: "MEHR RAUM FÜR BESSERE MORGEN"
Subline: "Durchdachte Begleiter für einen leichteren Alltag."
CTA: "KOLLEKTION ENTDECKEN"
```

## Mixed-language poster

```text
Create a bilingual 4:5 cultural-festival poster. The local-language headline is primary and
occupies 70% of the typographic emphasis; the English translation is secondary. Keep the two
scripts in separate text blocks with shared baseline logic, not character-by-character pairing.
Render exactly:

"夏夜风物集"
"SUMMER NIGHT MARKET"
"8月30日 17:00–22:00"
"AUG 30 · 5–10 PM"

Do not translate the venue name "RIVER HALL". Do not add vendors, sponsors, ticket prices,
QR codes, or social handles. Check both scripts and every time value before finalizing.
```

## Localization QA

- Was the target locale specified, not just a broad language?
- Are brand names, product codes, URLs, prices, dates, units, and legal marks protected?
- Does the translation sound native and preserve intent?
- Are line breaks appropriate for the writing system?
- Are punctuation, spacing, capitalization, diacritics, and full-width forms correct?
- For right-to-left languages, was reading direction and mirrored layout explicitly planned?
- Did the image preserve the source hierarchy and non-text content?
- Has a native speaker reviewed the final artwork?

## Right-to-left adaptation pattern

```text
Create an Arabic `ar-SA` edition. Translate the declared marketing copy into natural Modern
Standard Arabic. Set all Arabic copy right-to-left with correct connected letterforms. Mirror
the text-column alignment and directional navigation cues, but do not mirror the product,
photography, logo, numbers, or asymmetric brand mark. Preserve prices and SKUs exactly.
Use an Arabic type style with visual weight equivalent to the source Latin type. Check letter
joining, punctuation placement, numerals, and reading order before finalizing.
```

## CJK adaptation pattern

```text
Create a Japanese `ja-JP` edition. Use approved Japanese copy exactly. Preserve the brand name
in Latin characters. Use Japanese punctuation and natural phrase-level line breaks; do not split
small kana, punctuation, or a unit from its number. Slightly increase line spacing if needed,
while preserving hierarchy and the source design's visual density.
```

