# Circus Jumper

A complete circus-themed platformer in a single HTML file. No build step, no
dependencies, no assets to download. Open `index.html` in any modern browser and
play.

You are the ringmaster. Stomp the clowns, grab the top hat, open the gift
boxes, and reach the big top at the end of the act.

This game was built as a demo of a large language model writing a full, polished
game from a single prompt. The entire codebase was authored by **Qwen3.8-27B**
running locally on an **AMD Ryzen AI Max+ "Strix Halo"** with **128 GB** of
unified memory. No cloud API calls were made; the model ran on-device.

> Note: the game was re-themed from a generic "Mario-style" brief to an original
> circus theme so it does not use any Nintendo characters, names, or artwork. All
> sprites, tiles, levels, and sound in this project are original.

## Run it

There is nothing to install. Just open the file:

```sh
# Option 1: open directly
xdg-open index.html        # Linux
open index.html            # macOS

# Option 2: serve it locally (optional)
python3 -m http.server 8000
# then visit http://localhost:8000
```

Or play the published version on GitHub Pages (URL below).

## Controls

| Key | Action |
| --- | --- |
| Arrow keys / A, D | Move |
| Space / W / Up | Jump |
| Shift | Run |
| P | Pause |
| R | Restart act |
| M | Toggle music |

On phones and tablets, touch buttons appear automatically.

## Features

- Two hand-built acts (day and night themes)
- Small / big power-up states with a top hat
- Stompable clowns and falling-clown enemies
- Gift boxes, breakable bricks, pipes, coins, and moving platforms
- Score, coin, life, and timer HUD
- A flag-pole act-clear sequence and a victory screen
- Procedural pixel-art sprites and parallax backgrounds drawn on a canvas
- A chiptune soundtrack and sound effects generated with the Web Audio API
- Screen shake, particles, and squash-and-stretch animation

Everything is generated at runtime. The sprites, tiles, and sound are all made in
code.

## How it was made

The whole game was produced from one instruction:

> Create a Super Mario clone in JavaScript as a single HTML page. Make the game
> engaging and the graphics as beautiful as possible.

Qwen3.8-27B wrote the HTML, the CSS, and roughly 1,500 lines of JavaScript in one
pass, including the physics, the level data, the sprite generator, and the audio
engine. It was then tested headlessly (with a stubbed browser environment) and a
static level-clearability analysis to confirm both acts are completable. The
artwork was later re-themed to an original circus style.

### Why Strix Halo + 128 GB matters

A 27-billion-parameter model needs a lot of memory to hold its weights and
activations. The Strix Halo's unified memory architecture lets the CPU and GPU
share one large pool, so the full model fits in 128 GB and runs entirely on the
laptop with no external hardware. This demo shows a frontier-class model doing a
real, non-trivial engineering task locally.

## Files

```
index.html   the entire game
README.md    this file
```

## License

MIT. Use it, break it, and build on it freely.
