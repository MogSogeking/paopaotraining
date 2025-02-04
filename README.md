# Pao Pao Training Mode #

## Getting Started ###
Pao Pao Training Mode is a tool on top of Fightcade witch gives you Dummy control and record/play features for Garou Mark Of The Wolves.

### Prerequisites ###
* Install [python 3.7](https://www.python.org/ftp/python/3.7.3/python-3.7.3.exe)
* Latest [Unibios](http://unibios.free.fr/download.html) and be able to use it in offline Fightcade 1
* Latest [Fightcade 1](https://www.fightcade.com/download/windows)

### Features ###
* Dummy control
* Record and play p2 inputs
* Record on multiple slots and replay a random slot

### Instructions ###
1. Click on **Clone or Download** and **Download ZIP**
2. Run run_input_viewer.bat and test your controller inputs
3. Report your controller inputs in input_map.ini **player 2 and "Stop" inputs must be keyboard letters (ex: Z for Up input)**

### Usage ###
1. Run offline fightcade emulator, garou (in mvs only, press START+A+B+C in game to open unibios menu) and enable infinite power, infinite life and infinite time
2. Chose P1 and P2 characters
3. run run_pao_pao_training.bat and start training

### Recording ###
0. **Do not forget to remove the default emulator input shortcuts (ABC/BCD/ABCD are by default mapped to respectively a/s/d keys)**
1. Press your p1-dummy button to enable p2 controls
2. Press your record button to start recording
3. Input what you want p2 to do
4. Press your stop keyboard letter
5. Press your p1-dummy button again to disable p2 controls
6. Press your play button to start the recorded replay

### Multiple slots and random replay ###
You can change record slots with the next_record and prev_record buttons (defaulted to start and select)
To record different inputs on the different slots, proceed as follows :
1. Press your p1-dummy button to enable p2 controls
2. Press your record button to start recording
3. Input what you want p2 to do
4. Press your stop keyboard letter
5. Press either your next_record button or prev_record button to change slots
6. Repeat steps 2/3/4
7. You can repeat step 5 and 6 to record yet another slot
8. Finally press your random_play button to pick and play one of your random slots

Note that you can still play the currently selected slot with the play button, and change slots with next_record and prev_record to just go through your recordings.

Last thing to note, the number of slots is currently fixed at 3. If you want to change it, simply open the pao_pao_training.py file, and look for the line :
```TOTAL_SLOTS = 3```
Then just change the number if you want a different amount of slots. Save the file and launch run_pao_pao_training.bat

### input_map.ini ###
```
[p1 controls]
p1-up = ABS_HAT0Y
p1-down = ABS_HAT0Y
p1-left = ABS_HAT0X
p1-right = ABS_HAT0X
p1-a = BTN_WEST
p1-b = BTN_SOUTH
p1-c = BTN_NORTH
p1-d = BTN_EAST
p1-dummy = BTN_TR

[p2 controls]
p2-up = z
p2-down = s
p2-left = q
p2-right = d
p2-a = i
p2-b = k
p2-c = o
p2-d = l

[record controls]
record = BTN_TL
stop = a # only keyboard letter working
play = ABS_Z
next_record = BTN_START
prev_record = BTN_SELECT
random_play = ABS_RZ
```

### NOTE: ###
**This tool is in an early stage, tested only in windows 10 and i'm not a software developer. Feel free to improve it**
