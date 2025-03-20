# GTA V Enhanced Modding Tutorial

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
3. Open the Developer build of Codewalker from the Codewalker github, in Visual Studio, then Build Codewalker, reach out to Codewalker support for help with this
4. Select all the build files, [mine built here: `.\CodeWalker\CodeWalker\bin\Debug\net48`]
5. Copy all the files to your Codewalker directory.
6. Open Codewalker, set location to your GTA5E Game Directory.

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


# Third Test: DLCPACKS
[Instructions coming soon(TM)]
