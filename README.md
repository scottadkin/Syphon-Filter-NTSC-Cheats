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
```