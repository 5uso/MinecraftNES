# MinecraftNES

NES Emulation in Minecraft, by Suso (https://www.youtube.com/SusoYT | https://twitter.com/5usos)
Made to be used with Minecraft 1.16.X, may work with future versions.

- Transform your NES ROM into the proper format using ROM.py: python ROM.py [input name (without .nes)] [output name] (Works only with mapper 0 and mapper 2 games)
- Place your ROM inside assets/minecraft/textures/effect/rom.png in either of the resourcepacks (depending on your game's mapper).
- Set your resolution to 640×480 from the launcher profiles and play in windowed mode. (Setting the resolution from the graphics menu and then using fullscreen is an alternative, but things may look blurry)
- Enter the world with the resourcepack on and your graphics set to Fabulous. (It may take a while to load, allow up to 5 minutes)

Controls:
    DPAD - Minecraft movement
    A - Move scroll wheel
    B - Move camera (moving it too fast could input other buttons if your frame rate is too low)
    START - Use Item/Place Block
    SELECT - Attack/Destroy

    I'd recommend using software to remap a controller to these actions (I use JoyToKey https://joytokey.net/en/download).

This was tested on vanilla Minecraft, using mods such as Optifine may prevent it from working.

TAS.py transforms .fm2 TAS files into images, which can be played by placing them in assets/minecraft/textures/effect/tas.png
Note that TASes don't work very well, since they desync on lag frames.

Uncommenting line 5 of assets/minecraft/shaders/program/ppu.fsh enables debug output (RAM and registers will be rendered to the screen).
Uncommenting line 5 of assets/minecraft/shaders/program/rst.fsh switches input to TAS.
Uncommenting line 6 of assets/minecraft/shaders/program/vertex.fsh sends the output to a in-world screen (unused feature). These screens can be made by placing glowstone and shroomlights.
Changing the values on lines 7-8 of assets/minecraft/shaders/program/vertex.fsh changes scaling on fullscreen mode. Useful to show all the debug information, which may go offscreen otherwise.
