---
title: Reference Image
parent: SlatForge
nav_order: 2
layout: default
---

# Reference Image

## Preparing the Reference Image

- The SlatForge server must be running and ready.
- Under **Reference Image**, click **Open** to select an image file.
- Alternatively, paste an image from the clipboard: Right-click an image in your web browser and select **Copy**, or capture a screen area, then click **Paste Image From Clipboard** in the SlatForge panel.

{: .tip }
The Windows Snipping Tool is a screen capture application that allows you to capture a screen area. Access it via `Win + Shift + S`.

![Copy and paste screen area](/assets/paste_screen_area.gif)

## Tips for Choosing a Good Reference Image

For optimal mesh generation results, keep these guidelines in mind:

- **Clear subject**: The object or subject should be easily distinguishable. Mesh generation works best with objects that have clear, identifiable geometry.
- **Minimal obstructions**: Avoid images where the subject is partially hidden or obscured. Clear visibility of the entire object improves generation accuracy.
- **Not cropped**: Ensure the subject is completely visible within the image boundaries. The resulting mesh will be cropped the same way as the reference image, so plan accordingly.
- **Decent resolution**: Use images with sufficient resolution to capture fine details. Low-resolution or pixelated images with jagged object borders will produce poor results and confuse the mesh generator.