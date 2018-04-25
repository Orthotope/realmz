I got alot of the information from [fuzziqersoftware](https://github.com/fuzziqersoftware/realmz_dasm). I have expanded on this and organized the definitions.

Filename | Contains
 ------ | ------ 
<scenario name> | Scenario metadata. Recomended levels, starting pos
Data BD | Battle data. Position of monster og battle start and what kind of monsters.
Data CI | Contact info.
Data CS | This seems to be the same as <scenario name> ??
Data Custom 1 BD | Custom land tileset definitions.
Data DD | Land action point codes
Data DDD | Dungeon action point codes
Data DES | Monster descriptions
Data DL | Dungeon levels
Data ED | Simple encounters
Data ED2 | Complex encounters
Data ED3 | Extra action points
Data EDCD | Extra codes
Data LD | Level data (tile map)
Data MD | Monster data (including NPCs)
Data MD1 | Almost the same as MD, but some values are changed.
Data MD-1 | Same as MD1
Data MD2 | Map data (includes descriptions)
Data MENU | ???
Data NI | ??? (200 * 100 bytes)
Data OD | Yes/no encounter (option) answer strings
Data Race | Custom race config
Data Caste | Custom caste config
Data RD | Random rectangles
Data RDD | Dungeon random rectangles
Data SD | Shop data
Data SD2 | Strings
Data Solids | Solid special tiles.
Data TD | Treasure data
Data TD2 | Rogue encounters
Data TD3 | Time encounters
Global | Global macros
Scenario | ???
Scenario.rsf | Resources (images, sounds, etc.)

### All values in the files are big endian

# <scenario name>
 
bytes | value
---|---
int32 | Recomended starting level
int32 | ??
int32 | Start level
int32 | Start X
int32 | Start Y
Rest of file is unknown bytes

# Data BD
File contains 256 battles
#### Battle
346 bytes

bytes | value
---|---
0-337 | Position of monster in 13x13 grid.
byte | Distance from party
byte | ???
int16 | Before battle string id
int16 | After battle string id (Displayed when collecting treasure)
int16 | ???

One of the unknown is probably battle macro id.

# Data CI
18 x 256 bytes strings with information on the creater of the scenraio.

# Data Custom 1 BD
This has the same structure as the main tilset definitions in main data: Data <landname> BD
Zero tile is not used, so we have 200 tiles.
 
bytes | value
---|---
Tile[201] | Position of monster in 13x13 grid.
int16 | Base tile id
rest of file is unknown bytes

**Tile**

bytes | value
---|---
int16 | Sound id
int16 | Time per move
int16 | Solid type
int16 | Is shore
int16 | Is / need boat
int16 | Is path
int16 | Blocks line of sight
int16 | Need fly / float
int16 | Forrest type
int16 | ???
int16 [9] | Battle expansion
int16 | ???

one of the unknown is "Indoor Tile Set"

# Data SD
File contains 21 shops. Zero shop is not used. So we have 20 shops.
**Shop**
3002 bytes

bytes | value
---|---
int16 [2000] | Item id per group. 5 groups x 400 items.
int8 [2000] | Item inventory count. 
int16 | Inflation (% of normal item price)

