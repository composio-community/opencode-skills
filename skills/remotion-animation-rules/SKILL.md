---
name: remotion-animation-rules
description: Workflow for building technically correct Remotion animations using frame-based rendering, spring physics, useCurrentFrame, and Remotion-native animation patterns.
---

# Remotion Animation Rules

## Overview

This skill enables Claude to create technically correct animations in Remotion by following Remotion-native rendering and animation principles.

Unlike traditional frontend animation workflows, Remotion relies entirely on deterministic frame-based rendering instead of browser-driven animation systems.

This workflow focuses on:
- proper use of `useCurrentFrame()`
- spring-driven motion systems
- deterministic rendering
- layout stability
- frame-based timing
- avoiding unsupported animation patterns

The goal is to ensure animations remain smooth, stable, render-safe, and consistent across all frames.

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
- Prettier extension

---

# Inputs Required

- Animation concept
- Video duration
- Scene structure
- Assets:
  - text
  - subtitles
  - images
  - audio

Optional:
- Branding guidelines
- Existing motion references
- Storyboards

---

# When to Use This Skill

Use this skill when:
- creating Remotion animations
- building subtitle systems
- implementing transitions
- designing motion graphics
- creating reusable animation logic
- debugging unstable animations
- optimizing rendering consistency

---

# When NOT to Use

Do NOT use this skill for:
- CSS-based animation systems
- browser-driven transition workflows
- static design tasks
- traditional video editors without React workflows

---

# Example Use Case

> Create animated subtitles for a startup launch video.

Claude should:

1. Use `useCurrentFrame()` for all animation timing
2. Apply spring physics for subtitle motion
3. Avoid CSS transitions entirely
4. Synchronize subtitle appearance frame-by-frame
5. Maintain stable layout dimensions
6. Ensure rendering remains deterministic across exports

Final output should:
- render consistently
- avoid timing glitches
- maintain smooth motion
- prevent layout instability
- remain export-safe

---

# Core Remotion Principles

## 1. Everything Should Be Frame-Based

In Remotion, animation timing should always derive from the current frame.

Preferred APIs:
- `useCurrentFrame()`
- `interpolate()`
- `spring()`

Example:

```tsx
const frame = useCurrentFrame();
```

This ensures:
- deterministic rendering
- precise synchronization
- export consistency

Avoid:
- `setTimeout`
- browser timing systems
- uncontrolled animations

---

## 2. Use Spring Physics for Motion

Motion should use spring-driven systems whenever possible.

Preferred approach:

```tsx
spring({
  frame,
  fps,
  config: {
    damping: 200,
  },
});
```

Spring systems provide:
- smoother easing
- predictable movement
- natural motion behavior

Best use cases:
- scaling
- fade-ins
- subtitle reveals
- slide animations
- transitions

Avoid:
- CSS easing transitions
- uncontrolled interpolation
- browser-driven animation timing

---

## 3. Avoid CSS Transitions Entirely

CSS transitions are not reliable in Remotion workflows.

Incorrect approach:

```css
transition: all 0.3s ease;
```

Problems caused by CSS transitions:
- inconsistent rendering
- export mismatches
- timing instability
- browser-dependent behavior

Preferred approach:
- calculate motion directly from frame values
- use interpolation or springs

---

## 4. Control Layout Stability

A common Remotion issue is layout shifting during animation.

Example issue:
- text jumps while typing animation plays

Recommended fix:
- render invisible full text in background
- overlay animated text separately
- preserve stable layout dimensions

Claude should proactively prevent:
- text reflow
- resizing during animation
- unstable positioning
- dynamic layout shifts

Stable layouts improve:
- render consistency
- subtitle readability
- animation smoothness

---

## 5. Keep Animations Deterministic

Animations should behave identically on every render.

Motion systems should:
- use predictable timing
- avoid randomness
- remain frame-controlled
- synchronize accurately with audio

Deterministic rendering improves:
- export reliability
- debugging
- synchronization
- production stability

---

# Workflow

## 1. Define Animation Structure

Start by identifying:
- video duration
- scene breakdown
- subtitle timing
- transition requirements

Organize the animation into reusable scene components.

Example structure:

```plaintext
scenes/
  Intro.tsx
  Features.tsx
  CTA.tsx
```

---

## 2. Implement Frame Logic

Use `useCurrentFrame()` inside scenes.

Example:

```tsx
const frame = useCurrentFrame();
```

All animation state should derive from frame progression.

---

## 3. Add Motion Systems

Use:
- `spring()`
- `interpolate()`

Preferred animation behaviors:
- smooth movement
- controlled scaling
- timed transitions
- synchronized subtitles

Avoid:
- CSS animation systems
- browser-controlled timing
- uncontrolled easing

---

## 4. Validate Layout Stability

Check for:
- text jumping
- resizing
- subtitle shifts
- unstable positioning

Fix instability before rendering.

---

## 5. Render Final Video

Before export validate:
- timing consistency
- motion smoothness
- subtitle synchronization
- layout stability

Render output:

```bash
npm run build
```

or:

```bash
npx remotion render
```

Preferred export:
- MP4
- platform-optimized settings

---

# Output Expectations

The final output should include:
- smooth frame-based animation
- deterministic rendering
- stable layouts
- synchronized subtitles
- production-ready video export

The workflow itself should remain:
- reusable
- modular
- maintainable
- render-safe

---

# Execution Strategy (for AI agents)

The agent should:

1. Use Remotion-native animation systems only
2. Control all motion frame-by-frame
3. Avoid unsupported browser animation patterns
4. Maintain deterministic rendering behavior
5. Detect and prevent layout instability proactively
6. Validate animation consistency before export

The workflow should optimize for:
- rendering consistency
- timing precision
- layout stability
- smooth motion
- export reliability

---

# Best Practices

- Use `useCurrentFrame()` for all timing
- Prefer spring animations over manual easing
- Keep scenes modular
- Validate animations frame-by-frame
- Avoid layout-dependent motion
- Keep subtitle systems stable
- Reuse motion patterns across scenes

---

# Notes

- `useCurrentFrame()` is central to Remotion workflows
- CSS transitions should never be relied on
- Spring systems produce more natural motion
- Stable layouts significantly improve render quality
- Deterministic rendering is critical for professional video workflows
