# City Drive 3D

A small browser-based 3D driving game prototype. Drive around a procedurally generated city at day or night, dodge pedestrians and AI traffic, and complete pickup-and-deliver missions for cash.

Built with plain HTML, JavaScript and [Three.js](https://threejs.org/). No build step and no install.

> This is an original project. It is not affiliated with or endorsed by Rockstar Games or Take-Two Interactive.

## Play

Live demo: `https://YOUR-USERNAME.github.io/YOUR-REPO/`

(Replace with your own link after deploying, see below.)

## Controls

| Key | Action |
| --- | --- |
| W / Up Arrow | Accelerate |
| S / Down Arrow | Brake / reverse |
| A / Left Arrow | Steer left |
| D / Right Arrow | Steer right |
| Space | Handbrake |
| N | Toggle day / night |
| R | Reset the car to the nearest intersection (if stuck) |

## How to play

1. Drive to the glowing **green** marker to pick up the passenger.
2. Then drive to the **yellow** marker before the timer runs out.
3. Faster deliveries earn a bigger bonus. A late delivery costs $50.
4. Follow the arrow at the top of the screen and the minimap. Blue dots on the minimap are traffic.

## Features

- 10x10 block city with three building styles (single tower, four towers, podium + tower), rooftop details, tree-lined sidewalks and street lights
- Real-time shadows and a day / night cycle with lit windows, glowing street lights and car headlights
- Zebra crosswalks and lane markings on the roads
- Detailed car with spinning and steering wheels, body tilt, and working brake lights
- AI traffic that drives on the right, turns at intersections, and stops for you
- Wandering pedestrians with walking animation that step out of your way
- Pickup and delivery missions with money, a delivery counter, distance and timer
- Per-building collisions, speedometer and minimap

## Project structure

```
.
├── index.html   # the whole game (this is the file GitHub Pages serves)
└── README.md
```

The game file must be named **`index.html`** so GitHub Pages loads it automatically. If your file has a different name, rename it before uploading.

## Deploy to GitHub Pages

### Option A: Upload through the website (no Git needed)

1. Sign in at [github.com](https://github.com) and click **New repository**.
2. Name it (for example `city-drive-3d`), set it to **Public**, and click **Create repository**.
3. Click **uploading an existing file**, then drag in `index.html` and `README.md`.
4. Click **Commit changes**.
5. Go to **Settings > Pages**.
6. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
7. Choose branch **main** and folder **/ (root)**, then click **Save**.
8. Wait 1 to 2 minutes. Your site will be live at:
   `https://YOUR-USERNAME.github.io/city-drive-3d/`

### Option B: Using Git

```bash
git init
git add index.html README.md
git commit -m "Add City Drive 3D"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/city-drive-3d.git
git push -u origin main
```

Then enable Pages in **Settings > Pages** as described in steps 5 to 8 above.

## Troubleshooting

- **404 page:** the file is not named `index.html`, or it is not in the repository root. Rename it and commit again.
- **Black or blank screen:** Three.js is loaded from a CDN, so you need an internet connection. Open the browser console (F12) to check for errors.
- **Choppy frame rate:** shadows and a large city are demanding on older or integrated graphics. In `index.html`, lower `sun.shadow.mapSize` from 2048 to 1024, or reduce `GRID`, `TRAFFIC_COUNT` and `PED_COUNT`.
- **Changes not showing:** GitHub Pages can take a minute to rebuild. Hard refresh with Ctrl+Shift+R.
- **Keys not responding:** click once on the game window to give it focus.

## Known limitations

- Cars, pedestrians and trees are simple shapes built from primitives, not 3D models.
- Handling is arcade-style, not real vehicle physics.
- Traffic does not obey traffic lights and can overlap with other traffic at intersections.
- Trees and street lights have no collision.
- No sound yet.

## Ideas for next steps

- Sound effects and engine audio
- Traffic lights and smarter AI
- Free 3D car and building models loaded with Three.js's GLTFLoader (for example from [Kenney.nl](https://kenney.nl/))
- More mission types and a progression system
- Better handling and drift physics

## License

Choose a license before sharing widely. [MIT](https://choosealicense.com/licenses/mit/) is a common choice for small projects like this. Third-party assets you add later (models, sounds) keep their own licenses.

## Credits

- [Three.js](https://threejs.org/) for 3D rendering
