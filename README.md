rising
=============

Packages for the simulation of the Rising

<h2>rising_gazebo</h2>

Launch files and world files to start the models in gazebo

<h2>rising_sim_bringup</h2>

Launch files that execute the complete simulation of the robot


<h2>Simulating Rising</h2>

1) Install the following dependencies:
  - [rising_common](https://github.com/RobotnikAutomation/rising_common)
  - [robotnik_sensors](https://github.com/RobotnikAutomation/robotnik_sensors)
  - [ros_kortex](https://github.com/Kinovarobotics/ros_kortex)

In order to install ros_kortex, you need to execute:

```bash
sudo apt install python3 python3-pip
```
```bash
sudo python3 -m pip install conan
```
```bash
conan config set general.revisions_enabled=1
```
```bash
conan profile new default --detect > /dev/null
```
```bash
conan profile update settings.compiler.libcxx=libstdc++11 default
```
```bash
mkdir -p catkin_workspace/src
```
```bash
cd catkin_workspace/src
```
```bash
git clone https://github.com/Kinovarobotics/ros_kortex.git
```
```bash
cd ../
```
```bash
rosdep install --from-paths src --ignore-src -y
```
 
2) Launch RB-Sherpa simulation.

