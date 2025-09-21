# Syphon Filter NTSC Cheats


Ai Max danger are 216 bytes apart
```
[Instant AI Max Danger]
Type = Gameshark
Activation = EndFrame
Description = Enemies will be able to damage to you instantly instead of waiting for danger bar to fill up.
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
- First Try +1AE724 , retry +1AE454 (based on last addresses)
- Pharcom Warehouses, addresses same distance apart but on retry they are 1696 bytes before the first try address.
- First Try +1AC6F8, retry +1AC058
- Missile Silo, addresses same distance apart but on retry they are 272 bytes before the first try address.
- First Try +1AD994, retry +1AD884

# Mission Index Byte
- +0116474


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






# AI structure?

Example:
- Last Fire Timestamp/TickID: 018B000
- AMMO +14(HEX) offset from fire timestamp
- Bullets To Fire In Current Burst + 1D
