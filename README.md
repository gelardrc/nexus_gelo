# Nexus Gelo

A ROS package for simulating the **Nexus robot** in **Gazebo**.

This package provides a simulation environment for the Nexus robot with 4WD mecanum wheels, making it suitable for testing robot behaviors and algorithms in a virtual environment.

---

## Installation

To install the package, follow the steps below:

**1. Navigate to your Catkin workspace source directory:**
   ```bash
   cd <your_catkin>/src
  ```
**2. Clone the necessary repositories:**
```bash
git clone https://github.com/RBinsonB/nexus_4wd_mecanum_simulator.git
git clone https://github.com/gelardrc/nexus_gelo.git
```
**3. Build the workspace:**
```bash
cd ..
catkin_make
```
**4. Source your workspace setup file:**
```bash
source <your_catkin>/devel/setup.bash
```
**5. Launching the Simulation/Launch your desired Gazebo simulation:**
```bash
roslaunch <your_gazebo_simulation>
```
**6. Launch the Nexus robot in the simulation:**
```bash
roslaunch nexus_gelo robot.launch
```
**7. Sending move_base Targets**

**To send navigation goals (i.e., move_base targets) for the robot:**

**Run the map_server node with your map file:**

```bash
rosrun map_server map_server <your_map>
```
**Launch the robot's navigation stack:**
```bash
roslaunch nexus_gelo mv_robot.launch
```
**Notes**

Ensure you have a valid map file for the map_server.
Replace <your_catkin> with the path to your Catkin workspace, and <your_gazebo_simulation> with the specific Gazebo simulation you want to use.
The nexus_gelo package provides the robot configuration and launch files to interface with move_base for autonomous navigation.
