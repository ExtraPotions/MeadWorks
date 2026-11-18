# MeadWorks Crafting

A crafting window and build menu, stations that work from nearby chests, and building conveniences. Switch each part on or off on the Crafting page of the MeadWorks menu (F8). Needs Meadworks: Core at exactly the same version.

![Workbench chest counts](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Crafting/01-workbench-chest-counts.png)
![Build menu at 56 px](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Crafting/02-hammer-menu-56px.png)
![Cultivator menu](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Crafting/03-cultivator-menu.png)
![Automation stations](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Crafting/05-automation-stations.png)
![Crafting list](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Crafting/06-craft-list.png)
![Crafting grid](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Crafting/07-craft-grid.png)

## What it does

### Crafting
The crafting window opens from your inventory or at a station as the first tab of the window's tab row, with the tabs Craft, Upgrade, Recycle and Enchant. Turn it off with Crafting search, batch and tabs to get the game's window back.

- Search by recipe name or a localized ingredient name, with favorites, category filters, and Ready and Missing groups, in a list or a grid.
- Click an ingredient to see the recipes that use it, then select a recipe from that list.
- Use Track on a recipe to pin it under Tracked on the HUD. Your character keeps up to three pins, showing missing materials based on your bag and nearby chests. Recipe pins hide while enemies are targeting you.
- Craft and Upgrade retain recipe selection and scroll position when switching tabs. Gamepad navigation follows list rows and grid columns, including partial rows.
- A recipe shows its stats, the upgrade baselines, and each requirement with what you carry and what the chests near you hold, as one line.
- Set a quantity or press Max, press Craft to start, then press the same button, now labeled Queue, to queue more batches while crafting. Cancel clears the drawer immediately. A batch waiting for chest materials keeps its quantity and blocks the next batch until delivery settles. Canceling or closing the inventory stops a pending batch from resuming; materials already requested from shared chests still arrive in your inventory once.
- A PvP switch, the station level and Repair all sit at the top. Gamepad navigation follows the active crafting tab and returns to the item grid when the inventory opens.
- Crafting, building, upgrading and enchanting also use the materials in chests near you, within the chest range, and the chest you have open. A chest whose Used for crafting switch is off (set with Inventory) is left out. Quality upgrades use the station's own upgrade craft. Reroll, rarity Upgrade and Fuse gems pull the same way before Equipment spends what is in the bag.
- Repair at crafting stations repairs everything you carry that the station can repair when you use it.
- Without a station, Repair all repairs damaged gear whose recipe needs no crafting station. Each repair costs one of every material used in its level-1 recipe, from your inventory only. Hover over the button for each item's cost and missing materials. The button names a missing material when nothing can be paid for. Repair all skips items you cannot afford, and station-required gear keeps its usual repair rules.
- Station reach multiplies how far you can stand from a crafting station and still use it. It changes crafting stations only, not doors or chests.

### Recycle and Enchant
- **Recycle.** Quality 2 or higher items lose one quality level and return a share of that level's upgrade materials, keeping their augments, custom data and crafter. Quality 1 items are consumed; items with MeadWorks augments cannot be consumed. Durability does not affect returns. Equipped and hotbar items appear in the list; equipped items require confirmation and are unequipped before recycling. Items whose recipes need no crafting station can also be recycled from your inventory. Other items keep their station requirements. Recycle return share sets the percentage of materials returned.
- **Enchant tab.** Socket puts a gem in or returns it intact. Cut socket, within Socket, adds one socket to eligible rarity gear with none. Fuse gems combines three matching gems into the next rarity with 100% success; Reroll replaces one bonus; Upgrade raises rarity within the world boss cap. Costs and odds appear before confirmation. Reroll, Upgrade and Fuse gems take their materials from the same nearby chests as crafting, at the chest range. Runes and Rune Dust are retired. Needs Equipment and a usable station.

Both tabs use the same two-column layout as the recipes: the items on one side, the item and its action on the other.

### Build
- **Compact build menu.** The hammer and cultivator menus become one centered window with the tabs Categories, Materials, Recent and Favorites. Search and Can build filter the grid. Can build starts on. Category counts follow the filter. Typing in search stays in the search field without selecting a piece or triggering gameplay hotkeys. Unaffordable pieces and search misses draw at half opacity. Selection previews keep build cells in place. The chosen piece keeps its gold marker, and hovering a piece shows what it needs from your bag and your chests.
- **Hammer sort.** Orders the hammer's pieces by the game's own order, by name, by material or by crafting station.
- **Wood swap.** With the hammer out, Ctrl+T (the Wood swap key) switches the piece you are placing to the same piece in another wood. The key is set on the Keys page.
- **Show piece stability.** Pointing at a building piece shows how well supported it is, in percent.
- **Repair nearby pieces.** With the hammer's Repair tool, alt-use (Shift + Interact with the default keys) repairs every damaged piece within the repair radius (10 m by default) and shows one count. A plain click still repairs one piece. The game still receives the Use press. Ward access and station rules match hammer repair. Stamina and hammer wear apply; no materials are used.
- **Floors.** A floor overhead (within 10 m) counts as a roof: the room under it is sheltered from rain, building pieces under it take no rain wear, and it counts as cover for resting, getting wet and fires. Fires, smelters, kilns, furnaces and refineries can be placed on floors, and floors do not wear down in the rain.
- **Auto doors.** Player-built doors open as you walk up and close once you have left. Range is measured from the doorway center. Matching wood doors, wood gates, darkwood gates, Dvergr doors, ashwood doors, iron gates and flametal gates with opposite outer hinges act as a double door when each has only the other as a matching neighbor: both open away from you and wait to close until you have left both and both doorways are clear. Closing either leaf by hand releases both until you walk away. A door you open by hand is left alone.

### Stations that work from chests
Open Automation from the Automation button on the Crafting page, or from its tab in the crafting window. It lists the stations near you with contents, progress and Actions.

- Smelters, kilns and furnaces take ore and fuel from chests near them: up to five fuel and five ore every three seconds.
- Cooking stations, ovens and fermenters are filled from chests, and emptied into chests when they are done while Store station output in chests is on.
- What a smelter, kiln, furnace, refinery, windmill, spinning wheel, beehive or sap collector makes goes into a nearby chest, but only when one chest takes the whole batch. Otherwise the station does what the game does, so a batch is never split between a chest and the ground.
- Feed from chests is the main switch for feeding, cooking and storing.
- Stations are grouped by observed contents or whether they are loaded. Contents do not mean a station is producing: it may lack fuel, shelter or another requirement. Loaded production stations show their recorded timer against the recipe duration, rather than a promised completion time. Unloaded rows show distance and a fuel snapshot where applicable, and are read-only. The window searches the station range from you (40 m by default), and the list holds the nearest 40 stations and 20 fires. Fires and torches are listed only while loaded, and a station inside a ward that shuts you out is not listed.
- Feed and Everlit are global server-controlled settings. Station Actions retain owner, ward and reach checks.
- Ingredients from a craft or build that could not be finished are kept for you and handed back, also after you leave and come back.

| Station | Takes from chests | Puts output in a chest | Everlit |
| --- | --- | --- | --- |
| Smelter, kiln, furnace | Ore and fuel | Yes | Smelters only, when switched on. Kilns never |
| Blast furnace | | | Only when switched on |
| Refinery, windmill, spinning wheel, beehive, sap collector | | Yes | Eitr refineries |
| Cooking station, fermenter | What they cook or ferment | Finished food and drink | |
| Torch, fire, hot tub, oven, frost foundry | | | Yes |
| Shield generator | | | Only when switched on |

Station range also sets how far station upgrades can connect to their matching crafting station, preserving any longer native range.

### Everlit
Everlit keeps torches, fires, hot tubs, ovens, eitr refineries and frost foundries lit without fuel. Smelters, blast furnaces and shield generators are covered only if you switch them on. A covered piece needs no fuel and burns none: it runs with an empty store, and Everlit never fills or changes what is stored, so destroying the piece returns exactly what players put in. Turning a switch off brings the game's own fuel use back with the stored amount unchanged. A charcoal kiln and a frigid kiln are never covered, because their wood and ice are what they work on.

Everlit scope picks all kinds, only torches or only fires. Everlit leaves alone lists pieces to skip. Everlit inside wards only covers only what stands inside a ward. Smoke chokes Everlit fires lets a covered fire go out when its smoke cannot escape. The fuel capacity of each kind only sets how much can be added by hand; Native keeps the game's amount.


### Keys
| Key | What it does |
| --- | --- |
| Ctrl+T | With the hammer out, switches the piece you are placing to another wood. Set on the Keys page. |
| Ctrl+B | Toggles the build camera while placing with the hammer. The camera holds its position within the Build camera range as you move. |
| Alt-use (default Shift + Interact) | With the hammer's Repair tool, repairs every damaged piece in range. |

## Settings

Press F8 and open the Crafting page. Every setting row has a hover tip describing its effect. A setting marked Advanced is under the Advanced row of the page. Server controlled values come from the server in multiplayer; admin-lockable values stay personal unless locked. Solo players, hosts and admins can edit gameplay values.

| Name | Default | Policy | What it does |
| --- | --- | --- | --- |
| Crafting search, batch and tabs | On | Personal | Adds search, batch amounts, chest counts and the Recycle and Enchant tabs to the crafting window. |
| Station reach | 2.5 | Admin-lockable | Multiplies how far you can stand from a crafting station and still use it. 1 is the game's own reach (1 to 10). Advanced. |
| Recycle return share % | 50 | Server controlled | The share of an item's materials that recycling gives back, in percent (0 to 100). Advanced. |
| Craft speed | 1 | Server controlled | Multiplies crafting and upgrade speed, with 1 keeping the current speed (0.1 to 10). Advanced. |
| Rested delay | Native (0) | Server controlled | Seconds of rest before Rested is granted; 0 preserves the native delay (0 to 60). Advanced. |
| Compact build menu | On | Personal | Shows the hammer's pieces in the compact MeadWorks menu in place of the game's. |
| Hammer sort | Vanilla | Personal | The order of the pieces in the hammer's menu: the game's own, by name, by material or by crafting station. |
| Wood swap key | Ctrl+T | Personal | Switches the piece you are placing to its other wood while the hammer is out. Advanced. |
| Build camera key | Ctrl+B | Personal | Toggles the build camera while placing with the hammer. |
| Build camera range | 20 | Personal | Maximum distance from the player to the build camera, in meters (5 to 40). |
| Repair nearby pieces | On | Server controlled | Alt-use with the hammer's Repair tool repairs every piece in range, not only the one you point at. |
| Repair radius | 10 | Server controlled | How far that repair reaches, in meters (1 to 50). Advanced. |
| Floors shelter | On | Admin-lockable | A floor above counts as a roof for beds, fires, stations and fermenters. Fires and smelters can stand on floors, and floors take no rain wear. |
| Auto doors | On | Personal | Doors open as you walk up to them and close once you have left. |
| Auto door range | 1.5 | Personal | How near you must be for a door to open, in meters (0.5 to 8). Advanced. |
| Use nearby chests | On | Server controlled | Crafting, upgrading and enchanting also use the materials in chests near you. |
| Chest range | 30 | Server controlled | How far away a chest can be and still be used, in meters (5 to 100). Advanced. |
| Feed from chests | On | Server controlled | Feeds smelters, furnaces, kilns, cooking stations, ovens and fermenters from chests, including fuel added to torches, hearths and campfires. Gates output storage too.|
| Smelter chest range | 10 | Server controlled | How far a smelter reaches for a chest, in meters (2 to 30). Advanced. |
| Store station output in chests | On | Server controlled | Everything a station makes goes into a chest near it, cooked food and drink included. Otherwise finished food and drink stay on the station. Feed from chests must be on. |
| Automation (Open button) |  | Personal view; global switches follow server policy | Opens the automation window, which lists the stations near you with contents, progress and Actions. |
| Station range | 40 | Server controlled | Automation search distance and augment connection range to matching stations, in meters (10 to 100). Longer native augment ranges are preserved. Advanced. |
| Leave each item in chests | 0 | Server controlled | Leaves this many of each item in each direct chest when feeding stations or tames (0 to 100); shared remote chests are excluded while a reserve is set. Advanced. |
| Kitchen rate | 1 | Server controlled | Multiplies cooking, fermentation and sap collection speed together with seasonal rates (0.1 to 10). Advanced. |
| Food never burns | Off | Server controlled | Keeps cooked food from turning into coal while leaving already burned food unchanged. Advanced. |
| Tames eat from chests | Off | Server controlled | Hungry tames eat accepted food from accessible direct chests within their eating range. Advanced. |
| Honey rate | 1 | Server controlled | Multiplies honey production speed together with the season, with 1 keeping the current rate (0.1 to 10). Advanced. |
| Everlit | Off | Server controlled | Covered stations stay lit without fuel and burn none of the fuel that is in them. |
| Everlit scope | All | Server controlled | What Everlit keeps lit: torches, fires, hot tubs, ovens, refineries and frost foundries, or only torches, or only fires. Advanced. |
| Everlit leaves alone | empty | Server controlled | Torches and fires Everlit never keeps lit. Use the game's internal piece names with commas between them. Advanced. |
| Everlit inside wards only | Off | Server controlled | Everlit keeps only what stands inside a ward. Advanced. |
| Smoke chokes Everlit fires | On | Server controlled | A fire kept lit by Everlit still goes out when its smoke cannot escape. Advanced. |
| Everlit diagnostics | Off | Personal | Writes what Everlit does with each torch and fire to the log. Advanced. |
| Night-only torches | Off | Server controlled | Keeps player-placed torches from burning during the day. Advanced. |
| Everlit smelters | Off | Server controlled | Everlit keeps this kind running without fuel. Advanced. |
| Everlit blast furnaces | Off | Server controlled | Everlit keeps this kind running without fuel. Advanced. |
| Everlit shield generators | Off | Server controlled | Everlit keeps this kind running without fuel. Advanced. |
| Torch fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Fire fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Hot tub fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Oven fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Refinery fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Smelter fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Blast furnace fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Shield fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |
| Frost foundry fuel capacity | Native (0) | Server controlled | Fuel capacity, 0 to 1000; 0 preserves the native amount. Advanced. |

Crafting search, batch and tabs, Compact build menu, Hammer sort, Auto doors, Auto door range, Wood swap key, Build camera key, Build camera range and Everlit diagnostics are personal. On a server, the rest are set by the server or can be locked by an admin.

## Known limits

- A smelter on a raised wooden deck falls under the game's own building physics, since it needs stronger support than wood gives off the ground. Give it a stone or iron-reinforced base, or use a floor at ground level.
- The Enchant tab is locked unless Equipment is installed.
- Smelters, blast furnaces and shield generators are not covered by Everlit until you switch them on.
- A charcoal kiln and a frigid kiln always use up their wood and ice.
- Stations that are not loaded cannot be switched from the Automation list.
- A craft or build that would take materials from chests is refused, with nothing taken, while your character cannot keep a refund.
- A station puts its output into a chest only when one chest has room for the whole batch.
- Shared chests and chest preferences are set in Inventory. Without Inventory installed, saved exclusions still apply.

## Compatibility

Needs Core at exactly the same suite version. MeadWorks clients can join servers without MeadWorks and use other mods. A MeadWorks server refuses only a missing, wrong-version or mismatched MeadWorks install. Solo players, hosts and admins retain control of gameplay settings; personal settings stay local.

## Install

Install with a mod manager, or put `meadworks.crafting.dll` in `BepInEx/plugins`. Install Core as well. Install on each player who wants it, and on the server for admin settings and locks.

## License

MIT. Copyright (c) 2026 expDARE.

Existing worlds: old per-object Feed and Everlit flags remain in saves and are ignored. Previously disabled stations now follow global settings. Retired cooking, smelter-feed and per-fire-switch config entries are ignored.
