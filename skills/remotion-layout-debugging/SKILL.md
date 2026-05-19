---
name: remotion-layout-debugging
description: Workflow for diagnosing and fixing layout instability, text jumping, resizing issues, and rendering inconsistencies in Remotion animations.
---

# Remotion Layout Debugging

## Overview

This skill enables Claude to diagnose and resolve layout instability issues in Remotion projects.

The workflow focuses on:
- fixing text jumping
- preventing layout shifts
- stabilizing animated elements
- debugging resizing issues
- preserving visual consistency
- maintaining deterministic rendering behavior

The goal is to ensure animations remain visually stable and professional even when dynamic content changes during playback.

---

# Setup

Before starting:

1. Install Node.js:
   https://nodejs.org

2. Verify installation:

```bash
node -v
npm -v
```

3. Create a Remotion project:

```bash
npm init video
```

4. Start development server:

```bash
npm run dev
```

5. Open the project in VS Code.

Recommended tools:
- VS Code
- Remotion Preview
- React knowledge
- Browser DevTools

Recommended extensions:
- ES7 React snippets
- Prettier

---

# Inputs Required

- Remotion project
- Reproducible layout issue
- Animated components
- Text or subtitle systems
- Video scenes with unstable positioning

Optional:
- Motion references
- Existing animation logic
- Scene timing information

---

# When to Use This Skill

Use this skill when:
- text jumps during animation
- subtitles resize unpredictably
- animated cards shift position
- layouts become unstable during typing effects
- scene elements flicker or move unexpectedly
- rendering differs between frames
- dynamic content changes cause instability

---

# When NOT to Use

Do NOT use this skill for:
- static layouts
- non-animated UI debugging
- backend issues
- traditional CSS-only workflows
- non-visual rendering problems

---

# Example Use Case

> Fix a subtitle card that jumps vertically while text types onto the screen.

Claude should:

1. Detect layout instability
2. Identify resizing caused by dynamic text length
3. Render invisible full text to preserve container height
4. Overlay animated text separately
5. Keep positioning stable across frames
6. Validate rendering consistency

Final result should:
- eliminate layout jumping
- preserve smooth animation
- maintain stable positioning
- improve readability
- render consistently frame-by-frame

---

# Core Layout Stability Principles

## 1. Prevent Dynamic Resizing

One of the most common causes of layout instability is dynamic resizing during animation.

Examples:
- typing effects changing container height
- subtitles expanding unexpectedly
- animated cards resizing between frames

Claude should proactively detect:
- changing dimensions
- unstable containers
- variable spacing
- reflow-triggering animations

---

## 2. Preserve Stable Layout Dimensions

Stable containers prevent visual jumping.

Recommended strategy:
- render invisible full text in the background
- preserve maximum container dimensions
- overlay animated content separately

Example approach:

```plaintext
Invisible Full Text
↓
Animated Visible Text Overlay
```

This ensures:
- stable height
- stable width
- predictable positioning
- smooth animation

---

## 3. Separate Layout From Animation

Animation logic should not directly control layout structure.

Preferred approach:
- keep layout dimensions fixed
- animate overlays independently
- isolate transforms from containers

Avoid:
- resizing parent containers during animation
- dynamically changing layout flow
- uncontrolled scaling systems

---

## 4. Keep Motion Deterministic

All motion should remain:
- frame-based
- predictable
- synchronized
- render-safe

Preferred systems:
- `useCurrentFrame()`
- `spring()`
- interpolation

Avoid:
- browser timing systems
- uncontrolled transitions
- layout-dependent animations

---

## 5. Validate Frame-by-Frame

Layout issues are often invisible during fast playback.

Claude should inspect:
- individual frames
- subtitle positioning
- container dimensions
- motion synchronization

Frame-level validation improves:
- rendering consistency
- visual polish
- animation stability

---

# Workflow

## 1. Reproduce the Issue

Start by reproducing the layout instability consistently.

Identify:
- when the jump occurs
- which component causes instability
- whether text or motion triggers the issue

Typical symptoms:
- text jumping
- subtitle flickering
- resizing cards
- unstable transitions

---

## 2. Diagnose the Root Cause

Check for:
- changing text dimensions
- dynamic container resizing
- layout reflow
- unstable transforms
- incorrect positioning logic

Determine whether:
- animation affects layout
- layout affects animation
- timing creates instability

---

## 3. Stabilize Container Dimensions

Preserve stable layout sizing.

Recommended fix:
- render invisible full text
- maintain fixed dimensions
- overlay animated content separately

This prevents:
- vertical jumps
- horizontal resizing
- text reflow
- unstable spacing

---

## 4. Isolate Animation Layers

Separate:
- layout structure
- animation overlays
- transforms
- subtitle motion

Example structure:

```plaintext
Stable Container
↓
Invisible Placeholder
↓
Animated Text Overlay
```

This improves:
- render stability
- debugging clarity
- motion consistency

---

## 5. Validate Motion Systems

Check:
- frame synchronization
- spring behavior
- interpolation ranges
- transform stability

Ensure:
- movement remains smooth
- positioning stays consistent
- animation timing remains deterministic

---

## 6. Render & Validate

Before export validate:
- frame-by-frame consistency
- subtitle readability
- stable positioning
- smooth animation
- absence of layout jumping

Render output:

```bash
npm run build
```

or:

```bash
npx remotion render
```

---

# Output Expectations

The final output should include:
- stable animated layouts
- smooth subtitle behavior
- deterministic rendering
- fixed positioning consistency
- production-ready animation quality

The workflow itself should remain:
- reusable
- modular
- easy to debug
- render-safe

---

# Execution Strategy (for AI agents)

The agent should:

1. Detect instability proactively
2. Identify whether layout or animation causes the issue
3. Preserve stable container dimensions
4. Separate layout structure from animation overlays
5. Validate rendering frame-by-frame
6. Ensure deterministic rendering behavior

The workflow should optimize for:
- layout stability
- rendering consistency
- readability
- smooth motion
- professional visual quality

---

# Best Practices

- Keep container dimensions stable
- Avoid layout-dependent animation
- Use invisible placeholders when needed
- Separate overlays from layout structure
- Validate animations frame-by-frame
- Preserve subtitle readability
- Keep transforms isolated from layout flow

---

# Notes

- Most Remotion layout issues come from dynamic resizing
- Stable layouts dramatically improve perceived quality
- Invisible placeholder rendering is often the cleanest solution
- Frame-level validation catches issues early
- Deterministic layouts improve rendering reliability
