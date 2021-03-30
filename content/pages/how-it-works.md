---
title: "How it works"
date: 2020-04-18T10:07:21+06:00
# post image
image: "images/blog/post-1.jpg"
# post type (regular/featured)
type: "featured"
# meta description
description: "This is meta description"
# post draft
draft: false
---

### The full Cloud 9 cleaning system includes several parts:

- An autonomous desk cleaning robot, named Clyde.
- A navigation stack for moving the robot between desks and mapping an area.
- A database that holds the locations of all tables, their sizes and colours.
- An arm that is attached to Clyde that cleans the desk.
- An accompanying app that facilitates desk booking.
- A Raspberry Pi comtroller computer.

These parts come together to make an autonomous sanitising system for desk tops and other flat surfaces in spaces such as libraries.

Below are more in-depth descriptions of each sub-system.

![image](../media/stateDiagram.png)
## ROS2 
The core software running on the robot is the Robot Operating System 2(ROS2). ROS2 is a collection of software libraries for developing robot systems, organised as packages. It is the successor to ROS, and aims to provide several updates to its predecessor to reflect the changes in robotics since it was made in 2007. 
ROS2 works by creating nodes that are responsible for certain functions in the system, like navigation and vision. It then provides several ways for the nodes to communicate and run in paralell, which is important when trying to integrate several subsystems of a robot. Especially vital are topics, which are communication channels that nodes can publish and subscribe to, that carry data of a specified type, like a number. In ClyDe we make use of many of these features. 
![image](../media/rosgraph.png)

## Webots Simulator
Since we were unable to create a physical system, a simulator was needed to test our robot. Webots was used for this, as it is easy to use and integrates with ROS2 well. Webots makes changing the robot or its enviroment quick and simple. This is especially useful if you want to test new features, or repeat a test many times. In these ways the simulator is superior to a physical system for development. 
ROS2 integration happens through the webots-ros2 package, that provides an interface between the two. Tha package discovers important components like motors and sensors in Webots, and makes sure they subscribe or publish to the appropriate topics in ROS2. For example, webots_ros2 discovers ClyDe's camera, and makes sure it publishes to the 'camera/image_raw' topic. 
Especially useful is the webots_ros2_turtlebot package which provides an interface especially made for the Turtlebot 3, as well as several examples on how to use the Turtlebot 3 for map-building and navigation. Integrating ROS2 and Webots this way is preferrable to writing controller software directly in webots. This is beacuse a physical system could inherit a large part of the software written using ROS2 because it is used by most robots, including the Turtlebot 3. Webots controllers cannot do this, and would need to be rewritten using ROS2.

### The Mobile App:

When a user scans the QR code through our app, the app will connect to the database running in the background and update the status of the corresponding table.

If the user chooses to check in a table, the table will be marked “occupied” as an indication of being used.

If the user chooses to check out a table, the table will be marked “dirty” as an indication of needs cleaning.

The app is implemented using Android Studio with Kotlin.

### The Database:

The booking database is built based on mysql. The database will store all the specific data on the desks, including location ,status (i.e. occupied, clean, dirty), usage timer and other desk attributes. It's one of the core parts of our cleaning system. Users will access the database by using the Clyde app and our robot will use mysql-python connector to get the target location and find the suitable path in using its navigation.


### Navigation:

The navigation sub-system employs Clyde’s 360° LIDAR unit to see his environment while his onboard Raspberry Pi computer to determines navigation routes - as seen in the photo below. (remove the photo if animation).

![image](../media/RVIZ.PNG)

- Before Clyde is able to work on his own in a library or office, he uses a method called Simultaneous Localisation and Mapping (SLAM) to generate a detailed Occupancy Grid Map of its environment using LIDAR, which can then be used later for pathfinding. A qualified technician performs this mapping on set-up by driving Clyde around the environment manually.  The animation … shows an example of the mapping in action.

![image](../media/test_world_OGM.png)

- Clyde uses the Navigation2 ‘navigation stack’ - driven by the A* search algorithm - to move between desks, while LIDAR helps Clyde detect and avoid obstacles, both stationary and moving.

- All of the above is handled by a package of automatic python scripts, meaning Clyde can turn on and go all by himself. These scripts tell Clyde where to go by querying - using WiFi - Clyde’s accompanying database that holds the positions of all tables, this information is then published using a ROS2 action client.

### Computer Vision

Clyde uses computer vision to perform two separate tasks. (preconditions before cleaning can be performed)

Before any cleaning is performed, ClyDe will keep adjusting the angle of the camera, take pictures of the current table and perform the following two steps.

1. Scanning QR code on desk.
Firstly, ClyDe performs a zoom in function on the picture which separates the picture into small pieces, then it tries to detect any QR codes using pyzbar on each piece of them. Pyzbar is a python package for dealing with QR code, using the decode() function in this package, ClyDe retrieves the information from the QR code. Once ClyDe gets the information from the table , it checks if the current table number matches the desired one.


2. Detecting obstruction on desk.
After the first step is checked, the robot will use a picture of the whole table and perform an obstruction detection algorithm on it.  For obstruction detection,  ClyDe chooses OTSU algorithm thresholds any obstruction into black and thresholds the table into white and it is invariant to different lightning conditions, brightness...etc. This ensures the desk is empty before any cleaning is performed.

Once the cleaning is done, the robot will connect to the database and update the table’s status to “free”.
![image](../media/illu3.jpg)

### The Arm

Once positioned at the desired desk, the arm performs the cleaning motion itself. The current version of the robot uses the PincherX 100 (?) robotic arm, which offers 5 degrees of freedom. The arm detects the surface of the desk, then carries out a series of movements to perform the sanitisation.

### The Cleaner

> The end of the arm is equipped with a custom...

### Methods:

> “Explain the key methods of how you got your system to work”

### System Diagrams:

> “You should include images (where available) which illustrate the methods you used, how the system works etc. This can include system diagrams, images of your system in certain states etc.”
