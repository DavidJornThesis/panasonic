# panasonic
ROS-driver for a Panasonic robot over the Profibus network

## Introduction

This repository contains the ROS driver for a Panasonic VR-006L manipulator using a Profibus fieldbus as a physical
connection between ROS and the Panasonic robot controller.

## Installation

The first thing you need to do is to create a local ROS environment and clone this repo into your local workspace. This can be
done as follows:

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

The next thing is to make sure that the Pyprofibus stack is 



## Usage




## Launching the driver


## Acknowledgments

The author would like to thank [Michael Büsch](https://bues.ch/cms/resources/contact.html) for using the open implementation of the Profibus protocol in python.
