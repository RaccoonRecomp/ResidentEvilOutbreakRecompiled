# Resident Evil Outbreak Recompiled 1.5.0

The first public release of Resident Evil Outbreak Recompiled: an unofficial PC port of Resident Evil Outbreak
(File #1, USA) for Windows, built by RaccoonRecomp with AI-assisted programming (Claude, Anthropic).

> [!IMPORTANT]
> **The game is prepared on your PC, once.** Nothing of the game is in the download. After you choose your own disc
> image or extracted files, the program prepares the game's code from them on your PC with the free compiler that
> comes with it. This takes about 3 to 6 minutes on a modern PC. Then *Start Game* starts the game.

## Download

| File | Size | SHA-256 |
|---|---|---|
| `ResidentEvilOutbreakRecompiled-1.5.0-Setup.exe` | 53,826,930 bytes | `8c58c2a276ea2cce985aeb26c257e53fef48cf9ecc68d76aa5d62ccc6824edda` |

The setup is not code-signed yet, so Windows SmartScreen may warn about an unrecognized app.

## What you need

- Windows 10 or 11 (64-bit) and a graphics card with Direct3D 11. Vulkan is optional and comes with your graphics
  driver.
- About 450 MB of free disk space.
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

3. The program prepares the game from your game data (*Preparing your game...*). When it says *Game code prepared.*,
   choose *Continue*, then *Start Game*.

## What is in 1.5.0

- **The game preparation.** After you choose your game data, the program prepares the game's code from your own disc
  on your PC, once: converted and compiled there with the included free compiler (LLVM 23.1.2, Apache License 2.0
  with LLVM Exceptions; its licence files are installed with it). Nothing is downloaded for this, and nothing from your
  disc leaves your PC.
  - It takes about 3 to 6 minutes on a modern PC: about 3.5 minutes measured with 2 compiler processes, up to about 6
    when the PC has little free memory. Later starts load the prepared game right away.
  - After you switch on a mod that changes the game's code (the Cheats' game-code cheats, the Modern Camera), *Start
    Game* offers to update the prepared game (*Update Now*): only what changed is compiled again, in about 30 to 60
    seconds.
  - The prepared game was checked against the developer's own build: identical, and not slower. With the Cheats'
    game-code cheats and the Modern Camera on, it matched as well.
  - The prepared game is kept in your profile (`%LOCALAPPDATA%\Resident Evil Outbreak Recompiled\GameCode`).
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
  saves and the prepared game unless you choose to remove them.

## Known limitations

- The Greatest Hits Cheats download carries no code sites. Its cheats marked *game data* or *save data* work; its
  cheats marked *game code* do not act in the game prepared on your PC. (The Cheats and Modern Camera downloads carry
  their code sites.)
- On a PC with Smart App Control or an App Control policy, Windows may block the game file built on your PC. The
  program explains what happened.
- Only the USA release, disc version 2.00, is supported.

## Legal

Unofficial fan project, not affiliated with or endorsed by Capcom. Resident Evil and all related names are trademarks
of Capcom; all copyright and credit for the game belong to Capcom. You need your own legal copy of the game. No game
data is included: no disc image, no game files, no game executable and no game code.
