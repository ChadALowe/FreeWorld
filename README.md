# FreeWorld

A low-poly open-world city game that runs in the browser (three.js). Walk the streets, drive cars through traffic, and knock over pedestrians.

Open `index.html` in a browser. It is a single self-contained page; the character model is embedded in it.

## Controls
- WASD walk, Shift run, Space punch, H wave
- Mouse to look (drag if not captured), Q/E turn camera, scroll to zoom
- F get in/out of a car; W/S gas and brake, A/D steer, Space handbrake

## Mobile
Touch devices get an on-screen stick (left thumb), drag-to-look (right side) and Punch/Wave/Drive buttons. In a car the stick steers (analog) and you hold Gas to go and Brake to stop or reverse. Append `?touch` to the URL to force touch controls on desktop.

## Assets
- `assets/lowpoly_human.blend` Blender source: low-poly human, 20-bone rig, Idle/Walk/Run/Wave/Punch actions
- `assets/lowpoly_human.glb` the same character exported for game engines
- `assets/car_c1.glb` Citroen C1 (about 500 tris), `assets/car_v60.glb` Volvo V60 (about 500 tris). Body paint is the `Body` material, wheels are two axle meshes (`*_WheelsF`/`*_WheelsR`) that spin on X
- `assets/lowpoly_cars.blend` Blender source for both cars (scene also contains the human)


