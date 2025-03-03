## Hardware preparation
Before you can start the software, you must prepare the hardware first.

1. Start the base staton PC, password is manchester.
2. Plug in both joysticks. If bluetooth connection is preferred, then long press the PS button until light is on. Blue light is for Bluerov and red light is for MallARD.
3. Install batteries into both robots. You should hear the classic ESC beeping on both robots.

*Safety warning: From this point onwards, you must resist the temptation of putting your fingers in the thrusters, not until the batteries are removed or fully cooked.*

3. Perform vacuum test if needed.
4. Do not yet put the robots in water. Complete the software preparation, test the joysticks, then lower the robots into water if all working fine.

## Software preparation

_Note: All steps are performed on the base station PC._

1. Start four terminal windows, or one terminal but having four divisions.

You may want to have your own terminal layout, but here is what I like:
```
---------------------
|         |         |
|    1    |    2    |
|         |         |
---------------------
|         |         |
|    3    |    4    |
|         |         |
---------------------
```

2. In terminal 1, start Base station software
```shell
runros1
start_basestation
```

3. In terminal 2, start QGround Control. QGround Control does not do much but is needed to initialise pixhawk IMU.
```shell
qgroundcontrol
```

4. In terminal 3, start Bluerov software
```shell
sshbluerov
# password: bluerov
start_robot
```

5. In terminal 4, start Mallard software
```shell
sshmallard
# password: bluerov
start_robot
```

6. Start Foxglove Studio and connect to ROS1 via IP address (see [Foxglove-Studio-Guide.md](FOXGLOVE_STUDIO_GUIDE.md)).

## Pre-sailing check
1. Test the robots individually:

   a) arm the robot.
   
   b) push lightly on the joysticks/buttons.
   
   c) check whether the thrusters respond correctly.

   d) disarm the robot.
   
3. Final check of all cylinders are free from any form of moisture, e.g. mist and standing water, and all penetraters and end caps are properly installed.

## Sail
1. Lower both robots into water, be cautious of the tether of the Bluerov getting tangled somewhere.
2. Arm the robot and drive them away from the tank walls
3. Turn on depth control of the Bluerov.
4. Enjoy.

## Mapping
1. To reset mapping, you will need to restart MallARD software from terminal 4, control-C shutdown and `start_robot` again.
2. To fix the map, you will need to open a new terminal (or what I like is to open a new tab in Terminal 1) and type:
```
sshros1
fixmap
```
3. To restart mapping, in the `sshros1` terminal, type:
```
unfixmap
```

If the mapping has gone wild, you will have to reset the mapping. Normally it is needed when you move the robot into the water tank.
