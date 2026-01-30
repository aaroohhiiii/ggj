UNIVERSAL BASE CHARACTERS — SETUP IN THIS PROJECT
=================================================
Quaternius Universal Base Characters [Standard]. Added properly for Mask Swap.

----------------------------------------
FOLDER STRUCTURE
----------------------------------------

  player/
    • Superhero_Male_FullBody.gltf + .bin + textures  — use for Player (and optionally Guard/Scientist/Janitor by changing material).
    • Superhero_Female_FullBody.gltf + .bin + textures — use for alternate Player or NPCs.
    • In Godot: instance from FileSystem → assets/3d/characters/player/Superhero_Male_FullBody.gltf (or Female) into your level or as child of Player node.

  npcs/
    • Guard, Scientist, Janitor: use the SAME character from player/.
    • In Godot: instance assets/3d/characters/player/Superhero_Male_FullBody.gltf (or Female) into the level for each NPC. Change material (Albedo Color) per role: Guard = dark blue, Scientist = light, Janitor = grey. No separate NPC model files needed.

  hairstyles/
    • Optional hair/eyebrows to add on top of the base character (rigged to head bone).
    • Files: Hair_Buzzed.gltf, Hair_Beard.gltf, Hair_SimpleParted.gltf, Hair_Long.gltf, Hair_Buns.gltf, Hair_BuzzedFemale.gltf, Eyebrows_Regular.gltf, Eyebrows_Female.gltf.
    • In Godot: import a hairstyle, then add it as a child of the character's Head bone (or Armature) so it follows the head. Use for variety (e.g. Guard = Beard, Scientist = SimpleParted).

  masks/
    • Put mask HUD icons here (mask_guard.png, mask_scientist.png, mask_janitor.png) or in assets/ui/. See MASK_ASSETS_EXACT_STEPS.txt in project root.

  License_Standard.txt
    • CC0 1.0 — use in any project, no attribution required. See file for full text.

----------------------------------------
HOW TO USE IN GODOT
----------------------------------------

  Player:
    1. Open your level (e.g. test_level.tscn).
    2. Ensure Player node (CharacterBody3D) exists.
    3. Drag assets/3d/characters/player/Superhero_Male_FullBody.gltf into the scene as a child of Player.
    4. Position/scale if needed. The character mesh will move with the Player.

  NPCs (Guard, Scientist, Janitor):
    1. Drag Superhero_Male_FullBody.gltf (or Female) into the level as a sibling of Player (e.g. under TestLevel).
    2. Select the NPC's body mesh (SuperHero_Male under Armature) → Surface Material Override → New StandardMaterial3D → set Albedo Texture to T_Superhero_Male_Dark.png and Albedo Color: Guard = dark blue, Scientist = light, Janitor = grey.

  Hairstyles (optional):
    1. Open the character scene (or instance in level).
    2. Drag a hairstyle from assets/3d/characters/hairstyles/ (e.g. Hair_Beard.gltf) into the scene as a child of the character's Armature or Head bone.
    3. Adjust position/rotation so it fits the head.

----------------------------------------
SOURCE
----------------------------------------

  Pack: Universal Base Characters [Standard] by Quaternius
  https://quaternius.itch.io/universal-base-characters
  License: CC0 1.0 (see License_Standard.txt)

----------------------------------------
END
----------------------------------------
