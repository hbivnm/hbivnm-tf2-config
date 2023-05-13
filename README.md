# HbiVnm's Team Fortress 2 config
These are the config I use, I generally value good visibility and high framerates.

* `hbivnm_config` - Maximize the frames, game looks potato.
* `hbivnm_config_high_optimized` - High framerate config while keeping the visual to a decently high level.
* `hbivnm_config_ultra` - Maximize the visuals. Great for recording or watching STVs.

NOTE: As of 2023-04-14, this config is no longer being designed to be user-friendly. Do what you want with these configs.

## Download
Download the repo. here [HERE](https://github.com/hbivnm/hbivnm-tf2-config/archive/refs/heads/main.zip).

## Installation
1. Remove all mastercomfig-related files in `tf/custom`
2. Remove or backup your current class specific configs
3. Drag and drop (and replace and merge) the "tf" folder (or place things manually)
4. Edit class configs or restore your own to `tf/cfg/user`
5. Edit the following files to your liking:
* `tf/cfg/hbivnm/hbivnm_binds.cfg`
* `tf/cfg/hbivnm/hbivnm_settings.cfg`
* `tf/cfg/hbivnm/hbivnm_userpref.cfg`
6. Add your own commands to `tf/cfg/hbivnm/hbivnm_custom.cfg`
7. Add launch options: `-novid -nojoy -nosteamcontroller -nohltv -particles 1 -precachefontchars -noquicktime -freq 144 +exec hbivnm_config`

**NOTE:** `-freq` should be changed to match your own monitor refresh rate of your monitor.

**NOTE:** This config is compatible with ALL mastercomfig addons.

Here is an overview of where things should be placed:
```
tf/
├─ cfg/
│  ├─ hbivnm/
│  │  ├─ hbivnm_addons.cfg
│  │  ├─ hbivnm_binds.cfg
│  │  ├─ hbivnm_custom.cfg
│  │  ├─ hbivnm_nullmovement.cfg
│  │  ├─ hbivnm_settings.cfg
│  │  └─ hbivnm_userpref.cfg
│  ├─ overrides/
│  │  ├─ demoman.cfg
│  │  ├─ engineer.cfg
│  │  ├─ heavyweapons.cfg
│  │  ├─ medic.cfg
│  │  ├─ pyro.cfg
│  │  ├─ scout.cfg
│  │  ├─ sniper.cfg
│  │  ├─ soldier.cfg
│  │  └─ spy.cfg
│  ├─ user/
│  │  ├─ demoman.cfg
│  │  ├─ engineer.cfg
│  │  ├─ heavyweapons.cfg
│  │  ├─ medic.cfg
│  │  ├─ pyro.cfg
│  │  ├─ scout.cfg
│  │  ├─ sniper.cfg
│  │  ├─ soldier.cfg
│  │  └─ spy.cfg
│  ├─ hbivnm_config.cfg
│  ├─ hbivnm_config_high_optimized.cfg
│  └─ hbivnm_config_ultra.cfg
└─ custom/
   ├─ __Horsie'sViewmodelEditor_vXXXXXX.vpk
   ├─ Engineer FP Overhaul.vpk
   ├─ FlatTexturesV1.vpk
   ├─ hbivnm-tf2-config.vpk
   ├─ mastercomfig-disable-pyroland-addon_vXXXXXX.vpk
   └─ mastercomfig-no-soundscapes-addon_vXXXXXX.vpk
```

## DISCLAIMER
This config is what works best for me and have been tested and used on two separate systems:
- AMD Ryzen 9 3900X
- NVIDIA GTX 1080TI
- 48gb RAM @ 3600MHz
- Windows 10
- TF2 installed on an M.2 NVMe SSD
---
- AMD Ryzen 9 7900X
- NVIDIA RTX 4080
- 64gb RAM @ 5200MHz
- Windows 10 Home
- TF2 installed on an M.2 NVMe SSD

Comments about certain commands within my cfg file might not be accurate for YOU and it could be worth experimenting on your own with my config as a foundation for your own future config :)

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
5. In the "Launch Options" input field, type one of the DirectX levels available (ex. `-dxlevel 100`)
6. Start Team Fortress 2 and let it fully launch
7. Close Team Fortress 2
8. Repeat steps 2, 3, 4
9. In the "Launch Options" input field, remove the previously added launch option (ex. `-dxlevel 100`)

You have now set a new DirectX level.

## NVIDIA Profile Inspector / LOD Tweak
You can alter the LOD (level of detail) bias so all textures render using their low resolution variants, this might give you an increase in performance for low-end systems and might be worth checking out.

You can download NVIDIA Profile Inspector from this repo [here](https://github.com/hbivnm/hbivnm-tf2-config/raw/main/NVIDIA%20Profile%20Inspector/nvidiaProfileInspector.exe).

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
