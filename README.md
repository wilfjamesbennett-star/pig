# Outlaw Rush

A 3D open-world mix of GTA and Fortnite that runs in the browser (Three.js, no build step).

- **Drop in** by parachute over a 600 m city of skyscrapers, parks and traffic-filled streets
- **GTA**: steal any car (even moving traffic), drive, crash, explode, run people over
- **Fortnite**: 24 AI rivals, shrinking storm, loot pickups, and **build mode** (walls, floors, ramps)
- Weapons: pistol, assault rifle, shotgun, plus found **SMG, sniper (zoom, 2.5x headshots) and rocket launcher**. Each comes in 5 rarities (common → legendary, up to +50% damage); loot glows in its rarity colour. Keys 1-6 / wheel to switch. Headshots do double damage. Shoot enemy builds to destroy them.
- Rival bots now carry weapons of their own with rarities and tiers (Rookie → Boss): snipers keep their distance, shotgunners rush you, rockets blast, wounded veterans retreat. They drop their gun when eliminated.

## Website

The game is a static site (`index.html` + `three.min.js`). Pushing to `main` deploys it to GitHub Pages via `.github/workflows/pages.yml`. One-time setup: repo **Settings → Pages → Source: GitHub Actions**. Then play at `https://<user>.github.io/pig/`.

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
- 2026-10-12: Added a 💾 SAVE CODE button in the lobby: copy a short save code and load it on any other device or browser (shards, items, stats).
- 2026-10-12: Free Roam and Brick World now autosave (position, cash, ammo, gold bricks, built bricks) and resume when you press PLAY again.
- 2026-10-12: New weapons (SMG, sniper, rocket launcher) with 5 rarity tiers, weapon loot, and smarter bots with weapons and difficulty tiers.
- 2026-10-10: Everything on foot is now first-person in every mode.
- 2026-10-10: Anime cel-shaded skins, lobby / locker / rotating item shop, Vex-Shards currency, weekly drops.
- 2026-10-10: Online play: names + name tags, random rival names, friends list (requests), parties, squad co-op (uses the artifact `room` capability).

## Online play

Open the shared artifact page (people need access via the Share menu). Everyone with the page open appears under **Friends → Players Online**.
- **Add friend** sends a request; they accept it. Friends are saved in the browser.
- **Invite** (creates a party if you are not in one). The invited player joins from Friends → Invites.
- The party leader presses **PLAY SQUAD**; everyone drops together with the same storm and sees each other with name tags, emotes and gunfire.
- Rival bots are simulated on each player's own machine, so bots are not shared between squad members.

## Game modes (pick in the lobby)

| Mode | What it is |
|---|---|
| Battle Royale | 25 players, shrinking storm, build, squads with friends |
| Red vs Blue | 6v6 team deathmatch, first to 30, respawns, team colours |
| Strike Force | 5v5 first-person, first to 40, killstreaks (3 = UAV, 5 = airstrike) |
| Free Roam | open city, wanted level 1-5 with cops/SWAT, cash, carjacking, civilians |
| Brick World | LEGO-style minifigs, unlimited coloured bricks (Q build, 4-9 colours), find 25 gold bricks |

Rewards: 10 Vex-Shards per elimination, 50 for a win (team modes), 50 for finding all gold bricks, up to 100 for leaving Free Roam with cash.
Squads with friends are Battle Royale only.

- 2026-10-10: Added Red vs Blue, Strike Force, Free Roam and Brick World modes.
- 2026-10-10: Minimap arrow now points the way you face; **M** opens a full city map (grid, landmarks, storm, waypoints by clicking); weekly Battle Royale quests (tab + in-match tracker, paid in Vex-Shards).

## Map and quests

- **M**: big map. Click to set/clear a waypoint (shown on the minimap with distance). **M** or **Esc** closes it.
- **Quests** tab: 6 weekly quests, new every Monday 00:00 UTC, progress counts in Battle Royale and rewards are paid as soon as a quest completes. Discover landmarks (parks, towers, plazas) for the landmark quest.
