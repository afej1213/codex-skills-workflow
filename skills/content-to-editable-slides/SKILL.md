---
name: content-to-editable-slides
description: "Analyze and deconstruct user-provided copy, documents, files, brand proposals, marketing strategies, or content plans; extract the core narrative; generate relevant ChatGPT Image / imagegen visuals when useful; and produce a polished, native editable 16:9 Google Slides deck. Use when the user asks to turn text, files, a proposal, brand strategy, client plan, campaign idea, pitch, report, or marketing content into editable Google Slides with editable text, shapes, matrices, flows, packages, and visual storytelling."
---

# Content To Editable Slides

Use this skill to turn user-provided content into a polished, editable Google Slides deck. The final output must be a native Google Slides presentation, not an image-only deck and not a Drive-hosted PPTX.

Default language: follow the user's content language. If the user writes Chinese, produce Chinese deck copy unless they request otherwise.

## Core Contract

- Final format: native editable Google Slides.
- Aspect ratio: 16:9.
- Editable objects: titles, body text, shapes, matrices, flows, package tables, timelines, KPI blocks, and diagrams should remain editable where practical.
- Images: use generated or sourced images as visual assets, backgrounds, or supporting imagery, but do not flatten full slides into screenshots.
- If visual style is uncertain, stop before image generation and ask the user to choose a direction, or provide 3 clear visual directions and wait for confirmation.
- Do not invent logos, fake screenshots, fake testimonials, fake client venue photos, or unsupported metrics.

## Required Workflow

### 1. Intake And Source Read

Read the user's provided copy, files, or existing strategy artifacts first. If local files are referenced, inspect them before asking questions.

Extract:

- audience and decision-maker
- goal and success criteria
- core message
- offer / package / service structure
- funnel or user journey
- key proof points, data, and citations
- constraints, compliance risks, and missing facts
- required final language and tone

If the source is long, create a short content spine before building slides: title, claim, proof object, and visual role for each slide.

### 2. Visual Direction Gate

Before using ChatGPT Image / imagegen, decide whether the visual style is sufficiently specified.

Treat style as specified when the user provides at least one of:

- a reference deck or completed example
- a brand style, mood, palette, or industry aesthetic
- a clear audience and design tone
- explicit approval of one proposed direction

If style is not specified, offer exactly 3 directions and wait. Use concise options such as:

1. Premium editorial: cinematic images, dark refined palette, high-end client pitch feel.
2. Modern commercial: clean business deck, bright product/service visuals, sharper sales clarity.
3. Social-first creative: bold hooks, lifestyle imagery, TikTok/Reels campaign energy.

After confirmation, generate only the visuals that have a clear slide role. Record generated images as AI concept visuals unless the user provides real brand assets.

### 3. Deck Story And Structure

Create a deck that reads like a client-ready presentation, not a copied document.

Default 10-14 slide structure:

1. Cover / positioning promise
2. Executive thesis
3. Current diagnosis or opportunity
4. Brand / message anchor
5. Market or audience insight
6. Audience persona / segmentation
7. User journey / funnel
8. Content or campaign system
9. AIGC / production workflow when relevant
10. Offer / package / service matrix
11. KPI / measurement roadmap
12. Compliance, risks, and next steps

Adjust the slide count to fit the source. Split dense content across slides instead of shrinking text.

### 4. Image Generation Rules

Use imagegen for premium raster visuals when visual storytelling matters.

For every generated image, define:

- slide role
- aspect ratio and crop
- focal placement
- text-safe area
- whether it is background, hero image, mood visual, or supporting image

Prompt rules:

- Ask for no logos and no readable text unless the user explicitly needs text in the image.
- Avoid fake brand marks, fake UI, fake testimonials, or fake screenshots.
- For brand/client cases without real photos, label generated images as concept visuals.
- Prefer 16:9 images for full-slide backgrounds.
- Generate a small set of purposeful images instead of flooding the deck with decorative assets.

### 5. Build Path For Native Editable Google Slides

Preferred path:

1. Use the Presentations skill to create a polished local 16:9 PPTX with editable primitives.
2. Use the Google Slides skill / Google Drive connector to import the PPTX with `upload_mode: "native_google_slides"`.
3. Read back the imported deck with the connector.
4. Verify the MIME type is `application/vnd.google-apps.presentation`.
5. Verify slide count and that deck content is editable, not one screenshot per slide.
6. Fetch and inspect fresh thumbnails for visual QA.
7. Final answer only with the verified Google Slides link or id, not the local PPTX path.

Direct Google Slides batchUpdate creation is allowed only when the user explicitly asks for it or when the local PPTX import path is unavailable. Warn that the PPTX import path normally gives better design quality.

### 6. Design Standards

Use visual hierarchy and editorial rhythm:

- short slide titles with a clear claim
- one proof object per slide where possible
- strong spacing and alignment
- no overcrowded tables
- no three consecutive slides with the same layout
- no generic card-grid deck unless a matrix is the actual proof object
- no decorative platform logos unless verified or user-provided

Use editable shapes for:

- funnels
- journey maps
- package matrices
- KPI timelines
- comparison tables
- process flows
- segment maps

Use images for:

- hero mood
- product/place/service visual context
- campaign or brand concept
- chapter atmosphere

### 7. Verification Checklist

Before handoff, verify:

- final deck is native Google Slides
- aspect ratio is 16:9
- text and shapes are editable
- important matrices, flows, packages, and KPI blocks are not flattened images
- no clipped text, overlap, or unreadable tiny text in thumbnails
- generated visuals are not presented as real client photos
- sources and compliance notes are included when needed
- final URL or presentation id came from connector import/readback, not a guessed link

## Output Style

In the final response, keep it short:

- provide the verified Google Slides link
- mention slide count and 16:9
- state that text/shapes are editable
- mention any caveat, such as AI concept visuals or missing real brand assets

Do not end by asking the user to download or copy local files.

