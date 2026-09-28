---
name: save-images
description: Save a photo, screenshot, menu, or diagram the user attached. Use when the user shares one or more images, or asks to remember what a picture shows.
---

# Save images

Load the subject with the continue-subject skill if none is active. Use the image the user attached. Do not invent image bytes.

## How to save

- One image: call `captureImage` with `image_data`, `mime_type`, `title`, and a short `description`.
- Two or more: call `captureImageBatch` once. Each item needs `image_data`, `mime_type`, and `title`. The batch holds at most 50 images.
- `mime_type` is `image/png`, `image/jpeg`, `image/webp`, or `image/gif`. Do not send SVG.
- `category` is `screenshot`, `diagram`, `asset`, or `other`.

The image is stored on the active world model.

## Paid plans

Image capture is not included on the free Starter plan. Paid plans include it, up to that plan's image limit.

If the tool says a paid plan is required, or that the image limit is reached, tell the user in one sentence. Then call `captureConversationContext` with a written description of what the image shows, so the subject still keeps the note.
