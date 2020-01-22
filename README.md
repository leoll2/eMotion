# eMotion: the in-car Virtual Reality experience

This is a basic prototype for eMotion, an entertainment system for autonomous featuring virtual reality.

![eMotion demo](https://github.com/leoll2/eMotion/blob/master/media/emotion_demo.gif)

## Setup

If you have an IMU, connect it to the main computer via serial port (UART, 9600 baud).

## Installation

In Ubuntu 18.04, install [ROS melodic](http://wiki.ros.org/melodic/Installation/Ubuntu) (destktop-full recommended) and [OpenCV](https://opencv.org/)

You will probably miss the following package, install it:
```
sudo apt install ros-view-controller-msgs
```

Then clone this repository:
```
git clone https://github.com/leoll2/eMotion.git
```

## Build

```
catkin_make
```

## Run

```
source devel/setup.bash
roslaunch emotion_launcher/emotion.launch
```

## Disclaimer

Everything is still experimental. If some ROS package is missing, you'll be notified when building or running the app: install it and rebuild to solve the issue.
