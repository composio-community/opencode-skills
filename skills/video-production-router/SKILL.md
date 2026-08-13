---
name: video-production-router
description: Route and lock a video brief to generation, designed composition, supplied-footage editing, or an end-to-end mixed workflow before implementation.
---

# Video Production Router

## Goal

Turn a video request into one explicit production route before creating media. This skill decides; downstream tools implement.

## Inputs

Read the topic, audience, platform, duration, language, aspect ratio, supplied media, exact visible copy, and export target. Classify each reference as `reproduce`, `edit`, or `guide`.

## Routes

- **Generate**: new model-generated footage or imagery dominates.
- **Compose**: designed HTML/SVG scenes, explainers, kinetic type, charts, captions, overlays, or motion graphics dominate. This is the explainer default.
- **Edit**: supplied footage must be selected, cut, cleaned, reframed, captioned, mixed, localized, or changed. Keep semantic pixel changes inside the Edit route.
- **AUTO**: multiple routes must be woven into one finished deliverable.

Choose one primary route and list supporting routes separately. Do not use AUTO for a simple title or caption overlay. Do not silently switch the primary route later.

Canvas defaults: 16:9 → 1920×1080; 9:16 → 1080×1920; 1:1 → 1080×1080.

## Output

Return the primary and supporting routes; reason and reference relationship; platform, duration, language, canvas, and export format; timed outline or shot list; supplied assets and missing inputs; local and optional provider-backed operations; review gates; and playback QA.

Confirm before destructive edits, overwrites, paid provider calls, or publishing. If tools are unavailable, return the full unexecuted production package and explicitly label it planned rather than rendered.

## Example

“Cut this interview to 45 seconds, remove pauses, add captions and an animated title” → **Edit primary**, **Compose supporting**, 1080×1920 for a vertical deliverable.

## Provenance

Adapted from [OrkasVideoStudio `video-router`](https://github.com/Orkas-AI/Orkas-VideoStudio/blob/7387d99d468e0cce22508854ba8bca04e79657e1/packages/skills/video-router/SKILL.md), Copyright (c) 2026 Orkas, under the MIT License.
