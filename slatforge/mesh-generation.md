---
title: Mesh Generation
parent: SlatForge
nav_order: 3
layout: default
---

# Mesh Generation

This page explains how to generate a 3D mesh from a reference image using the SlatForge Blender addon.

## Required state

- The SlatForge server must be running and ready.
- A reference image must be selected.

## Starting mesh generation

1. In the SlatForge sidebar, click **Generate Mesh**.
2. Adjust the generation settings in the dialog:
   - **Resolution**: Voxel synthesis resolution for the generated mesh.
   - **Target Face Count**: Target polygon count for mesh decimation.
   - **SS Sampling Steps**: Shape synthesis iterations. Determines the number of iterations used to establish the core 3D structure. Higher values improve results but increase generation time.
   - **Shape SLAT Sampling Steps**: Shape refinement iterations. Refines the latent representation to smooth out surfaces and sharpen edges. Higher values improve results but increase generation time.
   - **Remesh**: Enable remeshing as a post-processing step.
   - **Generate Texture**: Enable texture generation during mesh creation.
   - **Texture Size**: Resolution of the generated texture map. Higher values produce more detailed textures but require more computation and memory.
   - **Tex SLAT Sampling Steps**: Texture refinement iterations. Determines the number of iterations used to refine the texture synthesis. Higher values improve texture quality but increase generation time.

   Expand **Advanced** to adjust advanced settings.

3. Confirm the dialog to send the job to the server and wait.

## What happens during generation

- The addon sends a `mesh_from_image` job to the local SlatForge server.
- The server returns a generated GLTF mesh.
- The addon imports the result into Blender.

## Tips

- Use lower resolution and fewer sampling steps for faster iteration.
- Increase resolution and sampling steps to improve detail.

## Advanced Settings

1. ### Shape Structure Generation
   - **SS Guidance Strength**: Dictates how strictly the model follows the reference image's silhouette.
   - **SS Guidance Rescale**: Fine-tunes guidance strength balance to prevent artifacts.
   - **SS Rescale T**: Adjusts guidance noise schedule.

2. ### Shape Structured Latent
   - **Shape SLAT Guidance Strength**: Balances geometric complexity with the structural stability established during shape structure generation.
   - **Shape SLAT Guidance Rescale**: Fine-tunes guidance strength balance to prevent artifacts.
   - **Shape SLAT Rescale T**: Adjusts guidance noise schedule.

3. ### Texture Structured Latent
   - **Tex SLAT Guidance Strength**: This ensures the resulting texture remains faithful to the original reference image.
   - **Tex SLAT Guidance Rescale**: Fine-tunes guidance strength balance to prevent artifacts.
   - **Tex SLAT Rescale T**: Adjusts guidance noise schedule.
