# Survival Log Item Spawner

**Author:** BlackScriptor  
**Game:** Survival Log (SLGame)  
**Framework:** MelonLoader (net6)

A powerful, dynamic in-game item spawner and trainer for *Survival Log*. This mod bypasses the game's strict IL2CPP UI layout stripping by using a fully custom absolute-positioned IMGUI overlay and a raw hardware input parser. It reads the game's internal ConfigManager memory to dynamically dump and list items, bypassing the need for manual configuration files.

## Features
- **Dynamic Memory Reading:** Instantly reads and lists thousands of items directly from the game's _Config_Item_Dict memory.
- **Auto-Translation Engine:** Automatically cross-references and translates over 1,500 Chinese item names into English categories (Weapons, Ammo, Food, Wood, Medical, etc.) making searching effortless.
- **Safe Item Drops:** Modifies the physical DropItemManager to safely spawn items on the ground with maximum freshness (99M seconds) rather than corrupting the Redux inventory data models.
- **Custom Input Engine:** Completely bypasses the game's broken click-through interface by reading raw hardware states (Input.GetMouseButton), ensuring you don't accidentally shoot your weapon or open menus while spawning items.
- **Draggable UI:** Grab the top 30 pixels of the menu to drag it anywhere on your screen.

## Installation
1. Download and install [MelonLoader](https://github.com/LavaGang/MelonLoader) (Make sure you use the **.NET 6 (net6)** version).
2. Run *Survival Log* once to let MelonLoader generate its folders, then close the game.
3. Download SurvivalTrainer.dll from the [Releases](Releases/) folder of this repository.
4. Place SurvivalTrainer.dll inside the Mods folder located in your *Survival Log* game directory.
5. Launch the game!

## How to Use
- Press **Insert** or **F5** in-game to toggle the Spawner Menu.
- Click **Load Items from Game Memory** to populate the list.
- Use the **Search** box to find items by their English names (e.g., "Rifle", "Ammo", "Meat").
- Select your drop amount using the +/- buttons.
- Click **Drop**. The items will instantly drop at your feet!
- If the UI ever glitches, press **F1** as a hardcoded fallback to drop a piece of Glass.

## Disclaimer & Warning
**⚠️ Use at your own risk!**
This mod interacts heavily with raw memory and bypasses several internal game loops using reflection. It is not perfect. 
- It may cause physics glitches if you spawn hundreds of items at once.
- Game updates that change internal memory structures may break the mod.
- **I (BlackScriptor) am not responsible for any corrupted save files, game crashes, or issues you may encounter while using this.** Always back up your save files before using trainers!
