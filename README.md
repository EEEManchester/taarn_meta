# taarn_meta
A collection of repositories for TAARN.

## Development by ICE 9
### Base station software
- Bring up ROS package: [EEEManchester/taarn_basestation_ros](https://github.com/EEEManchester/taarn_basestation_ros/tree/ice9) _ice9 branch_
- Visual virtual tether: [EEEManchester/visual_virtual_tether]() **TODO**
- docker:
### Bluerov software
`taarn_bluerov_obard` is the ros package contains all the custom launch files and configurations specifically for the TAARN project. It is designed only for TAARN.
`taarn_bluerov` is the ros package contains the control functions (`bluerov_control`) and PhD work (`bluerov_autonomy`). It is more of a standard package that can be used by other projects.
- Bring up ROS package: [EEEManchester/taarn_bluerov_onboard](https://github.com/EEEManchester/taarn_bluerov_onboard/tree/ice9) _ice9 branch_
- Bluerov controller: [EEEManchester/taarn_bluerov](https://github.com/EEEManchester/taarn_bluerov/tree/ice9) _ice9 branch_
- docker:
### Mallard software
- Bring up ROS package: [EEEManchester/taarn_mallard_onboard](https://github.com/EEEManchester/taarn_mallard_onboard/tree/ice9) _ice9 branch_
- docker:

## Deverlopment by Tom Breeze
### Base station software
- ros2: [EEEManchester/taarn](https://github.com/EEEManchester/taarn)
- ros2: [EEEManchester/taarn_mallard](https://github.com/EEEManchester/taarn_mallard/)
- ros2: [EEEManchester/taarn_bluerov](https://github.com/EEEManchester/taarn_bluerov)
- ros1: [EEEManchester/taarn_mallard_basestation](https://github.com/EEEManchester/taarn_mallard_basestation)
- ros1: [EEEManchester/taarn_ros1_basestation](https://github.com/EEEManchester/taarn_ros1_basestation)
### Bluerov softare
- ros1 (inaccessible): [tbreezeuom/taarn_bluerov_onboard](https://github.com/tbreezeuom/taarn_bluerov_onboard/)
- ros1: [EEEManchester/taarn_bluerov_onboard](https://github.com/EEEManchester/taarn_bluerov_onboard/tree/main) _main branch_
#### Note
_tbreezeuom/taarn_bluerov_onboard_ is the git remote found on the Bluerov, as returned by `git remote get-url origin` shell command. _EEEManchester/taarn_bluerov_onboard_ seems to be a duplicate of it.
### Mallard software
- ros1 (inaccessible): [tbreezeuom/mallard_old_ros_repo](https://github.com/tbreezeuom/mallard_old_ros_repo)
- ros1: [EEEManchester/taarn_mallard_onboard](https://github.com/EEEManchester/taarn_mallard_onboard/tree/tb) _tb branch_
#### Note
_tbreezeuom/mallard_old_ros_repo_ is possibly private and no duplicate is found in EEEManchester. The entire content is copied into _EEEManchester/taarn_mallard_onboard_.

## Other related
- MallARD meta [EEEManchester/MallARD](https://github.com/EEEManchester/MallARD)
