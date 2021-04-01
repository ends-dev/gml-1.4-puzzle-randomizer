# puzzle-game-randomizer

DISCLAIMER:
WRITTEN FOR COMPATIBILITY WITH GAME MAKER STUDIO 1.4
USES FUNCTIONS OBSOLETE IN GAME MAKER STUDIO 2 AND HIGHER
CAN BE RUN IN GAME MAKER STUDIO 2 WITH COMPATIBILITY SCRIPTS


INCLUDES:
**scr_starterset, scr_drawset, README.md**

USES:
Randomizes a tile set for each player at the beginning of a match, and draws them to the screen
Designed that each player starts with the same puzzle layout, like in Panel de Pon and similar variants
Can easily be adjusted to support a variety of other puzzle game styles

INSTRUCTIONS:
1. Create scripts named **scr_starterset** and **scr_drawset** (or rename them)
2. Copy and paste the corresponding code into each script
3. Create a new object, and execute script **scr_starterset** in the Create Event
    
    (note: In my original project, this code was in an invisible controller object that handle a few other scripts and launched at the very start of a match. In its Create Event, I used a simple **scr_starterset();** before spawning the player controllers.)
    
5. Set the result to a variable called **tileset**
6. Execute script **scr_drawset**.
  
    (note: It will default to the bottom-left. In my original project, the controller object spawned different player object instances, which all copied **global.starterset** data structure to local variable **tileset** so they could make independent changes to their own tile structure. At the end of the Create Event in the player object, I ran **scr_drawset();**)
