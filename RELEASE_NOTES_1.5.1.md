# Resident Evil Outbreak Recompiled 1.5.1

An update of Resident Evil Outbreak Recompiled, the unofficial PC port of Resident Evil Outbreak (File #1, USA) for
Windows, built by RaccoonRecomp with AI-assisted programming (Claude, Anthropic). It makes the high graphics settings
faster, adds the controller's Share and View buttons and the mouse buttons in game, and brings two camera mods: the new
**REO First Person** and **Modern Camera 2.1.0**.

> [!IMPORTANT]
> **The game is prepared on your PC, once.** Nothing of the game is in the download. After you choose your own disc
> image or extracted files, the program prepares the game's code from them on your PC with the free compiler that
> comes with it. This takes about 3 to 6 minutes on a modern PC. Then *Start Game* starts the game.

## Download

| File | Size | SHA-256 |
|---|---|---|
| `ResidentEvilOutbreakRecompiled-1.5.1-Setup.exe` | 244,023,054 bytes | `21aa77b90d2689d863ae76511d89ef5711d097d4f6a8758fb6d0b8c54fe228ef` |

The setup is not code-signed yet, so Windows SmartScreen may warn about an unrecognized app.

## What you need

- Windows 10 or 11 (64-bit) and a graphics card with Direct3D 11. Vulkan is optional and comes with your graphics
  driver.
- About 780 MB of free disk space (the program, its three background videos and the prepared game).
- **Your own legal copy of the game**: Resident Evil Outbreak (USA) for the PlayStation 2, SLUS-20765, disc version
  2.00, as a disc image (`.iso`) or as files extracted from your disc. Other releases are recognized but not supported
  yet. Outbreak File #2 is not supported.

## Install or update

Run the setup. It installs for your Windows user only by default (no administrator rights needed); *Install for all
users* is available too. Your settings, saves and mods live in your Windows profile, so they stay when you install
1.5.1 over 1.5.0. A first install asks for your game data and prepares the game as described in the
[1.5.0 notes](RELEASE_NOTES_1.5.0.md#install).

## What is new in 1.5.1

- **The high graphics settings are drawn faster, with the same pictures.** At 4x resolution with MSAA 4x or 8x, and
  with Downsampling, the Direct3D 11 renderer draws the scene and the item screen with much less GPU time: MSAA 4x and
  8x keep a sample position that all its samples share once, runs of sprites (the item screen's layers, room effects)
  are drawn in a compute pass, and the scene's triangles use smaller shaders of their own. The item screen, which fell
  to about 13 pictures per second in the stairs room between 1F and 2F at 4x with MSAA 8x, now holds 30 pictures per
  second there (measured on the test PC, an RTX 4060 Ti). Every picture is the same as in 1.5.0 (checked frame by
  frame at many settings), and the default settings are untouched.
- **Steadier while other programs run.** The game's threads run on the processor's performance cores, are never
  power-throttled and run above the normal priority, at every timing setting, so other busy programs (recording
  software, for example) disturb the game less.
- **Controller: Share and View** (Xbox Series X|S controller). **Share** opens the program's menu over the running game
  and is Back in the menus, as Escape is; the game never sees it. **View** opens and closes the camera window while a
  camera mod is switched on in Mods (also when the camera's own On / Off is Off); View + Menu stays the program's menu,
  and with no camera mod on View is the game's Select as before.
- **Keyboard and mouse in game.** The right mouse button readies the weapon (R1) and the left mouse button is Cross: it
  fires while the weapon is ready. **Enter** confirms the game's own menus before play (main menu, scenario, character
  and difficulty choices: the new Controls row *Cross in Game Menus*) and is Start in a scenario. The mouse buttons are
  on port 1 of both input layouts; all of them can be rebound on the Controls tab, and an existing `input.ini` gets the
  mouse buttons where they are still free.
- **Camera mods.**
  - The camera window carries the camera mod's own name (the Modern Camera's window is unchanged). With a controller,
    Left and Right move between its Reset to defaults and Close buttons.
  - A camera mod can lock its window (`"locked": true` in its `window_layout.json`): the window and the mod's
    **Configure** page then show every setting with its value, but nothing can be changed and there is no Reset to
    defaults.
  - The program has the room-draw event the camera mods need to draw J's Bar's restroom mirrors with the game's own
    functions.
  - REO First Person has its own code sites, compiled in at the first preparation like the Modern Camera's and the
    Cheats'; a site both camera mods name is compiled in once, and each mod's entry on the Mods tab shows its own name
    for what it switches.
- **The official mods' code sites** in the program are those of Modern Camera 2.1.0, REO First Person 1.0.0 and the
  Cheats 1.2.0.

## The mods

The mods are separate downloads (see the project page). New with this release:

- **REO First Person 1.0.0** ([REO-FirstPerson](https://github.com/RaccoonRecomp/REO-FirstPerson)): an original
  first-person camera. The camera sits in your character's eyes and follows the head, lines up with the gun's sights
  while you aim, and the right stick looks around from her eyes. J's Bar's restroom mirrors show the room reflected.
  Its camera window is locked: you see its settings, but they cannot be changed.
- **Modern Camera 2.1.0** ([REO-ModernCam](https://github.com/RaccoonRecomp/REO-ModernCam)): the camera stays on your
  character (knockbacks, hits, recoil and the game's auto-aim no longer swing it), **Lock On Enemy** (the camera turns
  onto the enemy the game's aim locks onto), the walls and pictures of the rooms stay drawn, J's Bar's restroom mirrors
  show the room reflected, and the controls are the game's own while the camera is handed back to a cutscene.

Use one camera mod at a time: the Mods tab reports a conflict when both are on.

## Known issues

- **Downsampling with the item screen:** with Resolution 4x and Downsampling 2x, the item screen still stays below
  30 pictures per second (measured on the test PC). It is the one setting where that was found.
- **Share needs Bluetooth:** the Share button works only when the controller is connected over Bluetooth. Over USB or
  the Xbox Wireless Adapter Windows does not report it; hold **Back + Start** to open the menu there.
- **Switching a camera mod off during play:** after a camera mod is switched off mid-game, your partners may stand
  somewhere else than where they were.
- The Greatest Hits Cheats download carries no code sites. Its cheats marked *game data* or *save data* work; its
  cheats marked *game code* do not act in the game prepared on your PC.
- On a PC with Smart App Control or an App Control policy, Windows may block the game file built on your PC. The
  program explains what happened.
- Only the USA release, disc version 2.00, is supported.

## Legal

Unofficial fan project, not affiliated with or endorsed by Capcom. Resident Evil and all related names are trademarks
of Capcom; all copyright and credit for the game belong to Capcom. You need your own legal copy of the game. No game
data is included: no disc image, no game files, no game executable and no game code.
