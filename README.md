# Survival Log Item Spawner

**Author:** BlackScriptor  
**Game:** Survival Log (SLGame)  
**Framework:** MelonLoader (v0.7.3)

A powerful, dynamic in-game item spawner and trainer for *Survival Log*. This mod bypasses the game's strict IL2CPP UI layout stripping by using a fully custom absolute-positioned IMGUI overlay and a raw hardware input parser. It reads the game's internal ConfigManager memory to dynamically dump and list items, bypassing the need for manual configuration files.

## Features
- **Dynamic Memory Reading:** Instantly reads and lists thousands of items directly from the game's _Config_Item_Dict memory.
- **Auto-Translation Engine:** Automatically cross-references and translates over 1,500 Chinese item names into English categories (Weapons, Ammo, Food, Wood, Medical, etc.) making searching effortless.
- **Safe Item Drops:** Modifies the physical DropItemManager to safely spawn items on the ground with maximum freshness (99M seconds) rather than corrupting the Redux inventory data models.
- **Custom Input Engine:** Completely bypasses the game's broken click-through interface by reading raw hardware states (Input.GetMouseButton), ensuring you don't accidentally shoot your weapon or open menus while spawning items.
- **Draggable UI:** Grab the top 30 pixels of the menu to drag it anywhere on your screen.

## Installation

### Step 1: Install MelonLoader
*Survival Log* runs on the IL2CPP Unity engine, so you need MelonLoader to inject mods.
1. Download the **MelonLoader Installer** from their [official GitHub page](https://github.com/LavaGang/MelonLoader/releases).
2. Run MelonLoader.Installer.exe.
3. Click the **SELECT** button and navigate to wherever you installed *Survival Log*. Select the main Survival Log.exe (or SLGame.exe) file.
4. **CRITICAL:** Uncheck the "Latest" box next to the version dropdown, and manually select **version 0.7.3**. Ensure the architecture is set to **x64**. 
5. Click **INSTALL**. 
6. Launch *Survival Log* normally once. You should see a black console window pop up while the game loads. This generates the necessary Mods folder. Once you reach the main menu, close the game.

### Step 2: Install the Mod
1. Download SurvivalTrainer.dll from the [Releases](Releases/) folder of this repository.
2. Navigate to your *Survival Log* game installation folder.
3. You should now see a folder named Mods (created by MelonLoader in Step 1). 
4. Drop SurvivalTrainer.dll directly into the Mods folder.
5. Launch the game!

## How to Use
- Press **Insert** or **F8** in-game to toggle the Spawner Menu.
- Click **Load Items from Game Memory** to populate the list.
- Use the **Search** box to find items by their English names (e.g., "Rifle", "Ammo", "Meat").
- Select your drop amount using the +/- buttons.
- Click **Drop**. The items will instantly drop at your feet!

## Disclaimer & Warning
**⚠️ USE AT YOUR OWN RISK!**  
To be completely honest, the code holding this together is currently in a **"duct tape and spit"** kind of stage. Because the game developers aggressively stripped the UI engine, this mod interacts heavily with raw memory and bypasses several internal game loops using aggressive workarounds.

Expect glitches, expect bugs, and use carefully:
- It may cause physics glitches if you spawn hundreds of items at once.
- Game updates that change internal memory structures may break the mod.
- **I (BlackScriptor) will not be responsible for any corrupted save files, game crashes, or issues you may encounter because of this.** Always back up your save files before experimenting!
