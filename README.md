# panasonic
ROS-driver for a Panasonic robot over the Profibus network

## Introduction

This repository contains an experimental ROS driver for a Panasonic VR-006L manipulator using a Profibus fieldbus as a physical connection between ROS and the Panasonic robot controller.

## Installation

The first thing you need to do is to create a local ROS environment and clone this repo into your local workspace. This can be done as follows:

```
mkdir -p ~/catkin_ws/src
cd catkin_ws
catkin_make
source devel/setup.bash
```

After this, clone this repository into your workspace by using the HTTP or SSH of the repo:
```
cd catkin_ws/src
git clone -b https://github.com/DavidJornThesis/panasonic/
```

The next thing is to make sure that the Pyprofibus stack is properly installed. To install this, please check the [author's website](https://bues.ch/cms/automation/profibus.html), his [GitHub page](https://github.com/mbuesch/pyprofibus/) or the [Python (pypy) webpage](https://pypi.org/project/pyprofibus/#description). 

To check if this stack is properly installed on your system's python, you can verify it by launching the python shell in the terminal and check if there are no import errors:
```python
python
import pyprofibus
```
If no error shows up, the stack is properly installed.

The last thing you need to do is to adjust a few paths in some files. First, go to the ``` vr_driver/config ``` folder and change in ```panaprofi.config``` the specified path of the serial interface. This either can be a USB-port or a RS232-serial port. Secondly, in this file change also the specified path of the GSD-file of the robot to your local path. Lastly, navigate to the file ```interface.py``` located in ```vr_driver/scripts``` and change the local path of the config file to the adjusted path.


## Usage

A first thing is to is to make sure that a serial to RS485 adapter is used as a proxy between the serial port of the PC and the Profibus connector of the robot.



## Launching the driver


## Acknowledgments

The author would like to thank [Michael Büsch](https://bues.ch/cms/resources/contact.html) for using the open implementation of the Profibus protocol in python.
