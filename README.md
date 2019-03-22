# edo_ui_python

This is a python script which serves as a bare replacement for EDO Android [app](https://edo.cloud/apps/).

This work is reverse engineering of a source that used to be on comau [github](https://github.com/comau) page. Some ideas were also borrowed from this [project](https://github.com/jshelata/eDO_manual_ctrl).

## Running the code
* Before you can run the script, python package `get-key` needs to be installed. One of the easiest ways is through pip.
* [eDO_core_msgs](https://github.com/Comau/eDO_core_msgs) needs to compiled in local ROS environment.
* Export ROS environments.
* Export `ROS_IP` and `ROS_MASTER_URI` according to your system.
* Run `python setup_edo.py`

## Usability 
* This script can set up the robot to a run mode when it boots up. After every turn on, robot's joints need calibrating procedure, since EDO has no breaks and the last three joints have no breaks.
* Script can send a robot to home pose (vertical pose). When this execution is started, it is not possible to pouse robot movement.
* It supports jogging in joint and cartesian space.
* Short repetitions of movement in joint space is supported.
* If emergency button is pressed, the script can power back the motors. 

## Problems
* Rotations around the cartesian axis for jogging are not named correctly. Comau has some non-standard naming of angles. Also, rotations jogging is very slow and limited.
* Robot can be stuck in mode 3 (MOVE), the script can not handle this situation. Using an app is advised in this case. 
