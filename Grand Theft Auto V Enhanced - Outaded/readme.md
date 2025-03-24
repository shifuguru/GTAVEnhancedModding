# GTA V Enhanced Modding Tutorial - [OUTDATED]

Keeping this tutorial online for future reference.

# Legend / Key:
- GTA5E = Grand Theft Auto V Enhanced
- Mods folder = "./Grand Theft Auto V Enhanced/mods"
- Ultimate ASI Loader location = "./Grand Theft Auto V Enhanced/dsound.dll"
- 'Outer' = Parent .rpf file.
- 'Inner' = Child .rpf file.

# Setup:
1. Clean and legitimate copy of Grand Theft Auto V Enhanced
2. Create a new text file in the GTA5E directory called `commandline.txt`, with contents:<br>
`-skipPatcherCheck`
3. Create a new folder called `mods` in the GTA5E directory
4. Copy the `rpf.cache` file included in this repo to the `mods` folder
5. Copy `dsound.dll` from Ultimate ASI Loader to the GTA5E directory
6. Create a new text file called `Global.ini` file in GTA5E directory with contents:<br>
  `[FileLoader]`<br>
  `OverloadFromFolder=mods`


# CodeWalker Installation:
1. Visual Studio 2022 installed.
2. Latest public Codewalker installed.
3. Codewalker installation:<br>
A) Download from the Codewalker Discord Channel:<br>
https://discord.com/channels/329138547833700352/351357358460370944<br><br>
B) Build with Visual Studio:
    - Open the Developer build of Codewalker from the Codewalker github, in Visual Studio, then Build Codewalker, reach out to Codewalker support for help with this
    - Select all the build files, [mine built here: `.\CodeWalker\CodeWalker\bin\Debug\net48`]
    - Copy all the files to your Codewalker directory.
4. Open Codewalker and set location to your GTA5E Game Directory.


# ArciveFix:
1. Download ArchiveFix for GTA V: https://github.com/dedanab/ArchiveFix-for-GTA
2. Create a shortcut and move the shortcut to Desktop or preferred directory in order to access the shortcut faster
3. We will be dragging .rpf files to this shortcut often!

# Important Info:
To load mods, as of March 2025, you need to sign each edited .rpf file before copying to the game.
# This means that for each .rpf you edit, you must sign that .rpf before the game will launch successfully.


# First Test:
[I personally use OpenIV to make copies of update.rpf + update.rpf2 to make this step easier]
1. Create your mods folder in the GTA5E directory, if you haven't done so already.
2. Create a new folder called `update`.
3. Copy the `update.rpf` and `update2.rpf` files to the `mods/update/` folder.
4. Drag the `update.rpf` file into the ArchiveFix shortcut.
5. Drag the `update2.rpf` file into the ArchiveFix shortcut.
6. Launch the Game.
7. If the game crashes, we've missed a step, try again from the top and reach out if it's not working.
8. The game should launch, nothing will be different as we haven't altered any of the files.
9. Find a vehicle in-game, I usually go with a Grotti Carbonizzare or Pegassi Infernus, and get into it.
11. Save and Close the Game.


# Second Test: Editing Files
[Once you've achieved this, modding will be easier to understand and you can start doing it on your own]
1. Using **Codewalker**, go to: `./mods/update/update.rpf/common/data/handling.meta`.
2. You can choose to replace the whole file from a handling mod such as **https://github.com/shifuguru/HandlingV**, or edit it for yourself.
3. Using **File Explorer**, go to: `./mods/update/update.rpf`.
4. Drag the **update.rpf** file to the **ArchiveFix** shortcut.
5. Open the Game.


# Third Test: Migrating dlcpacks
[Codewalker - Legacy Setup]
1. Create a copy of Codewalker
2. Feel free to rename the Codewalker folders to - LEGACY, and - ENHANCED for easier management.
3. Open the Codewalker - Legacy app.
4. Set File > Game Configuration... to GTA 5 Legacy directory.
4. Migrate/Copy your chosen dlcpack from Legacy to Enhanced, recommend copying the dlcpack.


# Updating .yft, .ycd, .ytd etc. files from Legacy to Enhanced
1. Tip: create folders for exported filetypes to manage the .xml files easier.
2. Export the files as .xml from Codewalker - Legacy to recommended folders.
3. Import .xml files back to the dlcpack vehicles.rpf using Codewalker - Enhanced
- Tip: Once you have imported desired files ensure they open correctly
4. Export vehicles.rpf from dlcpack
5. Drag n Drop vehicles.rpf on ArchiveFix.exe
6. Import vehicles.rpf back to the dlcpack using Codewalker - Enhanced
7. In Codewalker check the .rpf is signed "NG", not "Open" or "None/No"
8. Repeat the process for the parent dlc.rpf
9. Add dlcpack to dlclist.xml in update.rpf the standard way:
- e.g. <Item>dlcpacks:/dlcpack_name/</Item>
10. Repeat the signing process for update.rpf
11. Launch Game

# Fixing Textures and vehicles crashing:
[ Thanks to @CP for this step ]
1. Open texture dictionary (.ytd) and find script_rt_* texture
2. Go to Details tab:
3. [G9_Flags: 2490920]
4. [format: D3DFMT_A8R8G8B8 ]
5. [G9_Format: B8G8R8A8_UNORM]
