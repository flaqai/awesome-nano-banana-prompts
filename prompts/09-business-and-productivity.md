# Business and Productivity Prompts

## 1. Investor pitch slide

**Best for:** narrative prototyping · **Format:** 16:9 · **Difficulty:** Advanced

```text
Create one 16:9 investor slide titled "{{slide_title}}". The single takeaway is {{takeaway}}.
Use one primary chart and no more than three supporting callouts. Render only this verified data:
{{data_with_units_dates_and_sources}}. Style: quiet, confident, boardroom-ready, large labels, strong hierarchy.

Do not invent market size, growth rates, sources, logos, customers, or forecasts. Use honest axes and distinguish
actuals from estimates. Include source text exactly: "{{source_line}}". Verify every value and unit.
```

## 2. Executive one-page visual summary

**Best for:** reports and decision memos · **Format:** 3:4 · **Difficulty:** Intermediate

```text
Design a 3:4 executive summary titled "{{title}}" with four sections: CURRENT STATE, SIGNALS, DECISION, NEXT 30 DAYS.
Use the approved content only: {{content}}. Combine short text, one mini-chart, and a four-item action list. Create a
clear top-to-bottom reading path and accessible color coding.

No invented metrics, decorative stock imagery, fake citations, jargon, or body text below readable size. Preserve
qualifiers such as "estimated" and "pending". Check dates, owners, and numbers.
```

## 3. Operational workflow diagram

**Best for:** process alignment · **Format:** 16:9 · **Difficulty:** Intermediate

```text
Create a 16:9 swimlane diagram for {{workflow}} with lanes {{lane_names}}. Show exactly these stages and decision
points: {{verified_steps}}. Use standard process shapes, one direction of flow, clear handoffs, and exception paths.
Title: "{{title}}". Color by ownership, not decoration.

Do not change step names, owners, or sequence. Do not hide loops or errors. Keep connectors from crossing labels and
verify that every decision has labelled outcomes.
```

## 4. Product roadmap

**Best for:** planning communication · **Format:** 16:9 · **Difficulty:** Intermediate

```text
Create a 16:9 outcome-based roadmap for {{product}} covering {{time_horizon}}. Use rows for {{workstreams}} and columns
for {{periods}}. Place only these approved initiatives: {{initiatives_with_status}}. Visually distinguish COMMITTED,
PLANNED, and EXPLORING and include a compact legend.

Do not invent dates, dependencies, owners, or delivery promises. Preserve uncertainty wording. Avoid Gantt-like false
precision unless exact dates are supplied. Verify every initiative appears once.
```

## 5. Report cover system

**Best for:** whitepapers and research · **Format:** A4 portrait / 3:4 concept · **Difficulty:** Beginner

```text
Design a restrained report cover for {{organization}}. Topic: {{topic}}. Use an original abstract visual metaphor
based on {{data_material_or_process}}, with {{palette}} and generous whitespace. Render exactly:
"{{report_title}}" "{{subtitle}}" "{{month_year}}" "{{organization_name}}".

No fake seal, barcode, issue number, data visualization, partner logo, or extra author unless supplied. Keep copy clear
at thumbnail size and leave safe margins for print trimming.
```

