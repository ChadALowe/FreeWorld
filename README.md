# FreeWorld

A low-poly open-world city game that runs in the browser (three.js). Walk the streets, drive cars through traffic, and shoot or knock over pedestrians.

Open `index.html` in a browser. It is a single self-contained page; the character, cars and weapons are embedded in it. (three.js loads from a CDN, so it needs an internet connection.)

## Controls
- WASD walk, Shift run, mouse to look (drag if not captured), Q/E turn camera, scroll to zoom
- Space or left click: attack / shoot (hold for the SMG)
- 1-5 or R: weapons (fists, baseball bat, pistol, SMG, shotgun). H waves when unarmed
- F get in/out of a car; W/S gas and brake, A/D steer, Space handbrake

## Mobile
Touch devices get an on-screen stick (left thumb), drag-to-look (right side) and Fire/Swing/Punch, Weapon, Wave and Drive buttons. In a car the stick steers (analog) and you hold Gas to go and Brake to stop or reverse. Append `?touch` to the URL to force touch controls on desktop.

## Weapons
Bullets are traced from the crosshair. Shot pedestrians fall and nearby ones run; cars take damage and are wrecked (they smoke) after enough hits. Infinite ammo.

## Assets (`assets/`)
- `lowpoly_scene.blend` Blender source for everything below
- `lowpoly_human.glb` low-poly human, 20-bone rig; actions: Idle, Walk, Run, Wave, Punch, plus arm-only Carry1H/Aim1H/Carry2H/Aim2H/Swing for weapons
- `car_c1.glb` Citroen C1 and `car_v60.glb` Volvo V60 (about 500 tris each). Paint is the `Body` material; wheels are two axle meshes (`*_WheelsF`/`*_WheelsR`) that spin on X
- `weapons.glb` bat, pistol, SMG, shotgun (grip at the origin, barrel along +Z, a `Muzzle_*` node at the tip)
