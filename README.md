# Render Burst - Batch Camera Rendering Add-on for Blender

Render all cameras, one by one, and store the results.

Updated to include some features I wanted - Mark Funston

Original Authors: Aidy Burrows, Gleb Alexandrov, Roman Alexandrov

## Add-on Files in This Repo

- `RenderBurst41.py` for Blender 5.0.1 - This is updated to include the features. Older versions have not.
- `RenderBurst40.py` for Blender 4.0.x
- `RenderBurst28.py` for Blender 2.80+
- `RenderBurst27.py` for Blender 2.79

## Features (`RenderBurst41.py`)

- Render mode filter: `All Cameras` or `Selected Only`
- Output path selector in the `Render Burst` panel (Render Properties)
- Per-camera custom resolution in the Camera Data tab:
  - `Use Custom Resolution`
  - `X` / `Y` resolution fields
- File naming per rendered camera (`<camera_name><extension>`)
- Marker camera binding workaround to avoid repeated camera renders

Note: Animation output formats (`FFMPEG`, `AVI_JPEG`, `AVI_RAW`, `FRAMESERVER`) are not supported by this add-on workflow.

## Install

1. Open Blender.
2. Go to `Edit > Preferences > Add-ons`.
3. Click `Install from Disk...`.
4. Select the script file for your Blender version (for Blender 5.0.1, use `RenderBurst41.py`).
5. Enable the add-on.

## Usage

1. Open `Render Properties > Render Burst`.
2. Choose camera filter mode (`All Cameras` or `Selected Only`).
3. Set `Output Path` in the same panel.
4. Optional per-camera resolution:
   - Select a camera.
   - Open `Camera Data Properties > Render Burst`.
   - Enable `Use Custom Resolution` and set `X` / `Y`.
5. Click `Render!`.

## Notes

- If a camera does not use custom resolution, Render Burst uses the scene resolution.
- Scene resolution is restored after the batch render finishes or is cancelled.
