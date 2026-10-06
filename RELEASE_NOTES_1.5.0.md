# Resident Evil Outbreak Recompiled 1.5.0

The first public release of Resident Evil Outbreak Recompiled: an unofficial PC port of Resident Evil Outbreak
(File #1, USA) for Windows, built by RaccoonRecomp with AI-assisted programming (Claude, Anthropic).

> [!IMPORTANT]
> **This version cannot start the game yet.** It installs the program and lets you set up your game data, settings,
> controls and mods. Before the game can start, its code has to be prepared from your own disc on your PC, once.
> **That automatic preparation comes in an update.** Until then, the program says so on its game data screen and at
> *Start Game*.

## Download

| File | Size | SHA-256 |
|---|---|---|
| `ResidentEvilOutbreakRecompiled-1.5.0-Setup.exe` | 5,728,959 bytes | `d17585ab09cb3d42f67369baa0d40416e8876e13b0347b6a1e615c90adb682ff` |

The setup is not code-signed yet, so Windows SmartScreen may warn about an unrecognized app.

## What you need

- Windows 10 or 11 (64-bit) and a graphics card with Direct3D 11. Vulkan is optional and comes with your graphics
  driver.
- **Your own legal copy of the game**: Resident Evil Outbreak (USA) for the PlayStation 2, SLUS-20765, disc version
  2.00, as a disc image (`.iso`) or as files extracted from your disc. Other releases are recognized but not supported
  yet. Outbreak File #2 is not supported.

## Install

1. Run the setup. By default it installs for your Windows user only (no administrator rights needed). *Install for
   all users* is available too.
2. Start **Resident Evil Outbreak Recompiled** and choose your game data. You have three options:
   - select your ISO;
   - select a folder of extracted files;
   - put either one into the installation's empty **ROM** folder. The program then offers it as *Use &lt;name&gt;
     from the ROM folder*.

   Your game data is only read, never modified or copied. Only its location is saved.

## What is in 1.5.0

- **The program and its PC runtime.** The game's code is recompiled to native x64 code and runs at its original
  30 fps. An optional 60 fps mode is available (experimental).
- **Graphics:**
  - Direct3D 11, Vulkan and software renderers.
  - Internal resolution up to 4x or Auto, with downsampling.
  - MSAA up to 8x and FXAA.
  - Texture and anisotropic filtering.
  - Nearest, Bilinear and Sharp Bilinear scaling.
  - Widescreen with HUD placement (experimental).
  - CRT effect, color filters and Reduce Flashing.
- **Controls:**
  - Controllers and keyboard and mouse, fully remappable.
  - PlayStation, Xbox or keyboard button symbols.
  - Compensate Game Deadzone, Mouse Acceleration and Hold To Toggle.
- **Saves:** a virtual memory card in the same raw `.ps2` layout as PCSX2, with backups, Save Profiles and Portable
  Saves.
- **Mods:** the mod framework and its Mods tab. The Modern Camera and the two cheat mods are separate downloads; see
  the project page.
- **The fresh start:** the installation brings an empty ROM folder for your own game data and installs no settings
  file. The program starts on its game data screen.
- **Installer:** installs per-user by default. Repair, Modify and Uninstall are supported, and uninstalling keeps your
  saves unless you choose to remove them.

## Known limitations

- The installed program cannot start the game until the automatic preparation update is released. In-game settings
  and the mods' game-data and save-data cheats take effect from then on. The mods' game-code cheats and the Modern
  Camera also need their code sites compiled into the prepared game; the mod downloads do not carry them, and that
  update has to provide them.
- Only the USA release, disc version 2.00, is supported.

## Legal

Unofficial fan project, not affiliated with or endorsed by Capcom. Resident Evil and all related names are trademarks
of Capcom; all copyright and credit for the game belong to Capcom. You need your own legal copy of the game. No game
data is included: no disc image, no game files, no game executable and no game code.
