rising
=============

Packages for the simulation of the Rising

You will need to install Gazebo 9.14 to make simulation work due to RS_BPearl lidar.

Please note that we are using Gazebo default version 9.0 in melodic but to make simulation work you will need to install Gazebo 9.14.

```bash
sudo apt-get remove ros-melodic-gazebo* gazebo*
```
```bash
sudo sh -c 'echo "deb http://packages.osrfoundation.org/gazebo/ubuntu-stable lsb_release -cs main" > /etc/apt/sources.list.d/gazebo-stable.list'
```
```bash
wget http://packages.osrfoundation.org/gazebo.key -O - | sudo apt-key add -
```
```bash
sudo apt-get update
```
```bash
sudo apt-get install gazebo9 gazebo9-* ros-melodic-gazebo9-*
```
```bash
sudo apt upgrade
```

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
 
2) Launch Rising simulation.

