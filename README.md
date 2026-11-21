# Hover Corpse Loot

**Hover Corpse Loot (HCL)** lets you inspect, loot, and manage dead stalkers' gear straight from a sleek, rounded OLED HUD window right next to your crosshair—without constantly opening the full-screen inventory menu and breaking the flow of combat.

Whether you want to check if a body is worth looting while under fire, vacuum-sweep ammo and meds on the move, field-strip a rifle in seconds, or quickly return an accidental pickup with **Inventory Quick Peek**, Hover Corpse Loot keeps you in the world and in control—working standalone on **Base S.T.A.L.K.E.R. Anomaly 1.5.3** as well as fully integrated into **S.T.A.L.K.E.R. G.A.M.M.A.**

---

## How It Works (Looting & Quick Peek Flow)

Hover Corpse Loot uses a natural **Look first, Scroll to loot** workflow so the UI never gets in the way of a firefight:

1. **Look to Preview (`Preview Mode`):**
   Aim at a dead stalker within range (`2.0 m` by default). After a brief delay (`200 ms` default), the Hover UI opens showing the stalker's name, rank, faction patch, faction color gradient, and sorted gear.
   - **Full Combat Freedom:** While passively looking, **your weapon works normally**—you can shoot, aim down sights, and switch weapons freely if ambushed.
   - **No Premature Triggers:** Glancing at a body will never prematurely trigger cash pickups, stash notifications, quest updates, or body-search animations.
2. **Scroll to Loot (`Loot Mode`):**
   Roll your **Mouse Wheel (`Up` or `Down`)** once to unlock the item cursor:
   - Entering **Loot Mode** automatically collects loose cash, PDA notes, and stash coordinates (once per unlooted body), hands over any quest information carried by the corpse just like opening the vanilla loot menu, triggers optional **FDDA Redone** search animations, and marks the corpse with a **`LOOTED`** badge.
   - Weapon fire, aiming, and weapon switching are temporarily blocked while looting so mouse clicks never fire your gun. Look away at any time to close the window and instantly restore weapon controls.
3. **Swipe to Return (`Inventory Quick Peek`):**
   Grabbed heavy scrap or the wrong item by accident? Hold (or toggle) **`Left Shift`** during **Loot Mode** after taking at least one item to smoothly swipe the window into **Inventory Quick Peek**:
   - Displays items taken from the current body in **most-recent-first (LIFO)** order (automatically breaking onto a new row whenever adjacent items belong to different item kinds) beneath a **horizontally mirrored Right-to-Left player header** showing your name, rank, and disguise-safe true faction patch & gradient.
   - Scroll to highlight any item and press **`Left Click (LMB)`** to return the item or stack straight back to the corpse (automatically swiping back to **Loot Mode** once emptied).
   - **Zero Movement Lockout:** HCL passively observes the Quick Peek key without consuming it, so sprinting and movement are never interrupted.
4. **Classic Inventory Anytime:**
   Prefer the full-screen inventory screen for deep gear comparisons? Pressing your normal **Interact / Use key (`F`)** opens the classic loot menu whenever you want.

---

## Controls & Keybindings

| Input / Action | What It Does |
| :--- | :--- |
| **Aim at a Body** | Opens passive **Preview Mode** (shooting, ADS, and weapon switching remain active). |
| **Mouse Wheel (`Up` / `Down`)** *(First Scroll)* | Unlocks **Loot Mode** (collects loose cash & PDA stashes, hands over corpse quest info, and enables the cursor). |
| **Mouse Wheel (`Up` / `Down`)** | Steps the cursor `1:1` **Left / Right** across the current row (wrapping at row edges). |
| **`Left Alt` + Mouse Wheel (`Up` / `Down`)** | Steps the cursor `1:1` **Up / Down** along the current column. |
| **`Left Click (LMB)`** | **Loot / Return Stack** — Loots the highlighted item or stack in **Loot Mode**, or returns it back to the corpse in **Inventory Quick Peek**. |
| **Hold `Left Click (LMB)` + Mouse Wheel (`Up` / `Down`)** | **Vacuum Sweep** — Rapidly sweeps and loots revealed items along a row as you scroll (scaled by **Cursor Acceleration**), automatically braking at row boundaries until your next scroll input. |
| **`Right Click (RMB)`** | **Loot All / Autoloot** — Loots all revealed items on the corpse by default, or runs **iTheon's Auto Looter** when installed and enabled under **MCM $\rightarrow$ Compatibility**. |
| **`Left Alt` + `Left Click (LMB)`** | **Field Strip Weapon / Unload Magazine** — On a **weapon**, safely detaches silencers, grenade launchers, and scopes and strips internal **WPO** parts at or above your minimum condition threshold (falling back to attachment & ammo stripping without WPO) with a color-coded PDA summary. On a loaded **Anomaly Magazines Redux** magazine, unloads rounds into your inventory at your configured AMR speed. |
| **`Left Alt` + `Right Click (RMB)`** | **Disassemble Item** — Disassembles the highlighted item on the body using a valid disassembly tool in your inventory (`200 ms` click debounce) and refreshes the resulting parts directly into the Hover UI grid. |
| **`Number Keys (1–5)`** | **Quick Row / Category Jump (`1–5`)** — Jumps to **Row `1–5`** *(default: Exact Row)* or matching **Category Slot `1–5`** *(Item Kind mode; press repeatedly to cycle multi-row categories)*. |
| **`Left Alt` + `Number Keys (1–5)`** | **Quick Row / Category Jump (`6–0`)** — Maps keys `1–5` to **`6–10` (`6–0`)** for one-handed navigation without leaving WASD. |
| **`Left Shift`** *(Hold or Toggle)* | **Inventory Quick Peek** — Smoothly swipes into a LIFO view of items looted from the current corpse so you can return items with **`LMB`** *(never blocks sprinting/movement)*. |

> **Tip:** Both **`Left Alt`** (*Universal Modifier Key*) and **`Left Shift`** (*Inventory Quick Peek*) can be freely rebound in MCM.

---

## Handy Features & Visual Indicators

- **Rounded OLED Window, Rolling Scrollbar & Faction Gradients:**
  Features a smooth `5 px` rounded-corner OLED-black frame (`150 px` base height dynamically scaling up to `625 px` with a slim auto-hiding rolling scrollbar that follows your cursor), anti-staircase gradient-faded white header/footer dividers, a clean **Stalker Name + Rank** header, and smooth `.dds` atlas faction gradients across all 14 Zone factions (including **Monolith** Dark Brown, **Trader** Violet, and **Zombified** Midnight Blue).
- **High-Contrast Tactical Pill Badges:**
   Crisp `5 px` rounded pill badges using bold squared **Tactical Fonts** display lettering in solid black all-caps:
  - **`LOOTED`** *(Slate Green header pill)* — Synced directly with Anomaly's native per-corpse looted storage state (retro-compatible with vanilla inventory searches and existing saves).
  - **`CLAIMED`** *(Slate Yellow centered pill)* — Displayed when **Stalker Loot Claim** marks a kill as owned by a nearby NPC, hiding the item grid and blocking rewards, looting, and animations so you never accidentally turn friendly squads hostile.
  - **`EMPTY`** *(Slate White centered pill)* — Cleanly marks empty or cleared bodies.
- **Full Icon Overlays, Vanilla Transfer Callbacks & Clean Audio:**
  Displays condition percentages, weapon/armor part condition dots, repair-type icons, armor faction patches, similar-item stack counts, **Utjan** quest/upgrade/recipe badges, and **SortingPlus** Favorite/Junk highlights. Every item move fires full vanilla `UIInventory` callbacks (preserving ammo stack aggregation, pickup notifications, mod vetoes, and corpse quest-info handovers) and plays clean native per-item take sounds (3DSS / Oleh compatible) without duplicate rucksack audio.
- **Adaptive Footer Bar:**
  Shows the selected item's full name centered in the footer (dynamically truncated with `...` to fit your window width) or a centered, scaled **Looting Takes Time — REDUX** loading spinner while progressive search is underway.

---

## Customization (MCM Settings)

Configure every visual and control detail under **MCM $\rightarrow$ Hover Corpse Loot**:

### 1. `UI Options` Tab
- **Toggle Hover Corpse Loot:** Master on/off switch *(default: `On`)*.
- **Icon Overlay Toggles:** Individually toggle **Condition Percentage**, **Weapon & Armor Parts Condition Dots**, **Repair Type Icons**, and **Armor Faction Patch Icons** *(all `On` by default)*.
- **Horizontal & Vertical Crosshair Offsets (`OFFSET : X` / `OFFSET : Y`):** Position the window anywhere left/right (`-500` to `500 px`, step `10 px`, default `150 px`) and up/down (`-250` to `250 px`, step `10 px`, default `0 px`) relative to your crosshair.
- **Hover UI Horizontal Size (`X Axis`):** Resize window width (`200–500 px`, step `10 px`, default `300 px`).
- **Window Opacity:** Adjust OLED-black background opacity (`10%–100%`, step `1%`, default `75%`).
- **Activation Delay:** Set hover delay before Preview Mode opens (`100–500 ms`, step `10 ms`, default `200 ms`).
- **Maximum Distance:** Set corpse detection & looting reach (`2.0–5.0 m`, step `0.5 m`, default `2.0 m`).

### 2. `UI Controls` Tab
- **Select Cursor Color & Brightness:** Choose **Gold** *(default)*, **Cyan**, **White**, **Green**, or **Blue**, and tune brightness (`1%–100%`, default `75%`).
- **Cursor Acceleration:** Adjust **Vacuum Sweep** scroll acceleration (`1.0–5.0`, step `0.1`, default `1.0`; standard single-cell scrolling always remains `1:1`).
- **Universal Modifier Key:** Rebind the modifier key *(default: `Left Alt`)*.
- **Keyboard Number Key Shortcut Behavior:** **Exact Row** *(default — jumps to Row `1–10`)* or **Item Kind** *(jumps to SortingPlus or built-in Anomaly category slot `1–10`, cycling multi-row categories)*.
- **Inventory Quick Peek & Control Scheme:** Rebind the Quick Peek key *(default: `Left Shift`)* and choose **Hold** *(default)* or **Toggle**.
- **Minimum Weapon Parts Condition to Strip:** Set the minimum durability (`1%–100%`, default `60%`) for **WPO** field-stripping *(automatically dimmed in MCM if Weapon Parts Overhaul is not installed)*.

### 3. `Compatibility` Tab
- **Enable iTheon's Auto Looter Override:** Toggle *(default: `Off`)* whether **`Right Click (RMB)`** triggers **iTheon's Auto Looter** instead of standard **Loot All** *(automatically dimmed in MCM if Auto Looter is not installed)*.

---

## Requirements, Installation & Compatibility

- **Requirements:** **S.T.A.L.K.E.R. Anomaly 1.5.3** with **Modded Exes** (`xray-monolith`) and **Mod Configuration Menu (MCM)**.
- **Installation:** Install via **Mod Organizer 2 (MO2)** (or extract `gamedata` into your Anomaly directory) and enable **Hover Corpse Loot** near the bottom of your UI/QoL load order. Safe to install or update mid-playthrough.
- **Standalone Base Anomaly 1.5.3 Ready:** Works out-of-the-box without G.A.M.M.A. or external UI mods—featuring native similar-item stacking, a 9-category Anomaly sorter (*Weapons, Armor, Ammo, Artifacts/Mutant Parts, Devices/Tools, Food/Drinks, Medical/Drugs, Upgrades, Misc*), standalone condition/parts/repair/patch overlays, and safe attachment + ammo stripping.
- **Automatic 8-Mod Ecosystem & G.A.M.M.A. Integration:**
  1. **SortingPlus (RavenAscendant):** Mirrors your MCM category priority list, Favorites/Junk sort order, icons, and cell highlights.
  2. **Item UI Improvements (Utjan):** Adopts inventory-matching cell styling, similar-item stacking, and quest/upgrade/recipe indicator badges.
  3. **Weapon Parts Overhaul (WPO):** Enables `Modifier + LMB` internal part stripping with minimum-condition filtering and color-coded PDA reports *(auto-dims MCM option if absent)*.
  4. **Anomaly Magazines Redux (AMR):** Enables `Modifier + LMB` remote magazine unloading respecting your AMR MCM unload speed.
  5. **iTheon's Auto Looter:** Optional `Right Click (RMB)` Autolooter override across revealed items *(auto-dims MCM option if absent)*.
  6. **Stalker Loot Claim (G.A.M.M.A.):** Blocks corpse rewards, looting, timed search, and animations on claimed kills with a centered **`CLAIMED`** pill badge.
  7. **FDDA Redone:** Triggers body search animations upon entering **Loot Mode** per your FDDA Redone Body Search MCM settings.
  8. **Looting Takes Time — REDUX (LTTR):** Progressive item reveal with persistent per-corpse revealed-item memory across hover exits and corpse swaps, full silhouette/spinner MCM styling, centered footer loading spinner, and unrevealed-item action protection.
  - Also compatible out-of-the-box with **S.T.A.L.K.E.R. G.A.M.M.A.**, **3DSS / Oleh Take Audio**, **Haruka's Scavenger Skill & Guaranteed Loot mods**, and **Custom UI Font Mods**.

---

## Changelog

### v2.0
- **Inventory Quick Peek (`Left Shift` — Hold or Toggle):**
  - Added a smooth horizontal HUD swipe during **Loot Mode** into a **LIFO** view of items looted from the current corpse (with automatic row breaks between item kinds) so accidental pickups can be returned instantly via **`Scroll`** / **`Modifier + Scroll`** + **`Left Click (LMB)`**.
  - Added a horizontally mirrored **Right-to-Left** player header showing your character's name, rank, and disguise-safe true faction patch & gradient, plus passive key observation that never blocks sprinting or movement.
- **Standalone Anomaly 1.5.3 + 8-Mod Compatibility Architecture:**
  - Complete ground-up v2.0 modular rewrite supporting standalone **Base Anomaly 1.5.3 (`Modded Exes`)** with native similar-item stacking, 9-category fallback sorting, attachment/ammo stripping, and standalone condition/parts/repair/patch overlays.
  - Added seamless runtime integration across **SortingPlus**, **Utjan's Item UI Improvements**, **Weapon Parts Overhaul**, **Anomaly Magazines Redux**, **iTheon's Auto Looter** (moved to a dedicated **`Compatibility`** MCM tab), **Stalker Loot Claim**, **FDDA Redone** (automatic body search animation on **Loot Mode** entry), and **Looting Takes Time — REDUX** (persistent per-corpse revealed items across hover exits/swaps and centered footer spinner), automatically dimming MCM options for uninstalled optional mods.
- **Visual & HUD Overhaul:**
  - Redesigned Hover UI with smooth `5 px` rounded OLED corners (`150 px` base height scaling up to `625 px` with a slim rolling scrollbar), `.dds` atlas faction gradients (including **Monolith** Dark Brown, **Trader** Violet, and **Zombified** Midnight Blue `#2C3E50`), cleaner **Stalker Name + Rank** header layout, **Gold** default cursor + **Blue** cursor option, high-contrast **Tactical Fonts** solid-black-text pill badges (**`LOOTED`**, **`CLAIMED`**, **`EMPTY`**), and signed X/Y crosshair offset sliders (`X: -500..500 px`, `Y: -250..250 px`, step `10 px`).
- **Quest, Transfer & Audio Polish:**
  - Added full vanilla `UIInventory` transfer-callback parity (ammo stack aggregation, mod pre-move vetoes, pickup notifications, and automatic corpse quest-info handover upon entering **Loot Mode**), `200 ms` click debounce, safe muzzle/underbarrel-first weapon attachment stripping, and removal of duplicate default rucksack loot audio so native per-item 3DSS/Oleh take sounds play cleanly.

### v1.1
- **Looting Takes Time - REDUX Compatibility:**
  - Full progressive corpse search support across both **Preview Mode** and **Loot Mode** (pausing cleanly when looking away and resuming where you left off).
  - Supports all **Placeholder Icon** MCM modes: **None** (items appear one by one as found), **Dark Silhouettes** (pure jet-black `RGB 0,0,0` silhouettes framed by a smooth 8-direction white contour border tailored for HCL's dark UI), and **Loading Icon** (jet-black silhouettes with 26 FPS animated spinner overlays respecting your configured spinner style, size, scale mode, and opacity).
  - Added animated `"Searching . . ."` text / indicator bar support, background rummaging audio, automatic SortingPlus re-sorting as items are revealed, and protection preventing unrevealed items from being looted or disassembled early.
- **iTheon's Autolooter Compatibility:**
  - Plain **Right Click (`RMB`)** in **Loot Mode** now delegates to **iTheon's Autolooter** (`z_auto_looter.auto_looter`) when installed and enabled in MCM (respecting your autoloot filters and weapon/part stripping rules), with automatic fallback to built-in **Take All** when absent or disabled.
- **Anomaly Magazines Redux Compatibility:**
  - Pressing **`Left Alt` + `Left Click (LMB)`** on a loaded magazine inside a corpse now unloads rounds directly into your inventory with native timed per-round unloading and live Hover UI stack updates.
- **Item Disassembly (`Left Alt` + `Right Click (RMB)`) Improvements:**
  - Added a `500ms` release-edge debounce to prevent a single `Alt + RMB` click from accidentally disassembling the next adjacent item in the row.
  - Restored vanilla corpse-spawn behavior so disassembled components spawn inside the corpse and automatically refresh and sort into the Hover UI grid.
- **Architecture & Diagnostics:**
  - Added a dedicated centralized debug hub (`hcl_debug.script`) managing the master debug toggle (`debug_level = 0` for public releases) and multi-level `z_probe` chokepoint telemetry across all modules.

### v1.0
- Initial public release of **Hover Corpse Loot**:
  - Two-stage **Preview Mode** and **Loot Mode** HUD workflow (`demonized_geometry_ray` LOS detection, two-phase corpse callbacks, and immediate `[LOOTED]` / `<CLAIMED>` / `<EMPTY>` status tracking).
  - Full 2D grid navigation (`Mouse Wheel`, `Left Alt + Mouse Wheel`, `1–5` and `Left Alt + 1–5` Exact Row / Item Kind category jumping), single-click stack looting, **Vacuum Sweep** with automatic row-boundary braking, and **WPO Field Stripping** (`Left Alt + LMB`).
  - Full **RavenAscendant's SortingPlus** and **Utjan's Item UI Improvements** MCM parity, dynamic footer item-name ellipsis truncation, and customizable MCM layout/color options.
  - Fixed a New Game faction-selection menu crash when `grok_gun_no_condition_text` was autoloaded prior to `on_game_start()`.

<p align="right"><sub><em style="opacity: 0.65;">(Designed using Z and AAMT)</em></sub></p>
<p align="right"><sub><em style="opacity: 0.65;">[GTTIC]</em></sub></p>
