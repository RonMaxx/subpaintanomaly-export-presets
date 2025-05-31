# subpaintanomaly-export-presets
Contained here a pair of texture export presets for Substance 3D Painter intended to streamline the making of color, bump and bump# (partially) for Stalker Anomaly. Usage was intended with the use of ASM PBR - Metalic Roughness template, creating the glosiness, normal, and height maps for the creation of the maps.

For every Texture Set exported, the preset will export 3 (or 2) texture maps:
suffix BaseColor - Contains the Base color of the map
suffix bump - Contains the normal and glosiness map
suffix bump#(optional) - contains a blank error correction for normal map and the height map for parallax normal mapping

The bump# map doesnt have any kind of error correction expected from it, but should not add any artefacts to the bump map.
Also, be noted that the bump# map uses the baked height mesh map as the basis for the grey map. This was chosen for it being mostly unused (for what i know) in most projects. As such, warnings may occur in the Substance Painter log, but it should create the map as intended.

There are two preset exports:
PBR to BumpX (faux bumpsharp) - creates the bump# as above
PBR to BumpX (sans bumpsharp) - DOESN'T create the bump# map

Add the .spexp files in the Documents\Adobe\Adobe Substance 3D Painter\assets\export-presets folder, and it shall appear in the program.

Additionaly im adding a Universal Substance Painter DDS Export Plugin (https://www.nexusmods.com/site/mods/1044) ini setting file that automatically converts the exported textures to the correct DDS format used by the game (BC3 DXT5). 

Follow the plugin installation instructions, put the ini file in the python plugins folder, and set the texconv path as instructed in the plugin instructions and activate the Export DDS files options in the plugin menu.
