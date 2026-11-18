# MeadWorks Core

The shared base of the MeadWorks suite for Valheim: the settings window, the MeadWorks look for the game's windows and HUD, the title screen, server settings and the rules for joining a server. Every other MeadWorks mod needs it.

![HUD at 56 px](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Core/01-hud-56px.png)
![HUD settings with a hover tip](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Core/02-hud-settings-tip.png)
![General window](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Core/03-general-window.png)
![Five characters at the campfire](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Core/04-campfire-five.png)
![HUD switches](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Core/05-hud-switches.png)
![World settings](https://raw.githubusercontent.com/ExtraPotions/MeadWorks/main/assets/Core/06-world-settings.png)

## What it does

### Settings
Press F8 to open the settings window. It has a General page, a HUD page, a Keys page and one page for every MeadWorks mod and every other installed BepInEx mod, built from its config: switches, sliders, dropdowns, text fields and key binders. Search covers labels and hover tips on every page, including other mods, and groups matches by page. The search stays until the window closes or you clear it. Hover a setting, or move to it with the keyboard or a gamepad, to see what it does and its default value. Changed rows have a small Reset button; it follows the same server permissions as editing the row. Reset page affects only that page, and resets preserve character-owned progress switches. Gamepad focus stays on the selected setting or fold header when a page refreshes; left and right move between controls on one row. While you type in a field, gameplay hotkeys stay out of it. Settings that are advanced sit under an Advanced row of their page, and the pages scroll three rows for every notch of the wheel.

- **Server settings.** On a server, the settings the server controls apply to every player and are never written into your own config. Leave the server and your own values are back.
- **Admin locks.** On a server or a world with other players, the host or an admin gets a small lock button at the right edge of each lockable setting. A locked setting is fixed for other players. The host, admins and solo players are never locked. Locks are saved in `BepInEx/config/meadworks.locks.txt` on the server.
- **No key clashes.** A key already used by a MeadWorks mod, another mod or the game is refused. A key the game's own windows read straight from the keyboard cannot be bound to a MeadWorks action. F8 always opens the menu.

### Title screen and joining
- **Title menu.** The title screen's menu in the MeadWorks look, with up to five of your characters wearing their saved gear around the campfire, most recently played first, each with its name above it (Title campfire character). Click a character or its name to choose it and the camera glides to it. Point at a character and it waves.
- **Character list.** The MeadWorks character list in place of the game's own: a Characters panel with the number of characters, a search box, and one row per character with its name, where the save is kept as the game words it (local or cloud) and when it was last played, newest first. Click a row to choose it and double click it to enter the world. New character, Manage saves and Remove sit under the list. Worlds and servers are chosen in the same flow, on the left. A server password you type at the join prompt is kept.
- **Worlds and servers.** Search saved worlds, create a world with a name and optional seed, inspect its seed and modifiers, and remove a world through the game's confirmation. World modifiers include the game's presets, sliders and switches. Hosting exposes Host server, Crossplay, Community server and password controls. The server browser keeps the game's lists, search, platform filter, refresh, favorites, ordering and address joins. Queued Steam lobby and invite joins continue through character selection. Save-source notices, save errors, duplicate names and online-permission failures remain visible.
- **Character stats and backups.** The selected character shows the game's saved lifetime hours, deaths, boss kills and enemy kills. Hours come from the game's time-in-base and time-out-of-base counters; older saves may have incomplete counters. Before confirming Remove, Core copies the selected character file and verifies it. A failed copy cancels removal. The newest five backups per character and source are kept in `characters_local/MeadWorks-backups/local/<character>/` or `characters_local/MeadWorks-backups/cloud/<character>/` under the game's current save folder. Cloud backups are local copies. The backup guard also applies to the native character picker; Manage saves stays native.
- **Gamepad and keyboard.** Up and down walk the character rows and then the buttons under them, left and right walk the buttons, and Enter or the gamepad's A button on a row starts the world.
- **Mods in the title menu.** Mods opens the MeadWorks settings window before you enter a world.
- **Changelog.** The game's Changelog button opens one window with a MeadWorks tab and a Valheim tab. The mark beside the button lights up after a MeadWorks update until you have opened the notes.
- **Joining.** To join a MeadWorks server you need the same MeadWorks version as the server. A player with MeadWorks can always join a server without it. A player with MeadWorks plus other mods can join a MeadWorks server. Only a missing, wrong-version or mismatched MeadWorks install is refused on a MeadWorks server. On a server without MeadWorks, server settings, locks and content sent by the server stay off, and your own settings apply.

### Look of the game's windows
- **Restyle game windows.** Crafting, inventory, container, trader and text prompt windows, and the title screen's panels, take the MeadWorks look: smoked oak, a few faint bubbles in the lower corners of a window, the MW rune before each window title and a line of light along the top. Corners are 12 px for windows and panels, 8 px for tooltip cards and 6 px for controls and slots. The game's layout and text stay. Off puts the game's look back exactly. Colors, strength and corner radii are in `BepInEx/config/meadworks.theme.json`, read when the game starts (`honey`, `foam`, `honeyStrength`, `radiusWindow`, `radiusTip`, `radius`, `radiusSmall`).
- **Worn items.** A bronze triangle marks the top-left corner of worn item slots in the bag, equipment panel, dedicated slots and hotbar, leaving the rarity color visible.
- **Mod name in tooltips.** An item tooltip ends with the name of the mod that added the item.
- **Pause screen.** The pause menu gets a MeadWorks button under Settings. Cards beside it list the players with distance, host and ping, and show the world's name, day and clock, how long ago it was saved, the MeadWorks version and the number of mods.
- **Text prompt and traders.** The text prompt for signs, portals, pet names and chest labels shows a character counter, and trader prices say what the coins cover.
- **Death card.** While you wait to respawn, a card shows what the death cost, where your grave is, what you kept and where you wake.
- **MeadWorks cursor.** A pointer in the MeadWorks style, drawn at the size you set.
- **Loading screen.** Artwork from the installed game, with the world's or server's name, its day, the loading step and the game's tips standing on it. No loading pictures are included in the mod. If the artwork is unavailable, the game's own loading screen stays visible.

### HUD
The MeadWorks HUD replaces the game's health, stamina and eitr panels with one framed set, and each part has its own switch on the HUD page: vitals with the weapon in hand, its quality and its secondary attack above them, food, mead and ammo beside them, the hotbar, the active effects under the minimap text (Icon, Time, Effect Name), the compass along the top, and the text lines under the minimap. The HUD follows the game's native GUI scale in Accessibility. At larger GUI scales the compass drops below the hotbar and the map-side block stacks below the minimap, with captions and effects following it. The minimap is hidden while the inventory is open. HUD text uses Averia Sans Libre, the font of the game's key hints, in regular weight. Effect rows fit both text columns, including comfort text. Boss powers include their supplied description or power totals on a second line. Thin translucent panels back the compass, effects, weapon text, slot captions and native key hints.

- **Equipped gear.** What you have equipped at the bottom left, with a wear bar for each piece, while the MeadWorks HUD is on: weapon, off hand, helmet, chest and legs while worn, and a cape or utility item when it can wear out. The bar turns red when the piece is nearly worn.
- **Carry weight.** Current/maximum weight in a chip above the bottom-left gear panel. It highlights at 85% of the limit and turns red over it. Inventory changes update the weight; changes to the effective carry limit update the maximum.
- **Pickups and skill gains.** Short rows at the top left in place of the game's own messages. Unlocks use the same rows. Each pickup row shows one number at its right edge: the amount gained. A row for an item you just picked up shows a New tag, and several new build pieces in the same moment become one row.
- **Build card.** The selected piece's card sits just above the bars. It shows only the requirement tiles: each item's icon, name and how many you have. A mode without materials, such as Repair, shows its name.
- **Chat.** The chat in the MeadWorks look. While chat is open, Page Up and Page Down move a page through the game's history, and the mouse wheel over chat moves three lines. Unfocused chat lets clicks pass through to the world. Native input and command history keep their bindings.
- **Key hints.** A bar of key hints at the bottom of the screen for what you can do right now.
- **Feedback.** Screen edge warnings pulses the edges of the screen while your health is low, and flashes them when you have too little eitr for what you tried.
- **Compass pins.** Nearby placed, location and player pins appear with their distances. A pin tracked in Travel stays on the compass at any distance and takes priority over ordinary nearby pins. Other players' shouts and pings appear for the game's chat-marker lifetime, at any distance. Pin names and a range for ordinary map pins are settings. Your last grave shows at any distance while its death pin remains; emptying or destroying that grave removes the pin. Older graves and other players' graves are left alone.

### Compendium
The Compendium is a tab beside the inventory and crafting tabs. It lists what you have discovered, on pages for Recipes, Pieces, Conversions and Items, with a header that shows how many of the entries you have seen, a search box that searches every page at once, and a chip for each page with its count.

- **Discovery.** A page lists only what your character knows. A recipe or piece appears when you learn it, a conversion when you know its station and its input, and an item when you know its material or hold its trophy.
- **Favorites.** A star on every row and on every card marks an entry, and the Marked chip shows only those. Favorites are saved with the character, up to 500.
- **New marks.** Entries you have not looked at yet carry a New mark, counted on the Compendium tab. Clicking an entry clears its mark, and Mark all seen clears them all. A character opened for the first time starts with nothing marked new.
- **Cards.** A card shows where an item or piece comes from (crafted at which station and level, gathered, grown or made in a station), the parts it needs with what you carry, what it makes, its weight, durability, damage and armor, and where it is used. An item's card lists every route that gives it.
- **Conversions.** Smelters, cooking stations, fermenters, beehive honey, and planted seeds and saplings growing into pickables, with their times.
- **Pages from other mods.** Creatures adds a Creatures page (F7 opens it), and Equipment adds Presets and Spellbook pages.

### Saves
- Items MeadWorks could not hand you right away are kept with your character for that world and given to you later, also after you leave and come back.
- **Shorter save pauses.** Map data is saved by copying the explored grids in bulk, and the bytes are checked against the game's own. If they differ, for example after a game update, the bulk copy is switched off for the rest of the session.

## Settings

Press F8 and open the General or HUD page. Everything here is personal. Every setting row has a hover tip describing its effect. A setting marked Advanced is under the Advanced row of its page.

| Name | Default | Policy | What it does |
| --- | --- | --- | --- |
| Restyle game windows | On | Personal | Gives the game's own windows the MeadWorks look. Off puts the game's look back exactly. |
| MeadWorks cursor | On | Personal | Uses the MeadWorks pointer in place of the game's. |
| Cursor size | 32 | Personal | How large the pointer is drawn, in pixels (16 to 96). Advanced. |
| Title menu | On | Personal | Draws the title screen's menu in the MeadWorks look. Advanced. |
| Title campfire character | On | Personal | Shows your recent characters around the campfire on the title screen. Advanced. |
| Character selection | On | Personal | Shows the MeadWorks character list on the title screen in place of the game's own. Advanced. |
| Loading screen | On | Personal | Shows the world's name, the loading step and the game's tips over a full picture while a world loads. Off leaves the game's own loading screen. Advanced. |
| Loading pictures | On | Personal | Chooses from installed artwork and images in the loading folder each time a world loads. Off shows the game's own loading picture. Advanced. |
| Last changelog version | empty | Personal | The last version whose release notes you opened. After an update the mark beside the Changelog button is lit until you open them. Advanced. |
| Death card | On | Personal | Shows a card while you wait to respawn: what the death cost, where your grave is, what you kept and where you wake. Advanced. |
| MeadWorks HUD | On | Personal | Replaces the game's health, stamina and eitr panels with one framed panel. Off puts the game's own back. |
| Hotbar | On | Personal | Draws the hotbar in the MeadWorks look. |
| Compass | On | Personal | Shows nearby map pins, temporary shouts and pings, and the last unrecovered grave with their distances. |
| Minimap text | On | Personal | Shows the lines of text under the minimap. |
| Effects | On | Personal | Draws your active effects in the MeadWorks look. |
| Vitals | On | Personal | Shows the framed health, stamina and eitr bars. |
| Food, mead and ammo | On | Personal | Shows your food, mead and ammo beside the health bars. |
| Gear durability | On | Personal | Shows the durability of your equipped gear at the bottom left. |
| Carry weight | On | Personal | Shows your carry weight and limit above the gear panel, or at the bottom left when gear is hidden. |
| Vitals numbers | On | Personal | Shows the numbers on the health, stamina, eitr and adrenaline bars. |
| Food timers | Always | Personal | Always shows the time left on a food, shows it only in the last minute, or hides it. |
| Pickups and skill gains | On | Personal | Shows pickups and skill gains as short rows at the top left in place of the game's own messages. |
| Chat | On | Personal | Draws the chat in the MeadWorks look. Off leaves the game's own chat. |
| Key hints | On | Personal | Shows a bar of key hints at the bottom of the screen for what you can do right now. |
| Screen edge warnings | On | Personal | Pulses the edges of the screen while your health is low, and flashes them when you have too little eitr for what you tried. |
| Pin names | Off | Personal | Writes the name of each pin under the compass. |
| Pin range | 200 | Personal | How near an ordinary pin must be to show on the compass, in meters (25 to 2000). Tracked pins, shouts, pings and the last grave have unlimited range. |

Keys on the Keys page:

| Name | Default | Policy | What it does |
| --- | --- | --- | --- |
| MeadWorks settings | F8 | Personal, fixed | Opens or closes the settings window. |
| Search in the open panel | None | Personal | Puts the cursor in the search box of the open window. |

### Loading folder

Add PNG or JPEG pictures to `BepInEx/config/MeadWorks/loading/`, and optional UTF-8 tips to `tips.txt` in that folder, one tip per line. Blank lines and lines starting with `#` are ignored. Tips join the game's normal tip list and use its normal controls. Folder contents are read at loading events, with no file watcher. A missing or empty folder keeps the existing behavior; installed loading artwork and any existing artwork notice files are left intact.

Up to 64 image files are considered. Images larger than 16 MiB, 8192 pixels on either side or 32 megapixels are skipped before decoding, and broken images fall back to installed artwork. The tips file can be up to 64 KiB, with up to 256 distinct tips of 512 characters each.

### Translations

Core loads a JSON object of text keys and translations from `config/MeadWorks/lang/<game language>.json` in BepInEx at startup and when you change the game language. Missing keys use English. Core writes `English.json` as the key list.

## Compatibility

Use the same suite version and matching MeadWorks modules on a MeadWorks server. Other installed mods do not prevent joining. MeadWorks clients can join servers without MeadWorks; only a missing, wrong-version or mismatched MeadWorks install on a MeadWorks server is refused. Interface settings stay personal.

## Known limits

- A server without MeadWorks cannot send settings, locks or content. On it only your own settings apply.
- A MeadWorks server needs exactly the same MeadWorks version from every player.
- Items in dedicated slots, backpack rows, the coin purse and bag stacks above the game's normal sizes are saved in the character's own item list, below the game's bag rows and split to the game's normal stack size. With MeadWorks they go back to their slots, rows and purse when the character loads. Without MeadWorks they drop at your feet the first time the character loads, and you decide what to keep. An item only MeadWorks adds, such as a backpack, cannot exist in a game without it: it stays in the character file and returns when MeadWorks is installed again. A quest item the game will not drop is saved in a free bag cell instead; with a full bag it stays in the character file until MeadWorks is installed again.
- Chests and graves use the game's own save format. Loading them without MeadWorks cuts oversized stacks to the game's normal size and discards the excess.
- Release builds ship no console commands.

## Install

Install with a mod manager, or put `meadworks.core.dll` in `BepInEx/plugins`. On a server that runs MeadWorks, every player needs it, at exactly the same version as the server. Install on the server and every player.

## License

MIT. Copyright (c) 2026 expDARE.
