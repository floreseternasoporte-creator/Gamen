# Pabellón Abandonado — Horror Game

## Overview
A single-file HTML3D horror game set in an abandoned psychiatric hospital. Built with Three.js, featuring a raycasting/3D engine with procedural textures, dynamic lighting, interactive doors, and atmospheric effects.

## Stack
- **Engine**: Three.js (r152, loaded from CDN)
- **Language**: Vanilla HTML/CSS/JavaScript — everything in `index.html`
- **Server**: Python 3 HTTP server (`python3 -m http.server 5000`)

## How to Run
```
python3 -m http.server 5000
```
Open the preview — click **EXPLORAR** to start.

## Controls
- **PC**: WASD + Mouse (click to lock pointer), E to interact with doors
- **Mobile**: Left joystick to move, drag right side to look, ABRIR button to interact

## Architecture (all in `index.html`)
- `generateMaterials()` — procedural textures for floor, walls, ceiling, doors
- `buildDetailedHallway()` — main hospital corridor (~60 units long)
- `buildLobby()` — reception/waiting room area
- `createCeilingLight()` → replaced with `createWallSconce()` — amber wall sconces
- `createWheelchair()` — realistic hospital wheelchair with spoked wheels
- `createHospitalChair()` — room transport chairs
- `buildVendingMachine()` — animated emergency vending machines in lobby
- `buildReceptionDesk()` — L-shaped desk with animated computer screens
- `animate()` — main render loop with flickering lights, animated displays

## User Preferences
- Keep the existing project structure (single-file)
- Spanish language for all in-game text
- Horror/realistic aesthetic — no cartoonish elements
