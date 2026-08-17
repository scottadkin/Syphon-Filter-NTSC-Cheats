# Syphon Filter NTSC Cheats

## Main Cheat File **SCUS-94240.cht**
- Instant AI Max Danger.
- One Hit KO All Levels.
- One Hit KO individual missions.
- Rapid Fire.
- Allow explosives on the mission Main Subway Line
- Multiple Give AI M79's mission tests.

## One Hit KO
- Forces player's max health to 1, removes all armour including pickups.
- All levels cheat, or per level cheats.

**/One Hit KO/SCUS-94240.cht**


## v2.0 Instant Max Danger
- In this version of AI max danger the AI will cause damage to you regardless if you are moving or not, if they can see you they will damage you.

**Notes**
Last Seen Timestamps Offsets(4bytes):
+11CFCC
+11D0A4
+11D17C
+11D254
+11D32C 

**+0x07** from each address is a byte, if it's value is 0 it can see it's target.
**+0x30** from each address is the danger value that the hud uses, 2 bytes, range 1-4096, higher the value more the danger bar fills up.
**-0x4C** from each address is a byte counter, if the value is over a certain value(>121) the NPC can cause damage to it's target.

Cheat pseudocode:
```
If NPC#1 can see target
    then set last seen target timestamp to max int
    set danger value to 4096
    and set byte counter over damage threshold
Repeat 5 times for different addresses.
``

```
[v2.0 Instant Max Danger]
Type = Gameshark
Activation = EndFrame
Description = Improved version of Instant Max Danger
C311cfd3 01
9011cfcc FFFFFFFF
8011cffc 1000
3011cf80 FF
00000000 FFFF
C311d0ab 01
9011d0a4 FFFFFFFF
8011d0d4 1000
3011d058 FF
00000000 FFFF
C311d183 01
9011d17c FFFFFFFF
8011d1ac 1000
3011d130 FF
00000000 FFFF
C311d25b 01
9011d254 FFFFFFFF
8011d284 1000
3011d208 FF
00000000 FFFF
C311d333 01
9011d32c FFFFFFFF
8011d35c 1000
3011d2e0 FF
00000000 FFFF
```

# Notes

AI Max danger are 216 bytes apart(0xd8)
```



[v1.0 Instant AI Max Danger]
Type = Gameshark
Activation = EndFrame
Description = Enemies will be able to damage you instantly instead of waiting for danger bar to fill up.
9011CFCC FFFFFFFF
9011D0A4 FFFFFFFF
9011D17C FFFFFFFF
9011D254 FFFFFFFF
9011D32C FFFFFFFF

[Rapid Fire]
Type = Gameshark
Activation = EndFrame
Description = Player will be able to fire their weapon's every frame.
30127DA0 0000


(-2 bytes from each of these addresses, of type byte set to 255 as well)
[test ai rapid fire]
Type = Gameshark
Activation = EndFrame
9018B000 FFFFFFFF
9018B200 FFFFFFFF
9018B400 FFFFFFFF
9018B600 FFFFFFFF
9018B800 FFFFFFFF
9018BA00 FFFFFFFF
9018BC00 FFFFFFFF
9018EF48 FFFFFFFF
9018F148 FFFFFFFF
```

# Weapon Ids
```
01 - Silenced 9MM
02 - 9MM
03 - 
04 - 45
05 - G18
06 - Combat Shotgun
07 - Shotgun
08 - PK102
09 - M16
0A - BIZ-2
0B - HK5
0C - Nightvision Sniper Rifle
0D - Sniper Rifle
0E - Air Taser
0F -
10 - M79
11 - K3G4
12 - Viral Scanner
13 - Grenades
14 - Gas Grenades
15 - Flashlight
16 -
17 -
18 - C4
19 - Antigen
```

# First Load & Retry AI Weapon ID Notes
- Georgia Street, addresses same distance apart but on retry they are 396 bytes before the first try address.
- First Try +1AA204, retry +1AA078
- Destroyed Subway, addresses same distance apart but on retry they are 1468 before first try address.
- First Try +1A351C, retry +1A2F60
- Main Subway Line, addresses same distance apart but on retry they are 1652 bytes before the first try address.
- First Try +1C7370, retry +1C6CFC
- Washington Park, addresses same distance apart but on retry they are 1588 bytes before the first try address.
- First Try +1AA5A4, retry +1A9F70
- Expo Center Reception, addresses same distance apart but on retry they are 720 bytes before the first try address.
- First Try +1AE724, retry +1AE454 (based on last addresses)
- Expo Center Dinorama, addresses same distance apart but on retry they are 1304 bytes before the first try address.
- First Try +1AA5A8, retry +1AA090
- Rhoemers base, addresses same distance apart but on retry they are 1288 bytes before the first try address.
- First Try +1A9D70, retry +1A9868
- Pharcom Warehouses, addresses same distance apart but on retry they are 1696 bytes before the first try address.
- First Try +1AC6F8, retry +1AC058
- Missile Silo, addresses same distance apart but on retry they are 272 bytes before the first try address.
- First Try +1AD994, retry +1AD884

# Mission Index Byte
- +0116474

# Health & Armour Offsets(Ignore first 2 bytes, Armour First, Health Second, Both 2 Bytes Each)
- Georgia Street: First Load +1A8BDA, retry +1A8A4C
- Destroyed Subway: First Load +1A349C, retry +1A2EE0
- Main Subway Line: First Load +1C733C, retry +1C6CC8
- Washington Park: First Load +1AA440, retry +1A9E0C
- Freedom Memorial: First Load +1C0B0C, retry +1C0494
- Expo Center Reception: First Load +1AC26C , retry +1ABF9C 
- Expo Center Dinorama: First Load +1A9FD0, retry +1A9AB8
- Rhoemer's Base: First Load +1A9798, retry +1A9290
- Base Bunker: First Load +1B3A8C, retry +1B381C
- Base Tower: First Load +1C5A58, retry +1C5520
- Base Escape: First Load +1AE44C, retry +1ADF98
- Rhoemer's Stronghold: First Load +1AD590, retry +1AD320
- Stronghold Lower Level: First Load +1AB800, retry +1AB064
- Stronghold Catacombs: First Load +1ACE94, retry +1ACC7C
- Pharcom Warehouses: First Load +1AACF0, retry +1AA650
- Pharcom Elite Guards: First Load +1A4564, retry +1A4100
- Warehouse 76: First Load +1B7398, retry +1B725C
- Silo Access Tunnels: First Load +1A2304, retry +1A2090
- Tunnel Blackout: First Load +1B0C58, retry +1B0A60
- Missile Silo: First Load +1AD5D0, retry +1AD4C0

# Test byte to check if mission is first load or reload(Tunnel Blackout both same value...)
Memory offset +01164A8
- Georgia Street, First Load = 32(0x20), reload = 88(0x58)
- Destroyed Subway, First Load = 48, reload = 88
- Main Subway Line, First Load = 112, reload = 56
- Washington Park, First Load = 240, reload = 216
- Freedom Memorial, First Load = 112, reload = 56
- Expo Center Reception, First Load = 72, reload = 224
- Expo Center Dinorama, First Load = 240, reload = 104 
- Rhoemer's Base, First Load = 240, reload = 104
- Base Bunker, First Load = 208, reload = 152
- Base Tower, First Load = 48, reload = 152
- Base Escape, First Load = 8, reload = 176
- Rhoemer's Stronghold, First Load = 104, reload = 48
- Stronghold Lower Level, First Load = 216, reload = 16
- Stronghold Catacombs, First Load = 136, reload = 128
- Pharcom Warehouses, First Load = 24, reload = 200
- Pharcom Elite Guards, First Load = 232, reload = 176
- Warehouse 76, First Load = 88, reload = 184
- Silo Access Tunnels, First Load = 208, reload = 152
- Tunnel Blackout, First Load = 40, reload = 40.....................
- Missile Silo, First Load = 112, reload = 232



## Player Position
- Georgia Street First Load: +197614(4bytes), +4, +4.
- Georgia Street Retry: +197488(4bytes), +4, +4.
- Destroyed Subway First Load: +196A28, +4, +4.
- Destroyed Subway Retry: +19646C, +4, +4.


# NPC health data? in subway.fog

76 bytes apart?
after BARLIT.TMD text (3 different sets of same data?)
100health
64 00 FF FF 00 00 00 00 00 00 CA CA
150health
96 00 FF FF 00 00 00 00 00 00 CA CA
-1C from first byte is weapon id

WeaponId to health bytes from subway.fog
9mm npc
02 83 00 00 01 00 00 00 40 0B 00 00 FF FF FF FF 
00 00 00 00 01 00 01 00 FF FF 64 00 64 00 FF FF 
00 00 00 00 00 00 CA CA


? grenade /9mm bank roof guy?
weaponID -4 bytes
13 1A 00 00 02 C1 00 00 03 00 00 00 78 12 00 00 
FF FF FF FF 00 00 00 00 01 00 01 00 FF FF 64 00 
64 00 FF FF 00 00 00 00 00 00 CA CA 



flak jacket -2 bytes from health

# AI Health/Weapon Offsets
Example Rhomers base: (76 bytes apart?)
- Health 2 bytes
- -1C from health is weapon id. 1 byte

# AI Ammo offsets
Example rhomers base:
- Ammo 1 byte
- -14(hex) last shot fired

# AI structure?

NPC Positions:
- Offsets seem to be same on first load and retry
NPC Positions 1a8 bytes apart? (-0x40 another set off addresses for same ai)(position offsets same on level 1 and level 3?)
//Krav spawn coordinates 29 FA FF FF C1 08 00 00 17 1A 00 00
Level 1/3 offsets:
+11D478 (npc)
npc +1A8 (npc2)
npc2 +1A8 (npc3)
npc3 +1A8 (npc4)
npc4 +1A8 (npc5)



Example:
- Last Fire Timestamp/TickID: 018B000
- AMMO +14(HEX) offset from fire timestamp
- Bullets To Fire In Current Burst + 1D
- Pause between fire bursts(+1b from ammo offset)
- ? set to 0 to make ai rapid fire m16(-7 from pause between bursts)

last shot fired -227B8 from ai health??
another was 22BB8??
another was 22B6C??



## Crates
- Objects 0x24 bytes apart?

- 0(9th byte) = Not Taken, 32(0x20) = Taken. If set back to 0 you can retake the item if you return to it.
- Following 2 bytes offset to data? always 256 bytes apart //wrong
- the 2nd byte is item index/order? DC, DD, DA
m79 crate not taken 00 00 00 00 06 00 0B 00 00 10 49 01 D9 00 00 00
m79 crate taken bytes: 00 00 00 00 06 00 0B 00 20 10 49 01 D9 00 00 00

Geogria Street Bank
m16 crate not taken 00 00 00 00 06 00 0B 00 00 09 51 01 DC 00 00 00
m16 crate taken 00 00 00 00 06 00 0B 00 20 09 51 01 DC 00 00 00

Geogria Street Bank
grenades crate not taken 00 00 00 00 06 00 0B 00 00 13 53 01 DA 00 00 00
grenades crate taken 00 00 00 00 06 00 0B 00 20 13 53 01 DA 00 00 00

Georgia Street Bank
Flak Jacket not taken 00 00 00 00 06 00 0B 00 00 80 52 01 DD 00 00 00
Flak Jacket taken 00 00 00 00 06 00 0B 00 20 80 52 01 DD 00 00 00

Georgia Street Bar
Shotgun not taken 00 00 00 00 06 96 07 00 00 07 48 01 DB 00 00 00
Shotgun taken 00 00 00 00 06 96 07 00 20 07 48 01 DB 00 00 00

## Random tests
```
;* F4XXXXXY 00WWSIZE - 8-Bit Find and Replace, Find and Replace for 16 bytes.
;  aabbccdd eeffgghh   WW = Wildcard Byte, SIZE = Size of Area to Search/4 so FFFF=256K,
;  iijjkkll mmnnoopp   XXXXXY = Address @ centre of Search Area (Y must be even 0/2/4/6/8/A/C/E)
;  AABBCCDD EEFFGGHH   Find aa,bb,cc,dd,ee,ff,gg,hh,ii,jj,kk,ll,mm,nn,oo,pp and
;  IIJJKKLL MMNNOOPP   replace with AA,BB,CC,DD,EE,FF,GG,HH,II,JJ,KK,LL,MM,NN,OO,PP.
;                      Any byte matching the WW character in the find bytes will
;                      be ignored. Any byte matching the WW character in the
;                      replace bytes will be ignored, ideally all bytes in the
;                      replace line should be WW with the exception of where
;                      an actual replacement is required.

FF Wildcard, 32kb search region starting at address +1AD978
This is buggy as it only checks for one byte and that can be anything and not the AI weapons, this also gives the glasses/bottles in the bar a glitchy look.

The ai weapon stuff normally has several 00 bytes in the 16 byte regions, we could replace several wildcards with 00 instead.

[test 8 bitfind  and replace m1 replace ai 9mm with shotgun]
Type = Gameshark
Activation = EndFrame
Description = test 8 bitfind  and replace
F41AD978 00FF2000
02FFFFFF FFFFFFFF
FFFFFFFF FFFFFFFF
07FFFFFF FFFFFFFF
FFFFFFFF FFFFFFFF
``