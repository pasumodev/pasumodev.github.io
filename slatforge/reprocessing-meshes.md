---
title: Reprocessing Meshes
parent: SlatForge
nav_order: 4
layout: default
---

# Reprocessing Meshes

This page explains how to refine the most recently generated mesh using the SlatForge addon.

## When to use reprocessing

- The generated mesh lacks quality.
- The mesh contains visible artifacts.
- You want to change remeshing or texture generation settings after the first job.

## Requirements

- The SlatForge server must be running.
- A mesh generation job must have completed successfully during the current SlatForge Server session.


## Reprocessing workflow

1. Open the SlatForge sidebar panel.
2. Click **Reprocess Last Mesh** next to the **Generate Mesh** button.
   
   ![Reprocess Mesh Button](/assets/reprocess_mesh_button.jpg)
3. In the dialog, adjust:
   - `Target Face Count`
   - `Remesh`
   - `Generate Texture`
   - `Texture Size` (if texture generation is enabled)

4. Confirm to send the reprocessing job to the server.

## What happens

- The addon sends a `reprocess_last_mesh` job using the latest generated mesh.
- The server returns the mesh result.
- The addon imports the new GLTF mesh and replaces the previous result.

## Notes

- If the previous mesh was generated without texture, texture options may not have any effect.
- The reprocess operator is limited to the last mesh produced in the current session.
- Use the panel’s last job timer to confirm that a mesh generation job has completed.
