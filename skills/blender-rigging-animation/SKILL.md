---
name: blender-rigging-animation
description: End-to-end workflow for setting up Blender, rigging a character, and creating a simple animation with a clear output (rendered animation).
---

# Blender Rigging & Animation

## Overview

This skill enables Claude to guide a complete workflow in Blender — from setup to rigging to animation and final render.

It is designed to take a static 3D model and turn it into a fully rigged and animated output.

---

## Setup

Before starting:

1. Install Blender (latest version from https://www.blender.org)
2. Open Blender and select **General Project**
3. Delete default cube (optional)
4. Switch to **Animation workspace**
5. Ensure:
   - Timeline is visible
   - Outliner is open
   - Properties panel is accessible

---

## Inputs Required

- A 3D model (imported via `.obj`, `.fbx`, or created manually)
- Basic understanding of viewport navigation (optional)

---

## When to Use This Skill

- Animating characters or objects
- Preparing assets for games or videos
- Creating simple animated clips
- Learning rigging workflows

---

## When NOT to Use

- Static modeling tasks
- Rendering without animation
- Non-3D workflows
- UI/2D design tasks

---

## Example Use Case

> “Create a simple animation of a character waving”

Claude should:

1. Load or create a basic humanoid model
2. Add an armature (skeleton)
3. Rig the model using automatic weights
4. Apply IK constraints to arms
5. Insert keyframes for waving motion
6. Adjust timing for smooth animation
7. Render final animation as video

---

## Workflow

### 1. Model Preparation

- Import or create a model
- Apply transformations:
  - `Ctrl + A → Apply All Transforms`
- Ensure mesh is clean (no overlapping geometry)

---

### 2. Armature Creation

- Add armature: `Shift + A → Armature`
- Enter edit mode
- Create bone hierarchy:
  - Spine
  - Arms
  - Legs
- Align bones with model

---

### 3. Binding (Rigging)

- Select mesh → Shift + select armature
- Press `Ctrl + P → With Automatic Weights`
- Verify deformation by moving bones

---

### 4. Constraint Setup

- Add IK constraints for arms/legs
- Set target bones for control
- Add rotation limits to avoid unnatural movement

---

### 5. Control System

- Create control bones
- Add custom shapes for easier selection
- Organize rig for usability

---

### 6. Animation

- Select a bone
- Insert keyframes (`I → Location/Rotation`)
- Move timeline forward
- Change pose → insert new keyframe
- Use Graph Editor to refine motion

---

### 7. Lighting & Camera (Basic)

- Add light: `Shift + A → Light`
- Position camera: `Ctrl + Alt + 0`
- Frame the subject

---

### 8. Rendering

- Go to Render settings
- Set output format (MP4 recommended)
- Choose frame range
- Click **Render → Render Animation**

---

## Output Expectations

- A fully rigged 3D model
- Smooth animation (e.g., waving motion)
- Exported video file (MP4)
- Clean and reusable rig setup

---

## Execution Strategy (for AI agents)

The agent should:

1. Identify if the task involves animation or rigging
2. Break the task into:
   - setup → rigging → animation → render
3. Guide the user step-by-step through Blender UI actions
4. Validate each stage before moving forward
5. Ensure final output matches requested animation

---

## Best Practices

- Keep rigs simple initially
- Test deformation early
- Use consistent naming for bones
- Avoid over-complicating constraints
- Save versions frequently

---

## Notes

- Rigging quality directly impacts animation quality
- IK systems improve natural movement
- Complex rigs can become difficult to debug
