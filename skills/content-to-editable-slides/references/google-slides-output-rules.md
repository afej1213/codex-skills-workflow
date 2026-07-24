# Google Slides Output Rules

Load this reference when creating or verifying the final deck.

## Native Google Slides Requirement

The finished deliverable must be a native Google Slides file:

- MIME type: `application/vnd.google-apps.presentation`
- Import mode when using a local PPTX: `native_google_slides`
- Do not return a Drive-hosted PPTX link as the final deliverable.
- Do not return a deck made only of slide-sized PNG screenshots.

## Recommended Connector Verification

After import or creation:

1. Read the presentation with the Google Drive / Google Slides connector.
2. Confirm title, presentation id, slide count, and slide object ids.
3. Confirm the URL came from import response or readback.
4. Fetch thumbnails for visual QA.
5. If thumbnail URL must be curled, use a fresh file and inspect the actual image.

## Editable Element Expectations

Keep editable whenever practical:

- titles
- body copy
- section labels
- diagrams and connectors
- package matrices
- KPI timelines
- comparison tables
- CTA blocks

Images may be used as:

- backgrounds
- hero visuals
- mood visuals
- supporting concept images

Images should not replace whole slides unless the user explicitly asks for image-only slides.

