# FreeWorld

A low-poly open-world city game that runs in the browser (three.js). Walk the streets, drive cars through traffic, and shoot or knock over pedestrians.

Open `index.html` in a browser. It is a single self-contained page; the character, cars and weapons are embedded in it. (three.js loads from a CDN, so it needs an internet connection.)

## Controls
- WASD walk, Shift run, mouse to look (drag if not captured), Q/E turn camera, scroll to zoom
- Space or left click: attack / shoot (hold for the SMG)
- Right mouse or hold Z: aim (GTA IV style: tight over-the-shoulder camera, narrower field of view, steadier shots, slower look). Scroll while aiming to zoom further
- 1-5 or R: weapons (fists, baseball bat, pistol, SMG, shotgun). H waves when unarmed
- F get in/out of a car; W/S gas and brake, A/D steer, Space handbrake (hold it while steering to drift: skid marks, tyre smoke and screech)

## Mobile
Touch devices get an on-screen stick (left thumb), drag-to-look (right side) and Fire/Swing/Punch, Weapon, Wave and Drive buttons. In a car the stick steers (analog), you hold Gas to go, Brake to stop or reverse, and the red Hand brake button for handbrake turns and drifts. Hold Fire and slide the same thumb to keep aiming while shooting. The Aim button toggles the zoomed aim view, and the game asks for fullscreen when you tap to play (there is also a fullscreen button; iPhone Safari does not allow it). Append `?touch` to the URL to force touch controls on desktop.

## Weapons
Every weapon is held with both hands: the right hand holds it, and the left hand is placed on a grip point stored in each weapon model (`Grip2_*`) using two-bone IK. The weapon points where the camera aims.
Bullets are traced from the crosshair. Shot pedestrians fall and nearby ones run; cars take damage and are wrecked (they smoke) after enough hits. Infinite ammo.

## Money and the gun shop
You start with fists and $500, and the cash shows top-right in the GTA IV style (with the change underneath). No weapons are owned at the start: walk into the yellow arrow over the door of the GUNS & AMMO shop (yellow marker on the minimap, a short walk from the start), the screen fades into the shop, walk up to the counter and press F (or tap Talk) to talk to the shopkeeper. Browse the weapon board with the arrow keys (or the on-screen arrows) and press Enter / Buy. Walk into the yellow arrow by the inside door to leave. Cash, kills and purchased weapons are saved in the browser.

## Vehicles
There are 20 vehicles in traffic and parked on the kerb: the C1 and V60 plus 18 more in `assets/cars_roster.glb` (saloon, hatchback, coupe, muscle car, roadster, hot hatch, SUV, pickup, van, minibus, taxi, patrol car, ice cream van, kei truck, 4x4, limousine, classic saloon, GT coupe). Each is built from the same parametric body generator in the Blender file, around 500 triangles.

## Ammo and reloading
Guns have a magazine and a reserve. Pistol 12 + 24 reserve, SMG 30 + 60, shotgun 6 + 12. Each shot uses a round (a shotgun blast is one round). Press G (or the Reload button on phones) to reload; you cannot fire while reloading, and switching weapons cancels it. An empty gun with no reserve clicks and tells you to buy more. Buy ammo boxes at the gun shop with the Ammo button (or B) for the gun you have selected.

## Gangs
Three gang compounds (Crimson Dogs, Verdes, Violet Kings; coloured rings on the minimap and a flag you can see from afar) are held by armed members with pistols, SMGs, shotguns and bats. They spot you, take cover-ish positions, strafe and shoot back, so you have health (it slowly regenerates), a damage flash, and a WASTED screen with respawn at the start. Gunfire alerts the whole gang. Kills pay $100 ($150 for a headshot), clearing a turf pays $500 and the gang returns after a few minutes. Members use the same two-handed weapon IK as the player. Shooting, bats and cars all hurt them.

## Test range
The park block north-west of the start (orange marker on the minimap, orange beam in the sky) is a fenced shooting range: crash-test dummies that wobble, topple and stand back up, a moving dummy, bullseye targets at 20/30/40 m, physics props (crates, barrels, cones, balls) and two cars to shoot or ram. A panel shows shots, hits, accuracy, damage, headshots and target score. Press T (or tap Reset) to reset it. With a gun out the camera sits over the right shoulder, so aim with the crosshair.

## Assets (`assets/`)
- `lowpoly_scene.blend` Blender source for everything below
- `lowpoly_human.glb` low-poly human, 20-bone rig; actions: Idle, Walk, Run, Wave, Punch, plus arm-only Carry1H/Aim1H/Carry2H/Aim2H/Swing for weapons
- `car_c1.glb` Citroen C1 and `car_v60.glb` Volvo V60 (about 500 tris each). Paint is the `Body` material; wheels are two axle meshes (`*_WheelsF`/`*_WheelsR`) that spin on X
- `weapons.glb` bat, pistol, SMG, shotgun (grip at the origin, barrel along +Z, a `Muzzle_*` node at the tip and a `Grip2_*` node for the off hand)









