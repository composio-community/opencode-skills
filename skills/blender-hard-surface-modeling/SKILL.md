---
name: blender-hard-surface-modeling
description: Workflow for creating precise hard surface models in Blender using clean topology, subdivision workflows, bevel systems, and production-ready modeling techniques.
---

# Blender Hard Surface Modeling

## Overview

This skill enables Claude to guide users through creating precise hard surface models in Blender.

The workflow focuses on:
- clean topology
- subdivision modeling
- bevel workflows
- precise edge control
- production-ready geometry
- efficient modeling practices

The goal is to create clean, detailed, and realistic hard surface assets suitable for:
- product renders
- game assets
- sci-fi props
- mechanical objects
- cinematic scenes

Unlike sculpting workflows, hard surface modeling prioritizes precision, edge definition, and controlled geometry.

---

# Setup

Before starting:

1. Install Blender:
   https://www.blender.org

2. Open Blender and create a new project.

3. Switch to the **Modeling Workspace**.

4. Enable useful add-ons:

Edit → Preferences → Add-ons

Recommended:
- LoopTools
- Node Wrangler
- F2
- Extra Mesh Objects

5. Recommended viewport settings:
- enable wireframe overlay
- enable face orientation
- enable cavity shading

Recommended tools:
- Blender
- Graphics tablet (optional)
- Reference images
- Orthographic views

---

# Inputs Required

- Modeling concept or reference
- Mechanical or object design references
- Target asset type:
  - sci-fi prop
  - product model
  - weapon
  - vehicle
  - environment asset

Optional:
- Blueprints
- Orthographic references
- Existing blockouts
- Material references

---

# When to Use This Skill

Use this skill when:
- creating mechanical objects
- building sci-fi assets
- modeling weapons or vehicles
- designing product renders
- creating game-ready props
- building subdivision-ready meshes
- producing clean hard surface geometry

---

# When NOT to Use

Do NOT use this skill for:
- organic sculpting workflows
- character anatomy sculpting
- cloth simulation
- terrain generation
- procedural-only modeling workflows

---

# Example Use Case

> Create a cinematic sci-fi helmet for a product-style render.

Claude should:

1. Analyze reference shapes
2. Block out primary forms
3. Build clean edge loops
4. Apply bevel workflows
5. Maintain subdivision-ready topology
6. Add secondary mechanical details
7. Prepare the model for materials and rendering

Final result should:
- look precise
- maintain clean geometry
- subdivide smoothly
- support realistic materials
- remain production-ready

---

# Core Hard Surface Modeling Principles

## 1. Prioritize Clean Topology

Hard surface models rely heavily on clean geometry.

Good topology improves:
- subdivision quality
- shading consistency
- bevel behavior
- rendering quality

Preferred topology:
- quads whenever possible
- evenly distributed geometry
- controlled edge flow

Avoid:
- unnecessary ngons
- stretched polygons
- chaotic topology

---

## 2. Use Subdivision Modeling Properly

Subdivision workflows are central to hard surface modeling.

Typical workflow:
1. Create low-poly base mesh
2. Add support loops
3. Apply subdivision modifier
4. Control sharpness using bevels and edge placement

Subdivision modeling improves:
- smooth surfaces
- edge control
- realistic curvature

---

## 3. Control Edges With Bevels

Bevels create realistic edge highlights.

Real-world objects rarely have perfectly sharp edges.

Preferred methods:
- bevel modifier
- support loops
- weighted normals

Bevel systems improve:
- realism
- lighting response
- render quality

---

## 4. Start With Large Forms First

Modeling should progress from:
- large shapes
→ medium details
→ small details

Claude should avoid:
- adding tiny details too early
- overcomplicating the mesh initially
- dense geometry during blockout

Strong primary forms create better final models.

---

## 5. Maintain Non-Destructive Workflows

Whenever possible:
- use modifiers
- keep backup geometry
- preserve editable structures

Recommended modifiers:
- Mirror
- Bevel
- Subdivision Surface
- Solidify

Non-destructive workflows improve:
- iteration speed
- flexibility
- debugging

---

# Workflow

## 1. Gather References

Collect:
- front/side references
- material inspiration
- shape language references
- mechanical detail references

Analyze:
- silhouette
- proportions
- panel structure
- edge behavior

Good references improve modeling accuracy significantly.

---

## 2. Create Base Blockout

Start with simple primitives:
- cubes
- cylinders
- planes

Focus on:
- silhouette
- proportions
- primary forms

Avoid detailing during this stage.

The blockout should establish:
- scale
- structure
- major shape language

---

## 3. Build Clean Topology

Refine the mesh using:
- loop cuts
- extrusion
- inset operations
- bevel workflows

Maintain:
- clean edge flow
- subdivision support
- quad-dominant geometry

Check topology regularly using:
- wireframe view
- face orientation
- subdivision preview

---

## 4. Add Secondary Details

After primary forms are stable:
- add panel lines
- vents
- bolts
- mechanical cuts
- layered geometry

Use details to support:
- realism
- functionality
- visual hierarchy

Avoid overcrowding the design.

---

## 5. Apply Modifiers

Use:
- Bevel modifier
- Subdivision Surface
- Weighted Normals
- Mirror modifier

Recommended workflow:
- keep modifiers non-destructive
- apply only when necessary

Validate:
- shading quality
- edge smoothness
- subdivision consistency

---

## 6. Prepare for Materials & Rendering

Before rendering:
- apply proper smoothing
- check normals
- remove geometry artifacts
- optimize topology if needed

Ensure:
- edges catch highlights properly
- surfaces remain smooth
- topology remains clean

---

## 7. Final Validation

Before export or rendering validate:
- topology cleanliness
- subdivision behavior
- shading consistency
- bevel quality
- silhouette readability

Render test images to verify:
- edge highlights
- realism
- material response

---

# Output Expectations

The final output should include:
- clean hard surface geometry
- subdivision-ready topology
- realistic bevel behavior
- production-quality modeling
- render-ready mesh structure

The workflow itself should remain:
- modular
- non-destructive
- reusable
- production-friendly

---

# Execution Strategy (for AI agents)

The agent should:

1. Prioritize large forms before details
2. Maintain clean topology continuously
3. Use subdivision workflows correctly
4. Preserve non-destructive modeling practices
5. Validate shading and edge quality regularly
6. Optimize geometry for rendering consistency

The workflow should optimize for:
- precision
- realism
- topology quality
- rendering quality
- production usability

---

# Best Practices

- Work from large forms to small details
- Keep topology quad-dominant
- Use bevels for realistic highlights
- Validate subdivision frequently
- Avoid unnecessary geometry density
- Use modifiers non-destructively
- Maintain consistent edge flow

---

# Notes

- Clean topology is critical for professional hard surface modeling
- Bevel quality strongly affects realism
- Strong silhouettes matter more than excessive detail
- Subdivision workflows require disciplined edge management
- Good modeling structure improves shading and rendering significantly
