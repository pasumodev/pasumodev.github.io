---
title: Texture Generation
parent: SlatForge
nav_order: 5
layout: default
---

# Texture Generation

This page describes how to generate and apply textures to a mesh using SlatForge.

## Requirements

- The SlatForge server must be running.
- A reference image must be set in the SlatForge panel.
- A valid active mesh selected in Blender.
- The mesh must have valid UV coordinates.

## How to generate textures

1. Select the mesh that should receive the texture.
2. Ensure the selected mesh has a valid UV map. Check [UV Unwrap](https://docs.blender.org/manual/en/latest/modeling/meshes/editing/uv.html#unwrap){:target="_blank"}
3. Click **Generate Texture** in the SlatForge panel.
4. In the dialog, configure:
   - **Texture Size**: Resolution of the generated texture map. Higher values produce more detailed textures but require more computation and memory.
   - **Tex SLAT Sampling Steps**: Texture refinement iterations. Determines the number of iterations used to refine the texture synthesis. Higher values improve texture quality but increase generation time.
   - **Advanced** guidance controls if needed.
5. Confirm to send the texture job.

## What the addon does

- Exports the selected mesh to a temporary PLY file.
- Sends a `textured_from_mesh_and_image` job to the server.
- Imports the textured GLTF result.
- Applies the generated material to the selected mesh objects.
- Removes temporary imported mesh.

## UV and mesh requirements

- The operation checks for active UV layers.
- If the active mesh lacks valid UVs, the addon reports a warning and cancels.
- Use Blender's [UV Unwrap](https://docs.blender.org/manual/en/latest/modeling/meshes/editing/uv.html#unwrap){:target="_blank"} before running texture generation.

## Best practices

- Use a clean UV layout with no overlapping islands for best results.
- Keep the active mesh selected and ensure it is the current object.
