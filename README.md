# Choplifter

> Know what I miss—the old Choplifter game that used to be available on Apple personal computers in the early 1980s. Back when I was a kid in Muncie, Indiana, there was an arcade that had a row of Apple PCs in the back rigged up to play Choplifter. I loved that. Write me a playable version of Choplifter.

A fan homage to the 1982 Apple ][ classic *Choplifter*, written from scratch as a single self-contained HTML file. Retro pixel art, chiptune-style sound effects, and CRT scanlines included — no dependencies, no build step.

## Play

Open `choplifter.html` in any modern browser. That's it.

```sh
open choplifter.html
```

## Mission

64 hostages are being held in four barracks behind enemy lines. Fly your chopper east past the fence, blast open the barracks doors, land nearby, and load up to 16 hostages at a time. Fly them back west and unload on the **H** pad at your base. Rescue all 64 to win — but every hostage lost to crashes, tank fire, or friendly fire counts against you.

## Controls

| Key | Action |
| --- | --- |
| Arrow keys / WASD | Fly |
| Space | Fire (side-facing) or drop bombs (camera-facing) |
| X | Turn to face the camera — bomb mode for hitting tanks |
| M | Toggle sound |
| Enter | Start / return to title |

## Tips

- Land gently. Coming down too fast, or drifting sideways on touchdown, destroys the chopper — along with everyone aboard.
- Shoot the barracks door to release the hostages inside; they'll run to your chopper once you've landed nearby.
- Tanks take two hits from your gun, or one bomb. Watch out — an exploding tank kills anyone standing next to it, and tanks crush hostages as they roll.
- Enemy jets appear once the rescue is underway and fire homing missiles. Shoot them down or stay out of their flight path.
- Stray bullets and bombs can kill hostages on the ground. Check your fire.
- You have three choppers. A perfect run rescues all 64 with none lost.

## Development

Everything — game logic, pixel art, and Web Audio sound — lives in `choplifter.html`. The game runs a fixed 60 Hz update loop on a 512×320 canvas, integer-scaled to the window.

For automated testing, the page exposes a small state object on `window.__game` with the current mode, chopper, barracks, hostages, and rescue counts.

## Credits

An original tribute to Dan Gorlin's *Choplifter* (Brøderbund, 1982). All code and art here are written from scratch; not affiliated with or endorsed by the original rights holders.
