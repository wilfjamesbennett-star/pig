# Outlaw Rush

A 3D open-world mix of GTA and Fortnite that runs in the browser (Three.js, no build step).

- **Drop in** by parachute over a 600 m city of skyscrapers, parks and traffic-filled streets
- **GTA**: steal any car (even moving traffic), drive, crash, explode, run people over
- **Fortnite**: 24 AI rivals, shrinking storm, loot pickups, and **build mode** (walls, floors, ramps)
- Weapons: pistol, assault rifle, shotgun. Headshots do double damage. Shoot enemy builds to destroy them.

## Run

    python3 -m http.server 8000   # then open http://localhost:8000

Click **PLAY** (mouse is captured; Esc pauses).

| Key | Action |
|---|---|
| WASD / Shift / Space | move / sprint / jump (handbrake in car) |
| Mouse / Click | aim / shoot (place piece in build mode) |
| F | enter / exit car |
| Q | toggle build mode (1 wall · 2 floor · 3 ramp) |
| 1-3, wheel, R | weapons, reload |

## Weekly drops

- **Every Monday 00:00 UTC** the game generates a new batch of skins (3 outfits, 2 gliders, 2 back blings), the same for every player.
- **Every Monday** a scheduled Claude session also adds one hand-made addition (new skin, emote, weapon, map piece…) and logs it below.

### Changelog
- 2026-10-10: Anime cel-shaded skins, lobby / locker / rotating item shop, Vex-Shards currency, weekly drops.
