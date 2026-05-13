---
title: Installation
parent: SlatForge
nav_order: 1
layout: default
---

# Installation

This page explains how to install and configure the SlatForge Blender addon and the local SlatForge server it depends on.

## Requirements

- **Blender**: Version 5.0 or later.
- **Operating System**: Windows 10 or 11.
- **RAM**: 32 GB recommended; 16 GB may work but startup will be very slow.
- **Graphics Card**: Modern NVIDIA GPU with 8+ GB VRAM (RTX 3050 8GB or newer); 12+ GB is recommended for medium/high voxel resolution.
- **Disk Space**: ~32 GB for program files and AI models.

## Addon installation

1.  **Download the files**:
    - Download the `slatforge_addon` and `slatforge_server` archives from your Gumroad account.
    - Alternatively, the SlatForge Server can be downloaded from [GitHub](https://github.com/pasumodev/slatforge-server/releases). Ensure you select a version that matches the addon downloaded from Gumroad.

2.  **Install Blender addon**:
    - Open Blender.
    - Drag the downloaded `slatforge_addon` ZIP file directly into the 3D Viewport in Blender.
    - Click Install in the confirmation pop-up.

3.  **Extract the server files**:
    - Extract the `slatforge_server-win_amd64.7z` file to a location of your choice using **Winrar** or **7-Zip**.

## Server configuration

1.  Open the SlatForge side panel in the 3D viewport.

    ![SlatForge side panel](/assets/addon_side_panel.jpg)

2.  Click on **Set Server Directory**.

    ![Set the SlatForge server directory from the Blender UI](/assets/set_server_directory_button.jpg)

3.  Navigate to the directory where you extracted the SlatForge Server (make sure the path includes the server folder itself) and click on **Set Server Directory** to confirm.

    ![Find the server directory](/assets/set_server_directory_browser.jpg)

    If the server is detected in the selected directory, Blender will show a confirmation message and the SlatForge panel will update to indicate the server is connected and ready to use.

    ![SlatForge UI panel](/assets/addon_interface.jpg)

## Starting the server

{: .important }
If you have Windows Smart App Control enabled in your system, you may need to **run Blender as administrator** before running the next step to download the required AI models.

SlatForge is almost ready to be used. It just need to download and cache all AI models that it requires to function. This is a one-time step.

1.  In the SlatForge sidebar panel, click **Start Server**.

    ![Start server button](/assets/start_server_button.jpg)

2.  Wait until the panel reports **Ready**. The terminal window will display the message `SlatForge Server is ready to receive jobs`.

Subsequent server starts will use cached AI models and you won't need to run Blender as administrator anymore.