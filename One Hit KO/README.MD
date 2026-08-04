# One HIT KO Cheat(NTSC)
Forces your max health to 1, if you pick up any armour it will be reset back to 0.


## Version 3.0 Notes
All the cheats have been merged into a single cheat, the rhomers fuel tank bug still happens with this version.

# Known Issues v3.0
- Playing Rhomer's Base with cheat activated stops one of the fuel tankers from having C4 placed under it, disable cheat and restart from last checkpoint to fix issue.


## Version 2.0(v1_SCUS-94240.cht) Notes
I've added some additional checks to help prevent bugs when you have Georgia Street enabled while playing another level, the cheat will also wait a few level ticks to apply to prevent messing up data when the level loads.

- Each cheat checks to see if you are in a menu or loading state.
- If you are not in a loading state the cheat will check what mission index you are on.
- If you are on the correct mission index the cheat will check if you are on a first load attempt or reload(died, failed objective....).
- Once the level ticks count is above a certain value all your armour will be removed and you will be left with 1 health, picking up armour automatically gets removed



# Duckstation Install
- Download the cheat file from https://github.com/scottadkin/Syphon-Filter-NTSC-Cheats/blob/main/One%20Hit%20KO/SCUS-94240.cht
![Download file](images/pic0.png)
- Run Duckstation
- Launch Syphon Filter NTSC
- Open Duckstations Game Properties Window
![Download file](images/pic1.png)
- Go to the cheats tab, click the import and then click import from file.
![Download file](images/pic2.png)
- Select the downloaded file and click open.
![Download file](images/pic3.png)
- You should now see a new cheat group called "One Hit KO", you can now tick the levels you want to cheat active.
![Download file](images/pic4.png)



## Version 1.0(v1_SCUS-94240.cht) Notes


Each cheat checks to see if you are on the correct mission, if you are not in the current mission it shouldn't run to prevent issues with other memory addresses being overridden, however after some more play testing there are still a few issues with loading and objectives in some missions not working correctly so it's best to toggle only the mission you are currently on until I make a better cheat.

# Known Issues
- Playing Rhomer's Base with Georgia Street cheat activated stops one of the fuel tankers from being able to have C4 placed under it, disable the Georgia Street cheat and restart from last checkpoint to fix issue.
