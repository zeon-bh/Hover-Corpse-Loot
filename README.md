# Hover Corpse Loot

**Hover Corpse Loot (HCL)** lets you inspect and loot dead stalkers straight from a sleek, modern HUD window right next to your crosshair—without constantly opening the full-screen inventory menu and breaking the flow of combat.

Whether you want to quickly check if a body is worth looting while under fire, sweep up ammo and meds on the move, or field-strip a rifle in seconds, Hover Corpse Loot keeps you in the world and in control.

---

## How It Works (Two-Stage Looting Flow)

Hover Corpse Loot uses a natural **Look first, Scroll to loot** flow so the UI never gets in the way of a firefight:

1. **Look to Preview (`Preview Mode`):**
   Simply aim at a body within range (`2m` by default). After a split second, the Hover Loot window pops up showing the stalker's name, faction, rank, faction patch, and all of their gear.
   - **Full Combat Freedom:** While you are just looking, **your weapon still works normally**—you can shoot and aim down sights freely if you get ambushed.
   - **No Accidental Triggers:** Simply glancing at a body won't prematurely trigger cash pickups, stash notifications, or scavenging animations.
2. **Scroll to Loot (`Loot Mode`):**
   Roll your **Mouse Wheel (`Up` or `Down`)** once to activate the item selector!
   - As soon as you enter **Loot Mode**, you automatically pocket the stalker's loose cash, PDA notes, and stash coordinates, and the corpse is immediately marked **`[LOOTED]`** so you always know which bodies have already rolled for stashes and cash.
   - Your weapon fire and aiming are temporarily locked while the selector is active so you can click to grab items without firing your gun.
   - Look away from the body at any time to close the window and instantly restore normal weapon controls.
3. **Classic Inventory Anytime:**
   Prefer the traditional inventory screen for a deep gear comparison? Pressing your normal **Interact / Use key (`F`)** still opens the classic full-screen loot menu whenever you want.

---

## Controls & Keybindings

| Input / Action | What It Does |
| :--- | :--- |
| **Aim at a Body** | Opens the passive **Preview Mode** window (shooting & aiming remain active). |
| **Mouse Wheel (`Up` / `Down`)** *(First Scroll)* | Unlocks **Loot Mode** (pockets loose cash & PDA stashes and activates the item cursor). |
| **Mouse Wheel (`Up` / `Down`)** | Move the highlight cursor **Left / Right** across the current row. |
| **`Left Alt` + Mouse Wheel (`Up` / `Down`)** | Move the highlight cursor **Up / Down** along the current column. |
| **`Left Click (LMB)`** | **Loot Item / Stack** — Grabs the highlighted item (and any identical items stacked with it). |
| **Hold `Left Click (LMB)` + Mouse Wheel (`Up` / `Down`)** | **Vacuum Sweep** — Rapidly sweeps and loots items along a row as you scroll, with an automatic pause at the end of each row so you don't accidentally sweep into the next row. |
| **`Right Click (RMB)`** | **Take All** — Grabs everything left on the body at once. |
| **`Left Alt` + `Left Click (LMB)`** | **Field Strip Weapon** — Strips removable internal weapon parts (at or above your minimum condition threshold) and detaches scopes, silencers, and grenade launchers straight into your backpack, then shows a color-coded part condition summary on your PDA. |
| **`Left Alt` + `Right Click (RMB)`** | **Disassemble Item** — Disassembles the highlighted weapon, armor, or item right on the body and sends the spare parts straight to your inventory (automatically uses your disassembly tools if you carry them). |
| **`Number Keys (1–5)`** | **Quick Row / Category Jump (`1–5`)** — Instantly jumps the cursor to **Row `1–5`** *(default: Exact Row)* or to the matching **Inventory Category Tab (`1–5`)** *(Item Kind mode; press again to cycle through multiple rows of the same category)*. |
| **`Left Alt` + `Number Keys (1–5)`** | **Quick Row / Category Jump (`6–0`)** — Shifts keys `1–5` to **`6, 7, 8, 9, 0`** so you can jump to **Rows `6–10`** or **Inventory Category Tabs `6–0`** with one hand without leaving WASD. |

> **Tip:** `Left Alt` is the default **Universal Modifier Key** and can be rebound to any key you like in the Mod Configuration Menu (MCM).

---

## Handy Features & Visual Indicators

- **Full Inventory Icon Details:**
  Displays item durability/condition bars, weapon and armor internal part condition dots, repair-kit compatibility icons, armor faction patches, ammo types, item stack counters, and **SortingPlus** Favorite/Junk overlay icons and cell background highlights—matching the look and rules of your main inventory.
- **Smart Status Tags:**
  - **`[LOOTED]` Tag:** A bright green badge in the top-right corner of the header is applied immediately upon entering **Loot Mode** (in sync with stash and cash generation, and retro-compatible with bodies already searched in existing saves) so you can see at a glance which bodies you have already checked after a chaotic firefight.
  - **`<CLAIMED>` Banner:** If another living stalker nearby has claimed the kill, the window displays `<CLAIMED>` in yellow and locks out looting so you don't accidentally steal their loot and turn their squad hostile.
  - **`<EMPTY>` Banner:** Clearly marks bodies that have nothing left to take.
- **Full SortingPlus Parity, Auto-Sorting & Scrollable Grid:**
  Automatically mirrors your **SortingPlus** MCM configuration—including your custom category priority list, **Favorites** and **Junk** custom sorting order, and Favorite/Junk icon overlays and cell highlights—while adding a clean, auto-following scrollbar whenever a heavily packed body exceeds the window height.
- **Adaptive Footer Item Label:**
  Displays the highlighted item's full name centered in the footer bar and dynamically truncates extra-long names with trailing `...` scaled to your configured Hover UI window width (`Window Width (X Axis)`).

---

## Customization (MCM Settings)

Everything can be tailored to your screen setup under **MCM $\rightarrow$ Hover Corpse Loot**:

### 1. `UI Options` Tab
- **Toggle Hover Corpse Loot:** Master on/off switch for the mod.
- **Icon Overlay Toggles:** Individually toggle **Condition %**, **Weapon & Armor Part Condition Dots**, **Repair Type Icons**, and **Armor Faction Patches**.
- **Window Position (`OFFSET : X` & `OFFSET : Y`):** Adjust the horizontal (`0–500 px`, default `150 px`) and vertical (`0–250 px`, default `0 px`) distance from your crosshair.
- **Window Width (`X Axis`):** Resize the window width (`200–500 px`, default `300 px`) to fit more or fewer item columns per row.
- **Window Opacity:** Adjust the OLED-black background transparency (`10%–100%`, default `75%`).
- **Popup Delay:** Set how long you need to aim at a body before the preview appears (`100–500 ms`, default `200 ms`).
- **Max Looting Distance:** Adjust how far away you can inspect and loot bodies (`2.0–5.0 meters`, default `2.0 m`).

### 2. `UI Controls` Tab
- **Selection Cursor Color:** Choose between **Amber** *(default)*, **Cyan**, **White**, or **Green**.
- **Selection Color Brightness:** Fine-tune the glow and brightness of the highlight cursor (`1%–100%`, default `75%`).
- **Cursor Acceleration:** Adjust how fast the cursor speeds up when scrolling quickly (`1.0–5.0`, default `1.0` for 1:1 stepping).
- **Universal Modifier Key:** Rebind the modifier key used for column scrolling, row-jump shifting (`6–0`), field-stripping, and disassembling *(default: `Left Alt`)*.
- **Keyboard Number Key Shortcut Behavior:** Choose between **Exact Row** *(default — jumps directly to Row `1–10` in the Hover UI)* or **Item Kind** *(jumps to the row matching your inventory category tab, e.g., `2` = Weapons, `3` = Outfits, `4` = Ammo, `5` = Artifacts/Mutant Parts, and cycles across rows when pressed repeatedly)*.
- **Minimum Weapon Parts Condition to Strip:** Set the minimum durability threshold (`1%–100%`, default `60%`) required for internal weapon parts to be pulled during a field strip, leaving worn-out junk parts behind.

---

## Requirements & Compatibility

- **Requirements:** Built for **S.T.A.L.K.E.R. Anomaly 1.5.3** with **Modded Exes** and **Mod Configuration Menu (MCM)**.
- **Out-of-the-Box Compatibility:**
  - **S.T.A.L.K.E.R. G.A.M.M.A.** (respects G.A.M.M.A. firearm condition display rules and loot tables)
  - **Arti's Weapon Parts Overhaul (WPO)** (full internal part dot display and one-click field-stripping)
  - **FDDA / Animations** (works seamlessly alongside body search and disassembly animations)
  - **RavenAscendant's SortingPlus** (full MCM parity: respects your custom category priority list, Favorites & Junk sorting order, Favorite/Junk overlay icons, and persistent cell background highlights)
  - **Utjan's Item UI Improvements / QoL Bundle** (mirrors your part dots, repair badges, and icon overlays)
  - **Grok's NPC Loot Claim** (detects claimed bodies safely without triggering hostility)
  - **Haruka's Scavenger Skill & Guaranteed Loot mods**
  - **Custom UI Font Mods** (automatically adapts to your active modpack font profile)

<p align="right"><sub><em style="opacity: 0.65;">(Designed using Z and AAMT)</em></sub></p>
<p align="right"><sub><em style="opacity: 0.65;">[GTTIC]</em></sub></p>
