# HBIVNM CONFIG for Team Fortress 2
This is the config I use to get as many frames per second as possible :)

It is a combination of a none-preset [mastercom](https://mastercomfig.com/) config along with my own [config file](https://github.com/hbivnm/hbivnm-tf2-config/blob/main/tf/cfg/hbivnm_config.cfg).

## Download
Check out the releases and download [here](https://github.com/hbivnm/hbivnm-tf2-config/releases).

## Contents
- Edited version of [ahud](https://huds.tf/site/s-ahud)
- Custom viewmodels
- No explosion addon
- Flat texture addon
- mastercomfig none-preset
- mastercomfig modules.cfg
- mastercomfig no soudscapes addon
- mastercomfig disable pyroland addon
- mastercomfig null cancelling movement addon
- Class specific configs
- My own config file

## Installation
1. Remove all mastercomfig related files in your current "custom" folder.
2. Remove `tf/cfg/user/modules.cfg` (or create a copy/backup).
3. Drag and drop (and replace and merge) the "tf" folder (or place things manually).
4. Edit class configs or restore your own.
5. Add launch options: `-fullscreen -novid -nojoy -nosteamcontroller -noipx -particles 1 -precachefontchars -noquicktime -noforcemaccel -refresh 144 -high -threads 6 +exec hbivnm_config`.

**NOTE:** `-refresh` and `-threads` should be changed to match your own monitor refresh rate and hardware.

## DirectX (dxlevel)
Team Fortress 2 supports a few different DirectX levels, some give more frames than others, some look better and some are more stable.

### Available DirectX levels
The following are the available DirectX levels supported by the game:
- `80`
- `81`
- `90`
- `95`
- `98`

DX8 gives the most frames but worst looking graphics.

DX9 gives less frames but better looking graphics.

### Tutorial
1. Add launch option `-dxlevel XX` (`XX` - desired DX level).
2. Launch the game fully.
3. Close the game.
4. Remove the launch option you added (`-dxlevel XX`).
5. Done!

## NVIDIA Profile Inspector / LOD Tweak
You can alter the LOD (level of detail) bias so all textures render using their low resolution variants, this might give you an increase in performance for low-end systems and might be worth checking out.

You can download NVIDIA Profile Inspector from this repo [here](https://github.com/hbivnm/hbivnm-tf2-config/raw/main/NVIDIA%20Profile%20Inspector/nvidiaProfileInspector.exe).

### How to enable LOD Tweak
1. Close TF2.
2. Launch NVIDIA Profile Inspector as Administrator.
3. Set profile to: "Team Fortress 2".
4. Scroll down.
5. Set `Antialiasing - Transparency Supersampling` to `0x00000008 AA_MODE_REPLAY_MODE_ALL`.
6. Set `Texture filtering - LOD Bias (DX)` to `0x00000078` (copy this value if it is not available in the list).
7. Top right hit "Apply changes".
8. Close NVIDIA Profile Inspector.
9. Launch TF2.
