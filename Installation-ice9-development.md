# Installation guide

You will need to configure three computers to get the TAARN project setup fully running:
- Base station computer
- MallARD on-board computer
- Bluerov on-board computer

## Base station computer
1. You need a machine running Ubuntu 16.04 or Ubuntu 16.04 in docker.
2. Install [ROS melodic](https://wiki.ros.org/melodic/Installation/Ubuntu) (recommend to use Desktop-Full Install).
3. Install [QGroundControl](https://qgroundcontrol.com/).
4. Install [Foxglove Studio](https://foxglove.dev/download) or use RVIZ for visualisation.
5. Install [taarn_basestation_ros](https://github.com/EEEManchester/taarn_basestation_ros/tree/main).
6. Set up .bashrc
```shell
cat >> ~/.bashrc<< EOF
source ~/taarn_basestation_ws/devel/setup.bash #NOTE if you are using docker, you need to replace "~" with "docker_data"

export ROS_IP="172.16.0.101"
export ROS_MASTER_URI="http://172.16.0.101:11311"
export ROS_HOSTNAME="172.16.0.101"
export BLUEROV_IP=172.16.0.103
export MALLARD_IP=172.16.0.100

alias start_basestation='roslaunch taarn_basestation_bringup basestation.launch'

alias qgroundcontrol="~/Desktop/QGroundControl.AppImage" #Note change to the correct directory
alias runros1="~/Dockers/dockers/ros1_melodic/run.sh" #Only needed for docker, change to the correct docker script location
alias shellros1="~/Dockers/dockers/ros1_melodic/shell.bash" #Only needed for docker, change to the correct docker script location

function get_ssh_done() {
	ssh $1
	while test $? -gt 0
	do
		echo "Trying again ..."
		ssh $1
	done
}

alias sshbluerov="get_ssh_done $BLUEROV_IP"
alias sshmallard="get_ssh_done $MALLARD_IP"

function fixmap() {
	rosparam set /hector_mapping/map_update_angle_thresh 1000
	rosparam set /hector_mapping/map_update_distance_thresh 1000
	echo done
}

function unfixmap() {
	rosparam set /hector_mapping/map_update_distance_thresh 0.4
        rosparam set /hector_mapping/map_update_angle_thresh 0.06
	echo done
}
EOF
```
7. Connect the PC to the TARRN network switch and manually change IPv4 address to `172.16.0.101`.

## MallARD on-board computer
Install [taarn_mallard_onboard](https://github.com/EEEManchester/taarn_mallard_onboard/tree/main)
```
git clone -b main git@github.com:EEEManchester/taarn_mallard_onboard.git
```

Follow the [instructions](https://github.com/EEEManchester/taarn_mallard_onboard/blob/main/install/INSTALL.md) to install dependencies and run the package.

## Bluerov on-board computer
Install [taarn_bluerov_onboard](https://github.com/EEEManchester/taarn_bluerov_onboard/tree/main)
```
git clone -b main git@github.com:EEEManchester/taarn_bluerov_onboard.git
git clone -b main git@github.com:EEEManchester/taarn_bluerov.git
```
