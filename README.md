# GTA V Enhanced Modding Tutorial - [New OpenRPF Method]

# Legend / Key:
- Game Directory = Grand Theft Auto V Enhanced
- Mods folder = "./Grand Theft Auto V Enhanced/mods"

# Setup:
1. Clean and legitimate copy of Grand Theft Auto V Enhanced
2. Create a new folder called `mods` in the Game Directory
3. Copy the file `rpf.cache.disable` included in this repo to the Game Directory.
4. [Install OpenRPF](https://www.gta5-mods.com/tools/openrpf-openiv-asi-for-gta-v-enhanced)
5. [Install ScriptHookV](https://dev-c.com/gtav/scripthookv/)


# First Test:
[ I personally use OpenIV to make copies of update.rpf + update.rpf2 to make this step easier ]
1. Create your `mods` folder in the Game Directory, if you haven't done so already.
2. Create new folder in `mods` called `update`.
3. Copy the original `update.rpf` and `update2.rpf` files from the `update` folder to the `mods/update/` folder.
4. Launch the Game.
5. If the game crashes, we've missed a step, try again from the top.
6. The game should launch, nothing will be different as we haven't altered any of the files.
7. Find a vehicle in-game, I usually go with a Grotti Carbonizzare or Pegassi Infernus, get into it and save the game from the player's mobile phone
8. Close the Game.


# Second Test: Editing Files
[ Once you've achieved this, modding will be easier to understand and you can start doing it on your own ]
1. Go to: `./mods/update/update.rpf/common/data/handling.meta`.
2. You can choose to replace the whole file from a handling mod such as [HandlingV](https://github.com/shifuguru/HandlingV), or edit it for yourself.
3. Using **File Explorer**, go to: `./mods/update/update.rpf`.
5. Open the Game.


# Third Test: Migrating dlcpacks
[ Codewalker - Legacy Setup ]
1. Create a copy of Codewalker
2. Feel free to rename the Codewalker folders to - LEGACY, and - ENHANCED for easier management.
3. Open the Codewalker - Legacy app.
4. Set File > Game Configuration... to GTA 5 Legacy directory.
4. Migrate/Copy your chosen dlcpack from Legacy to Enhanced, recommend copying the dlcpack.

# Fixing Textures and vehicles crashing:
[ Edit: These instructions are now outdated, you can use the Asset Converter tool in Codewalker to convert vehicle files now ] <br>
[ Thanks to @CP for this step ]
1. Open texture dictionary (.ytd) and find script_rt_* texture
2. Go to Details tab:
3. [G9_Flags: 2490920]
4. [format: D3DFMT_A8R8G8B8 ]
5. [G9_Format: B8G8R8A8_UNORM]


# Updating .yft, .ycd, .ytd etc. files from Legacy to Enhanced
1. Tip: create folders for exported filetypes to manage the files easier.
2. Export the files as .xml from Codewalker (Legacy).
3. Import .xml files back to the dlcpack vehicles.rpf using Codewalker (Enhanced).
- Tip: Once you have imported desired files ensure they open correctly.
4. Add dlcpack to dlclist.xml in update.rpf the standard way: - e.g. <Item>dlcpacks:/dlcpack_name/</Item>
5. Repeat the signing process for update.rpf
6. Launch Game

You can also try using the Asset Converter in Codewalker.
