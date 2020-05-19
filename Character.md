# Not complete

Spell points is calculated from knowledge and level.

hex offset | bytes | value
---|---|---
0|INT8[4] | ??? 
4|INT16 | Chance to hit
6|INT16 | Dodge missile
8|INT16 | Missile adjust
a|INT16 | two-hand adjust
e|INT16 | Attacks per round ? (divide by 2)
16|INT16 | Number of items (max 30)
28|INT16 | Magic resistance
2c|INT16 | Armor rating
2e|INT16 | Damage
30|INT16 | Race
32|INT16 | Caste
36|INT16 | Gender
38|INT16 | Skill level
3c|INT16 | Movement
4e |INT16 | Current stamina (hit points)
50 |INT16 | Max stamina (hit points)
52|INT16 | Portrait ID
54|INT16 | Battle image ID
56|INT16 | Current spell Points
58|INT16 | Max spell Points
5a|INT16 | ???
5c|INT16 | ???
5e|INT16 | ???
60 |INT16 | Bare hand damage
62|INT16 | retreating
64|INT16 | helpless
66|INT16 | tangled
68|INT16 | cursed
6a|INT16 | magic aura
6c|INT16 | stupid
6e|INT16 | slow
70|INT16 | shielded from hits
72|INT16 | missile shield
74|INT16 | poison
76|INT16 | regenerating
78|INT16 | pro' heat
7a|INT16 | pro' cold
7c|INT16 | pro' electric
7e|INT16 | pro' chemical
80|INT16 | pro' mental
82|INT16 | pro' 1st
84|INT16 | pro' 2nd
86|INT16 | pro' 3rd
88|INT16 | pro' 4th
8a|INT16 | pro' 5th
8c|INT16 | strong
8e|INT16 | pro' foe
90|INT16 | speed
92|INT16 | invisible
94|INT16 | animated
96|INT16 | stoned
98|INT16 | blind
9a|INT16 | diseased
9c|INT16 | confused
9e|INT16 | reflect spells
a0|INT16 | reflect attacks
a2|INT16 | attack bonus
a4|INT16 | absorb energy
a6|INT16 | energy drain
a8|INT16 | absorb spells
aa|INT16 | hindered attack
ac|INT16 | hindered defense
ae|INT16 | defense bonus
b0|INT16 | silence
b2|INT16 | + vs magic using
b4|INT16 | + vs undead
b6|INT16 | + vs demon
b8|INT16 | + vs reptilian
ba|INT16 | + vs evil
bc|INT16 | + vs intelligent
be|INT16 | + vs giant
c0|INT16 | + vs non-humanoid
f2|INT16 | sneak
f4|INT16 | hide in shadows
f6|INT16 | resurrect
f8|INT16 | major wound
fa|INT16 | detect secret
fc|INT16 | acrobatic act
fe|INT16 | detect trap
100|INT16 | disable trap
102|INT16 | hear noise
104|INT16 | force lock
106|INT16 | move silently
108|INT16 | pick lock
10a|INT16 | pick pocket
10c|INT16 | turn undeod
110|INT16 | DR vs Charm
112|INT16 | Heat
114|INT16 | Cold
116|INT16 | Electric
118|INT16 | Chemical
11a|INT16 | Mental
11c|INT16 | Magic
11e|INT16 | Special
124 |30*6|items[]
-|INT16 | Item ID
-|INT8 | Equiped
-|INT8 | Identified
-|INT16 | Number of uses | Infinite = FFFF
1ec|INT32 | Age in days
1f0|INT32 | Victory points
1f4|INT16 | Load
1f6|INT16 | Max load
1f8|INT16 | Gold
1fa|INT16 | Gems
1fc|INT16 | Jewelry
205 |INT8 | Brawn
206|INT8 | Knowledge
207|INT8 | Judgment
208|INT8 | Agility
209|INT8 | Vitality
20a|INT8 | Luck
20b|INT8[84] | 12*7 Spells
25f |30|Character name
280 |INT32 | Damage taken
284|INT32 | Damage given
288|INT32 | hits given
28c|INT32 | Hits taken
290|INT32 | Missed attacks
294|INT32 | Dodged attacks
298|INT32 | enemies killed
29c|INT32 | times killed
2a0|INT32 | times unconscious
2a4|INT32 | spells cast
2a8|INT32 | undead destroyed
2ac|INT32 | undead turned
2b0|INT32 | penalty points
