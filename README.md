# HbiVnm's Team Fortress 2 config
This is the config I use, I value good visibility and high framerates. Hence this config is designed specifically for high framerates and minimizing visual clutters :)

It is a combination of a custom none-preset [mastercom](https://mastercomfig.com/) config along with my own [config file](https://github.com/hbivnm/hbivnm-tf2-config/blob/main/tf/cfg/hbivnm_config.cfg).

## Download
The repository (i.e config) can be downloaded directly [HERE](https://github.com/hbivnm/hbivnm-tf2-config/archive/refs/heads/main.zip).

## DISCLAIMER
This config is what works best for me with the following specs:
- AMD Ryzen 9 3900X
- NVIDIA 1080TI
- 48gb RAM @ 3600MHz
- Windows 10
- TF2 installed on an SSD

Comments about certain commands within my cfg file might not be accurate for YOU and it could be worth experimenting on your own with my config as a foundation for your own future config :)

## Contents
- My own config file for high framerate
- My own config for extremely high graphics (great for watching/recording demos)

Additional content:
- Edited version of [ahud](https://huds.tf/site/s-ahud)
- Class specific configs and overrides
- Custom viewmodels
- Flat texture addon
- Custom mastercomfig none-preset
- mastercomfig disable pyroland addon
- mastercomfig no soudscapes addon
- mastercomfig null cancelling movement addon

## Installation
1. Remove all mastercomfig-related files in `tf/custom`
2. Remove or backup your current class specific configs in `tf/cfg/user`
3. Drag and drop (and replace and merge) the "tf" folder (or place things manually)
4. Add your own commands to `tf/cfg/hbivnm_custom.cfg`
5. Edit class configs or restore your own
6. Add launch options: `-fullscreen -novid -nojoy -nosteamcontroller -noforcemaccel -noquicktime -noipx -particles 1 -precachefontchars -refresh 144 -high -threads 6 +exec hbivnm_config`

**NOTE:** `-refresh` and `-threads` should be changed to match your own monitor refresh rate and hardware.

# Additional customization

## DirectX (dxlevel)
**WARNING: Both of my configs automatically set DirectX level on execution, this process is no longer needed if you don't want to change your default DirectX level for the game.**

**I'd propose the idea of changing the DirectX level by editing my config file directly, simply change the command (`mat_dxlevel`) at the top to the DirectX level you would like to play with.**

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

# Help / FAQ
**Q:** I can't see my own bullet tracers, how can I fix this?

**A:** These are turned off by default in my config, add `r_drawtracers_firstperson 1` and `cl_particle_batch_mode 1` to `tf/cfg/hbivnm_custom.cfg`.
***
**Q:** I can't see flame particles at certain times, how can I fix this?

**A:** This is due to particle batching, add `cl_particle_batch_mode 1` to `tf/cfg/hbivnm_custom.cfg`.
***
