# Halcyon Skies

A three.js flight game over a low-poly mountain island at golden hour. Everything is in a single `index.html`; open it in a browser or serve the folder with any static server.

## Modes

- **Ring Run**: fly through gold rings before the clock runs out. Each ring adds time.
- **Dogfight**: waves of pirate raiders that chase you and shoot back.
- **Free Flight**: no timer, with a few raiders roaming.
- **Versus**: couch (two phones as controllers, split screen on the computer) or online (two computers, one link). First to five kills wins.

## Controls

| Action | Keys |
| --- | --- |
| Steer | Mouse, or W/S (nose down/up) and A/D (roll) |
| Fire | Left click or K |
| Rudder | Q / E |
| Throttle | R / F |
| Boost | Space |
| Camera / pause / sound | C / P / M |

Phones and tablets get an on-screen joystick, throttle, fire and boost.

## Note on Versus

Versus uses the live-room feature of Claude artifacts, so it only connects when the game runs as a published artifact on claude.ai and every player is signed in with access to it. Opened from this repo, Versus shows a "not available" message; the single-player modes work everywhere.
