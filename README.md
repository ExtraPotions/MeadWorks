# MeadWorks

A suite of Valheim mods built on one shared Core. Every module has its own page in the MeadWorks menu (F8), and its settings are on that page.

Version 1.0.0. Back up your worlds and characters before adding any mods, and report problems in Issues.

![HUD](assets/Core/01-hud-56px.png)

## Modules

| Module | What it adds | Install on |
|---|---|---|
| **Core** (required) | Settings menu (F8), server-controlled settings and admin locks, MeadWorks HUD, restyled windows, custom cursor, "who added this item" tooltips | Everyone |
| **Equipment** | Item rarity, gems and sockets, gear bonuses and enchanting, trinkets, special arrows, secondary attacks, loot glow and labels, warm torches | Everyone |
| **Creatures** | Elite creatures with mutations, nameplates, compendium | Everyone |
| **Inventory** | The inventory screen, sorting and stacking, shared and nearby chests, auto pickup, keep on death, auto equip | Everyone |
| **World** | Seasons, seasonal ground and gear frost, winter cold, seasonal crop growth, weather | Everyone |
| **Crafting** | Craft from nearby chests, batch crafting, recycling, smelter and cooking feed, shelter and fire tweaks | Each player |
| **Farming** | Grid planting, wild plants, area harvest, growth timers | Each player |
| **Skills** | Achievements, Trophies and Texts tabs in the inventory, progressive powers | Each player |
| **Cheats** | Safe stamina, loot multiplier, cheat flags, destroy tools | Each player |
| **Dungeons** | Loot chest refill, camp and dungeon respawn | Server |
| **Travel** | Full map with a side panel, pin search and filters; quick portals with distance-scaled waits and local arrival checks | Each player |

Everyone means the server and every player. Each-player mods also go on the server for admin settings and locks. Server means the dedicated server, or the host's game.

### Client and server

- **Core** on a server makes it required on every player who joins. A player without it, or whose suite version or MeadWorks install does not match, is disconnected. A player with MeadWorks can join a server without it; server-controlled settings, locks and server-sent content then stay off, and the player's own settings apply. Other mods do not stop a player with MeadWorks from joining a MeadWorks server. The version check trusts the version a client reports: a mod cannot verify a client's files, so it stops wrong or mismatched installs, not a modified client that reports a matching version.
- **Equipment** adds new items. Install it on the server and on every player, or players without it will see missing items.
- **Creatures, Inventory and World** work best on everyone. Without them on the server, server-controlled settings and server-side parts such as weather don't run. Without them on a player, that player doesn't see the feature.
- **Crafting, Farming, Skills, Cheats** are per player. Put them on the server too so the admin's settings and locks apply.
- **Dungeons** runs where the world runs: the dedicated server, or the host's game.
- **Travel** draws the map and handles quick portals on each player. Install it on the server too to set and lock portal settings; map and weather settings stay personal.

Settings marked as server-controlled use the server's values while you are connected, and your own values come back when you leave.

## Screenshots

| | |
|---|---|
| ![Inventory](assets/Inventory/01-layout3-open-chest.png) | ![Map pins](assets/Travel/02-hover-card.png) |
| ![Workbench](assets/Crafting/01-workbench-chest-counts.png) | ![Compendium](assets/Creatures/03-compendium.png) |
| ![Loot glow](assets/Equipment/02-legendary-loot-glow.png) | ![Gentle Rain](assets/World/02-gentle-rain.png) |

Every module's page below has more.

| Module | Page |
|---|---|
| Core | [Core/README.md](Core/README.md) |
| Inventory | [Inventory/README.md](Inventory/README.md) |
| Crafting | [Crafting/README.md](Crafting/README.md) |
| Equipment | [Equipment/README.md](Equipment/README.md) |
| Farming | [Farming/README.md](Farming/README.md) |
| Skills | [Skills/README.md](Skills/README.md) |
| Creatures | [Creatures/README.md](Creatures/README.md) |
| Dungeons | [Dungeons/README.md](Dungeons/README.md) |
| World | [World/README.md](World/README.md) |
| Travel | [Travel/README.md](Travel/README.md) |
| Cheats | [Cheats/README.md](Cheats/README.md) |

## Install

**With r2modman or Thunderstore Mod Manager.** Install MeadWorks Core and the modules you want; BepInExPack Valheim comes with them.

**By hand.** Install [BepInExPack Valheim](https://thunderstore.io/c/valheim/p/denikson/BepInExPack_Valheim/) first. Then unzip `MeadWorks-Core-<version>.zip` and the modules you want into `BepInEx/plugins/MeadWorks/<Module>/`.

Items in dedicated slots, backpack rows, the coin purse and bag stacks above the game's normal sizes are saved whole in MeadWorks' own part of the character file. Without MeadWorks, only ordinary bag items at normal sizes are visible. The hidden items stay in the character file and return when MeadWorks is installed again.

If a saved pack row is unavailable, its items stay whole in character custody (`+N held`) until a pack provides those rows again, even if the base bag has free cells. Taking off a worn pack normally moves its row items into free bag cells, or refuses removal if they do not fit.

Chests and graves use the game's own save format. Loading them without MeadWorks cuts oversized stacks to the game's normal size and discards the excess. Before removing MeadWorks, move oversized stacks out of chests and collect graves.

## Licence

MIT. Copyright (c) 2026 expDARE.
