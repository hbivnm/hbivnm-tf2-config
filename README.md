# HbiVnm's Team Fortress 2 config
Config I use for Team Fortress 2, probably not up-to-date.

## Installation
1. Copy the repo [`\tf`](https://github.com/hbivnm/hbivnm-tf2-config/tree/main/tf) contents to your local `...\Team Fortress 2\tf`
2. Add the following launch options: `-console -full -fullscreen -w 1920 -h 1080 -novid -nojoy -nosteamcontroller -nohltv -particles 1 -precachefontchars +exec custom`

# Additional customization

## DirectX (dxlevel)
Team Fortress 2 supports a few different DirectX levels, some give more frames than others, some look better and some are more stable.

### Available DirectX levels
The following are the available DirectX levels supported by the game:

- DirectX 8.0 - `80`
- DirectX 8.1 - `81`
- DirectX 9.0 - `90` 
- DirectX 9.5 - `95` 
- DirectX 9.8 - `98` 
- DirectX 9+ - `100` 

DirectX 8 gives generally **more frames** but **worse looking graphics**.

DirectX 9 gives generally **less frames** but **better looking graphics**.

### How to force set a default DirectX level
1. Open Steam
2. Go to the "Library"
3. Right-click "Team Fortress 2"
4. Select "Properties..." from the menu
5. In the "Launch Options" input field, type one of the DirectX levels available (eg. `-dxlevel 100`)
6. Start Team Fortress 2 and let it fully launch
7. Close Team Fortress 2
8. Repeat steps 2, 3, 4
9. In the "Launch Options" input field, remove the previously added launch option (eg. `-dxlevel 100`)

You have now set a new DirectX level.

## NVIDIA Profile Inspector / LOD Tweak
You can alter the LOD (level of detail) bias so all textures render using their low resolution variants, this might give you an increase in performance for low-end systems and might be worth checking out.

You can download NVIDIA Profile Inspector [here](https://github.com/Orbmu2k/nvidiaProfileInspector/releases).

### How to enable LOD Tweak
1. Close TF2
2. Launch NVIDIA Profile Inspector as Administrator
3. Set profile to: "Team Fortress 2"
4. Scroll down
5. Set `Antialiasing - Transparency Supersampling` to `0x00000008 AA_MODE_REPLAY_MODE_ALL`
6. Set `Texture filtering - LOD Bias (DX)` to `0x00000078` (copy this value if it is not available in the list)
7. Top right hit "Apply changes"
8. Close NVIDIA Profile Inspector
9. Launch TF2
