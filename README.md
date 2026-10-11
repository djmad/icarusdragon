# Icarus Dragon

A rideable night dragon for *Icarus*, with physics-based flight, blue fireballs, hunting vision, animated wings and a head that follows your view.

![Icarus Dragon](IcarusDragon.png)

## Installation

**Full manual: [INSTALL.md](INSTALL.md)**. It covers step-by-step installation, checking, playing, updating, uninstalling and help.

In short (default Steam folder):
1. Extract `IcarusDragon-Complete_<version>.zip` into `C:\Program Files (x86)\Steam\steamapps\common\Icarus\Icarus\Binaries\Win64\`. This installs UE4SS and the dragon logic. The Mod Manager can't install UE4SS mods.
2. Install `IcarusDragonIntegration_<version>.exmodz` with the Icarus Mod Manager: drag it in, add it to the install list, then **Install All Listed Mods**.
3. In the game, research or buy the dragon egg and place it. Your dragon hatches 10 seconds later.

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
