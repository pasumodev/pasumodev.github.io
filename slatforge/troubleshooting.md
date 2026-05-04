---
title: Troubleshooting
parent: SlatForge
nav_order: 6
layout: default
---

# Troubleshooting

This page helps you resolve common issues with the SlatForge Blender addon.

## Server path invalid

If the addon reports the server path as invalid:

- Ensure the path is accessible from Windows.
- Click on **Set Server Directory**, navigate to the directory where you extracted the SlatForge Server (make sure the path includes the server folder itself) and click on **Set Server Directory** to confirm.
- If the server is detected in the selected directory, Blender will show aconfirmation message and the SlatForge panel will update to indicate that the server is connected and ready to use.
- If necessary. Re-extract the server files and repeat the steps on [Server Configuration](/slatforge/installation.html#server-configuration)

## Server fails to start

- Windows Smart App Control can cause system priviledge errors. Run Blender as administrator and click **Start Server** in the addon panel.
- Make sure the server path points to a valid SlatForge installation.
- Try starting the server manually with `start_server.bat` to see console errors.
- If the server is already running, try running a generation job; the addon detects existing connections.

## Connection issues

- The addon connects to `127.0.0.1:50007`. Ensure there is no firewall or process blocking that port and that it's not being used by another process.
- If the server stops unexpectedly, the UI will report a warning.

## Texture generation issues

- The active object must be a mesh and have valid UVs.
- If the mesh is missing UVs, use Blender’s [UV Unwrap](https://docs.blender.org/manual/en/latest/modeling/meshes/editing/uv.html#unwrap){:target="_blank"} tools.
- Verify that the active object is selected before clicking **Generate Texture**.
- If the operation exits with a warning, correct the mesh or UV data and retry.

## Reprocess Last Mesh button not enabled

- **Reprocess Last Mesh** is only available after a mesh generation job has completed in the current Blender session.
- If it remains disabled, generate a new mesh first.

## Worker errors and debugging

- The addon logs worker errors to the Blender console.
- Review the local SlatForge server `log.txt` or console output for detailed error messages.

## Best practices

- Start with a low-resolution job and low sampling steps for fast feedback.
- Use a clean reference image and a well-unwrapped mesh.
