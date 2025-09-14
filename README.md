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

# First Load & Retry AI Weapon ID Notes
- Georgia Street, addresses same distance apart but on retry they are 396 bytes before the first try address.
- First Try +1AA204, retry +1AA078



# AI structure?

Example:
- Last Fire Timestamp/TickID: 018B000
- AMMO +14(HEX) offset from fire timestamp
- Bullets To Fire In Current Burst + 1D

Mission Cheats
```
[Mission 1 Give AI M79(Retry Loads)]
Type = Gameshark
Activation = EndFrame
Description = All NPC's will have M79.
301ADAA8 10
301AD978 10
301AA700 10
301AA74C 10
301AA584 10
301ADA5C 10
301ADA10 10
301AA960 10
301AA538 10
301AA61C 10
301AD9C4 10
301AA914 10
301AA8C8 10
301AA87C 10
301AA9AC 10
301AA830 10
301AA078 10
301AA240 10
301AA1F4 10
301AA15C 10
301AA1A8 10
301AA28C 10
301AA324 10
301AA3BC 10
301AA370 10
301AA408 10
301AA454 10
301AA0C4 10
301AA4A0 10
301AA668 10
301AA6B4 10
```