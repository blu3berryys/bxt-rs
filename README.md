# bxt-rs

Video recording, speedrunning, and TAS tools for Half-Life and mods.

## Features

- **Video recording** ([video tutorial](https://youtu.be/ZMjhCXA82tU)).
- **Interactive TAS editor**: Improved version of the BXT TAS editor ([video tutorial](https://youtu.be/zi3pw9iS1sk)).
- **Brute-force optimizer** for TASes ([video tutorial](https://youtu.be/ECuRruY3XLw)).
- `bxt_hud_scale`: Upscale the HUD for high-resolution video recording.
- Commands to play multiple demos at once (`bxt_play_run`).
- `bxt_force_fov`: Override FOV when `default_fov` doesn't work.
- Fixes for:
  - Command buffer overflow in BXT demos.
  - Non-determinism for TASes.
- Partial implementation of `bxt_tas_log` features, including RNG state dumping.
- Utilities like:
  - `bxt_fade_remove`, `bxt_shake_remove`, `bxt_skybox_remove`
  - `bxt_novis`, `bxt_wallhack`, `bxt_disable_loading_text`.
- Experimental real-time gameplay recording into `.hltas` scripts.

For the full list of features, commands, and variables, see the [wiki page](https://github.com/YaLTeR/bxt-rs/wiki/Features).

> **Note**: This project began as an experiment to re-architect Bunnymod XT from scratch with the benefit of hindsight.

## ⚠️ VAC Ban Warning

Do not connect to VAC-secured servers with bxt-rs to avoid the risk of a VAC ban.

## Usage

### Download

The downloads are from the latest CI run.

Windows release: [here](https://nightly.link/YaLTeR/bxt-rs/workflows/ci/master/bxt-rs-Windows-release.zip)
Windows debug: [here](https://nightly.link/YaLTeR/bxt-rs/workflows/ci/master/bxt-rs-Windows-debug.zip)

Linux release: [here](https://nightly.link/YaLTeR/bxt-rs/workflows/ci/master/bxt-rs-Linux-release.zip)
Linux debug: [here](https://nightly.link/YaLTeR/bxt-rs/workflows/ci/master/bxt-rs-Linux-debug.zip)

### Running bxt-rs

#### Linux
Use the [`runhl.sh`](runhl.sh) script.  
Ensure the paths at the top of the script are correct.

#### Windows
1. Download [Bunnymod XT Injector](https://github.com/YaLTeR/BunnymodXT-Injector/releases).
2. Create a folder containing:
   - `Injector.exe`
   - `bxt_rs.dll`
3. Start Half-Life using the injector:
   ```shell
   Injector.exe path\to\Half-Life\hl.exe
