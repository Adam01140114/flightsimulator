# Halcyon Skies

A three.js flight game over a low-poly mountain island at golden hour. Everything is in a single `index.html`; open it in a browser or serve the folder with any static server.

## Modes

- **Ring Run**: fly through gold rings before the clock runs out. Each ring adds time.
- **Dogfight**: waves of pirate raiders that chase you and shoot back.
- **Free Flight**: no timer, with a few raiders roaming.
- **Versus**: couch (two phones as controllers, connected straight to the computer over your Wi-Fi, split screen) or online (two computers, one link, through the game server). First to five kills wins.

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

## Running it

```
npm install
npm start
```

Then open http://localhost:7070. `server.js` serves the game and runs its
multiplayer rooms (Node, Express and socket.io). The single-player modes need no
server; opening `index.html` directly still works.

- **Couch versus**: open the game on the computer hooked up to the TV, pick
  Versus > Couch, and both players scan the code. When the game is opened on
  localhost, the code uses the computer's Wi-Fi address so phones can reach it.
  Each phone then opens a direct WebRTC link to the TV over your own Wi-Fi, so
  the stick and buttons don't make a round trip to a server; the controller
  shows "⚡ Direct to the TV". If that link can't open, input goes through the
  server instead.
- **Online duel**: Versus > Online gives a link for the other pilot. Duels run
  through the server, so for play over the internet host it somewhere public,
  such as Render.

The game still runs as a Claude artifact too: there, Versus uses the artifact's
live-room feature instead of `server.js`.

## Hosting on Render

`render.yaml` describes the service. In the Render dashboard choose
New > Blueprint and pick this repository; Render installs it, runs
`node server.js`, and redeploys on every push to `main`. Anyone can then open
the game at its onrender.com address and play couch or online versus.
