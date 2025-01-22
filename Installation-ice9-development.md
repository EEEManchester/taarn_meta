# Installation guide

You will need to configure three computers to get the TAARN project setup fully running:
- Base station computer
- MallARD on-board computer
- Bluerov on-board computer

## Base station computer
1. Install the QGroundControl software

You can download the software from their official website: https://qgroundcontrol.com/.

2. Install [taarn_basestation_ros](https://github.com/EEEManchester/taarn_basestation_ros/tree/main)
```
git clone -b main git@github.com:EEEManchester/taarn_basestation_ros.git
```

Follow the instruction to install dependencies and run the package.

## MallARD on-board computer
Install [taarn_mallard_onboard](https://github.com/EEEManchester/taarn_mallard_onboard/tree/main)
```
git clone -b main git@github.com:EEEManchester/taarn_mallard_onboard.git
```

Follow the instruction to install dependencies and run the package.

## Bluerov on-board computer
Install [taarn_bluerov_onboard](https://github.com/EEEManchester/taarn_bluerov_onboard/tree/main)
```
git clone -b main git@github.com:EEEManchester/taarn_bluerov_onboard.git
```

Follow the instruction to install dependencies and run the package.
