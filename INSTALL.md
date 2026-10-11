# Icarus Dragon - installation manual

This manual covers installing, checking, playing, updating and uninstalling the mod, plus help when something doesn't work.

All paths assume the default Steam folder `C:\Program Files (x86)\Steam\steamapps\common\Icarus`. If your Steam library is somewhere else, for example `D:\SteamLibrary\steamapps\common\Icarus`, replace the start of each path accordingly.

## What you need

| Part | Purpose | How it gets installed |
|---|---|---|
| `IcarusDragon-Complete_<version>.zip` | UE4SS (Lua script loader) and the dragon logic: flight, fireballs, animations, egg hatching | extracted by hand, **once** |
| `IcarusDragonIntegration_<version>.exmodz` | game data: dragon model, animations, items, research, prices | **Icarus Mod Manager** |

You also need the [Icarus Mod Manager](https://github.com/Jimk72/Icarus_Software) (IMM) by Jimk72, already set up as described in its own readme.

The Mod Manager cannot install UE4SS or Lua mods. That is why the first part is extracted by hand.

Download both files from the [Releases page](https://github.com/djmad/icarusdragon/releases).

## Step 1 - UE4SS and the dragon logic

1. Close Icarus.
2. Open the game folder `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64`.
   - In Steam you can also get there with right click on Icarus -> Manage -> Browse local files, then `Icarus\Binaries\Win64`.
3. Extract `IcarusDragon-Complete_<version>.zip` into this folder. Use right click -> Extract All, set the target to `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64`, and confirm.
4. Check the result. These must exist:
   - `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\dwmapi.dll`, in the same folder as `Icarus-Win64-Shipping.exe`
   - `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\UE4SS.dll`
   - `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\UE4SS-settings.ini`
   - `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon\enabled.txt`

### UE4SS already installed?

Don't extract the complete zip, because it would replace your UE4SS settings. Instead:

1. Extract `IcarusDragon-UE4SS_<version>.zip` into your UE4SS `Mods` folder, normally `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\`.
2. Check that `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon\enabled.txt` exists.

The mod starts through that `enabled.txt`. You don't need to add an entry to `mods.txt`.

## Step 2 - game data with the Icarus Mod Manager

1. Start the Icarus Mod Manager. It asks for admin rights; confirm.
2. Drag `IcarusDragonIntegration_<version>.exmodz` onto the Mod Manager window. Once the mod is listed in the Mod Manager's online list, you can download it there instead.
3. The mod appears in the list of extracted mods on the left as **IcarusDragonIntegration**.
4. Double-click it so it goes into the **Mods to Install** list. Add your other mods there as well.
5. Click **Install All Listed Mods**. The Mod Manager merges everything and writes the mod into the game's mods folder.

## Step 3 - check that it works

1. Start Icarus and load a game.
2. Open `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon\state\evidence\runtime-package-status.txt`. It must contain `source=ue4ss-mod`. If the file is missing, UE4SS didn't start the mod; see *Help* below.
3. In the game, the workshop now offers the dragon items under research and purchase.

## Playing

1. **Egg:** research or buy the **dragon egg** in the workshop (Ren + Exotics) and place it on the ground like any other deployable. After **10 seconds** your own adult dragon hatches next to it.
   - The egg keeps counting after saving and loading.
   - An egg never hatches twice.
2. **Saddle:** buy a **dragon saddle**, either the freight saddle or the light saddle. Open the dragon's inventory and put the saddle in the saddle slot. Then mount it.
3. **Whistle:** put the **dragon whistle** in your hotbar and use it. Your dragon flies to you and lands.
4. **Flying:** see *Key bindings* below. The dragon's stamina pays for flapping, sprinting, hovering and fireballs.

### Key bindings (while riding)

| Key | Action |
|---|---|
| Space | take off / flap wings (tap = climb a step, hold = keep climbing) |
| Left Shift | accelerate |
| Left Ctrl | slow down, down to hovering |
| Left Alt | descend; near the ground the dragon lands and folds its wings |
| W / S | nose down / nose up (loops and rolls are not limited) |
| A / D | roll left / right (banked turns) |
| Q / E | turn left / right |
| Left mouse button | blue fireball |
| Right mouse button | hunting vision on/off (living creatures green, corpses red, mining nodes blue) |
| Mouse | the dragon's head follows your view up to 60 degrees |

## Updating to a new version

1. Close Icarus.
2. Delete `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon`.
3. Extract the new `IcarusDragon-UE4SS_<version>.zip` into `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\`.
4. In the Mod Manager:
   1. Remove the old **IcarusDragonIntegration** entry.
   2. Drag in the new `.exmodz`.
   3. Install all listed mods again.

### After an Icarus game update

In the Mod Manager, run **Update data folder**, then **Install All Listed Mods** again. Don't change anything in `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon`.

## Uninstalling

1. In the Mod Manager, remove **IcarusDragonIntegration** from the list and install the remaining mods again. If it was your only mod, use **Remove All Mods From Game**.
2. Delete `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon`.
3. If you installed the complete zip and use no other UE4SS mods, also delete:
   - `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\dwmapi.dll`
   - `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss`

Owned dragons stay in your save. Without the mod they appear as plain mounts.

## Help

| Problem | Cause / fix |
|---|---|
| `runtime-package-status.txt` is missing | UE4SS didn't start the mod. Check that `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\dwmapi.dll` and `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon\enabled.txt` exist. If you use your own UE4SS with a custom `ModsFolderPath`, put the `IcarusDragon` folder there. |
| The egg doesn't hatch | See `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon\state\evidence\egg-hatch.log`. It must contain `egg watch registered` and, after placing the egg, `egg placed` and `hatched`. If the log is missing, the logic isn't running (see the row above). |
| The dragon looks like a buffalo, or can't fly | The game data (.exmodz) is installed but the logic isn't running. Check step 1. |
| No dragon items in the workshop | The .exmodz isn't installed, or the Mod Manager didn't install it. Repeat step 2 and click **Install All Listed Mods**. |
| The game crashes at start after installing | Temporarily remove `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\dwmapi.dll`. If the game then starts, UE4SS doesn't fit this game version. Please open an issue on GitHub. |

For bug reports, attach the files from `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon\state\evidence\` to an issue at https://github.com/djmad/icarusdragon/issues.

Single player is tested. Multiplayer is not tested yet.
