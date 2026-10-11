# Icarus Dragon

A rideable night dragon for *Icarus*, with physics-based flight, blue fireballs, hunting vision, animated wings and a head that follows your view.

![Icarus Dragon](IcarusDragon.png)

## Installation

Download the files from the [Releases page](https://github.com/djmad/icarusdragon/releases). The paths below assume the default Steam folder `C:\Program Files (x86)\Steam\steamapps\common\Icarus`; adjust them if your Steam library is somewhere else.

The Icarus Mod Manager only installs game data and .pak files. The dragon's logic (flight, fireballs, animations, egg hatching) runs on [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS), which needs one manual step:

1. **UE4SS + dragon logic:** extract `IcarusDragon-Complete_<version>.zip` into `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\`. Afterwards `dwmapi.dll` sits next to `Icarus-Win64-Shipping.exe`, together with a `ue4ss` folder. The zip contains the UE4SS build the mod was tested with, already configured.
   - **UE4SS already installed?** Extract only `IcarusDragon-UE4SS_<version>.zip` into your UE4SS `Mods` folder, e.g. `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\`. The mod starts through its `enabled.txt`.
2. **Game data:** import and install `IcarusDragonIntegration_<version>.exmodz` with the [Icarus Mod Manager](https://github.com/Jimk72/Icarus_Software). It contains the model, animations, items and research.
3. **Play:** start Icarus. Research or buy the dragon egg in the workshop and place it on the ground. After 10 seconds your own adult dragon hatches. Add a saddle and ride.

**Updating:** replace `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon` with the new version and import the new .exmodz.

**Uninstalling:** remove the mod in the Mod Manager and delete `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss\Mods\IcarusDragon`. If you installed the complete zip, you can also delete `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\dwmapi.dll` and `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\ue4ss`.

Single player is tested. Multiplayer is not tested yet.

## Key bindings (while riding the dragon)

- Space: take off / wing flap (tap = climb a step, hold = keep climbing; costs stamina)
- Left Shift: accelerate (costs stamina)
- Left Ctrl: slow down, down to hovering
- Left Alt: descend; near the ground the dragon lands and folds its wings
- W / S: nose down / nose up (loops and rolls are not limited)
- A / D: roll left / right (banked turns)
- Q / E: turn (yaw) left / right
- Left mouse button: blue fireball (the dragon opens its mouth; costs stamina)
- Right mouse button: hunting vision on/off (camera at the dragon's mouth; living creatures green, corpses red, mining nodes blue)
- Mouse: the dragon's head follows your view up to 60 degrees; shots go where you aim (not limited)
- Mount / dismount, saddle, inventory: the normal Icarus mount controls

## Features

- Dragon egg: research or buy it in the workshop and place it on the ground; after 10 seconds it hatches into your own adult dragon (survives saving/loading, never hatches twice).
- Own adult dragon mount with dragon saddles (freight saddle and light saddle) and a dragon whistle to call it back: it flies to you and lands.
- Physics-based flight: speed from diving and climbing (gravity), up to 60 m/s; ground speed up to 6 m/s; no height limit.
- Animated wings: they unfold on takeoff before the dragon lifts off and fold organically along the body on landing; 30 percent shorter span in flight; V-tail and middle fins react to the steering.
- Head follows the rider's view, mouth opens for fireballs and now and then at rest; lying rest pose with the tail curled around the folded wings and the legs tucked in.
- Blue HD fireballs with splash and 6 s burn; your own rider and ridden dragon take only 33 percent; the rider is fire-protected while seated.
- Stamina costs for flapping, sprinting, hovering and shots (from the dragon's own stamina).
- Riding camera raised and pulled back slightly; smooth camera in flight.
- A riderless dragon in the air lands safely by itself.
- Saved dragons get their dragon appearance back after loading.

## Shop

egg research 5000+1000 / buy 2000+300; whistle 750+150 / buy 250+0; freight saddle 2000+400 / buy 1000+150; light saddle 1500+300 / buy 750+100.

## Credits and license

- **Base dragon model:** BlendSwap blend #30054 by its uploader (https://blendswap.com/blend/30054), published there as CC-BY-NC. It was modified and rebuilt for this mod: new rig, rooted wing membranes, fold shapes, head and mouth shapes, and the complete animation set.
- **Mod code, data and pipeline:** © Rene Marhold (djmad), [CC BY-NC 4.0](LICENSE). Non-commercial use only.
- **Game:** Icarus is a game by RocketWerkz. This is an unofficial fan mod.
- **UE4SS:** the complete package includes [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS) (MIT license, see `ue4ss/LICENSE-UE4SS.txt`).
